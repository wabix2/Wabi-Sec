Wabi-Sec: My Heuristic System Auditor (v2.1)
I built this project for the INSA Cyber Talent Summer Camp 2026 application. It’s a tool that looks at a computer’s "health" not just by finding viruses, but by checking how the system is behaving.

Why I built this
A lot of security tools are made for global users, but I wanted to build something that felt local. For example, many people in Ethiopia store passwords in text files named in Amharic. Most scanners ignore these, so I added a feature to my scanner that specifically looks for those keywords (like ይለፍ).

This project also carries over the "Smart Match" logic I used in my previous project, AfriVoice AI. I wanted to see if I could take that same matching engine and use it for cybersecurity instead of healthcare or agriculture.

How it works (The Logic)
Wabi-Sec doesn't just guess if a system is safe. It follows a three-part process I designed:

The Scanner: It probes the local environment. It checks if risky ports like Port 80 are open and scans for processes running from temporary folders—a common trick used by malware.

The Rule Database: I created a database.json file that acts as the "brain." It stores different security risks and assigns them a "weight" based on how dangerous they are.

The Matcher: This is the core engine. It takes the scanner’s results, matches them against the rules, and subtracts points from a starting "Health Score" of 100.

Technical Challenges
The hardest part was deciding the "weights." I had to research which risks were actually critical (like unencrypted keys) versus which were just warnings (like an active guest account). I also had to make sure the Amharic character matching didn't break the scanner logic.

My Goal
Through this project, I want to show that I understand the modular architecture of security tools. I’m not just writing one long script; I’m building a system where the scanner, the logic, and the data are all separate and work together.
