Wabi-Sec: A Localized Security Auditor
I built this project for my INSA Cyber Talent Summer Camp application. It’s a security tool that doesn't just look for "bad files," but actually checks how a system is set up and gives it a "Health Score."

The "Why" Behind the Project
Most security software is built for a global audience, but I noticed something specific in Ethiopia: many people store their passwords in text files named in Amharic (like ቁልፍ or ይለፍ). Standard scanners don't look for these, so I built a heuristic engine that specifically targets these local risks.

How it works (The Logic)
This project is a hybrid. I’ve included both a local Python engine and a web dashboard to show how the system thinks.

The Scanner: My Python code actually probes the system. It checks if risky network ports are open and looks through the Desktop for those Amharic keywords I mentioned.

The Matcher: I adapted the "Smart Match" logic from my previous project, AfriVoice AI. It compares what the scanner finds against a set of security rules I wrote.

The Remediation Loop: I didn't want this to just be an alarm. If the auditor finds a risk, it suggests (or in the Python version, executes) a fix—like moving a sensitive file to a secure "vault" or killing a suspicious process.

Note on the GitHub Deployment
The index.html file here is a functional simulation. Since a browser can’t (and shouldn’t!) be able to scan your private files or close your ports for safety reasons, this site demonstrates the logic and UI.

To see the actual system-level audit, check out wabisec_pro.py in this repo.

What I learned
Building this taught me a lot about "Weighted Risks." Not every security flaw is equally dangerous. I had to decide how many "points" to take away from the System Health Score for each issue, which required a lot of research into how real malware behaves.

Wabi Tafese Grade 10 Student | Developer | Researcher
