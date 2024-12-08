# Advent-Of-Cyber
This will be a log to document my journey on TryHackMe throughout this month. In December they are hosting a festive raffle that focuses on a storyline invloving a parody of "The Grinch Who Stole Christmas". This raffle has many prizes such as tickets for DEFCON and PSVR headsets and much more while learning about Cybersecurity.

#### 12-07-2024.
Today I have learned about bad OPSEC, Operational Security, by finding out that Mayor Malware was behind a maliciious intent to steal peoples data by hosting a song-MP3 converter website that downloads youtube videos and converts them into downloadable mp3 files to listen offline. By browsing through the files in an AAtack Box on TryHackMe's website, I was able to find out the metadata of the file in linux using the exiftool command and seeing that it is a link to a github account that is owned by the Mayor. This command would be bad for a windows computer because of the powershell execution code found eithin the file. Luckily I used Linux instead. The script within the downloaded file is designed to collect highly sensitive information from the victim's system, such as cryptocurrency wallets and saved browser credentials, and send it to an attacker's remote server. Below I will post some info I snagged from the TryHackMe website that I liked about OPSEC stuff ^^.

Introduction to OPSEC
This is a classic case of OPSEC failure.

Operational Security (OPSEC) is a term originally coined in the military to refer to the process of protecting sensitive information and operations from adversaries. The goal is to identify and eliminate potential vulnerabilities before the attacker can learn their identity.

In the context of cyber security, when malicious actors fail to follow proper OPSEC practices, they might leave digital traces that can be pieced together to reveal their identity. Some common OPSEC mistakes include:

Reusing usernames, email addresses, or account handles across multiple platforms. One might assume that anyone trying to cover their tracks would remove such obvious and incriminating information, but sometimes, it's due to vanity or simply forgetfulness.
Using identifiable metadata in code, documents, or images, which may reveal personal information like device names, GPS coordinates, or timestamps.
Posting publicly on forums or GitHub (Like in this current scenario) with details that tie back to their real identity or reveal their location or habits.
Failing to use a VPN or proxy while conducting malicious activities allows law enforcement to track their real IP address.
You'd think that someone doing something bad would make OPSEC their top priority, but they're only human and can make mistakes, too.

For example, here are some real-world OPSEC mistakes that led to some really big fails:

AlphaBay Admin Takedown
One of the most spectacular OPSEC failures involved Alexandre Cazes, the administrator of AlphaBay, one of the largest dark web marketplaces:

Cazes used the email address "pimp_alex_91@hotmail.com" in early welcome emails from the site.
This email included his year of birth and other identifying information.
He cashed out using a Bitcoin account tied to his real name.
Cazes reused the username "Alpha02" across multiple platforms, linking his dark web identity to forum posts under his real name.
Chinese Military Hacking Group (APT1)
There's also the notorious Chinese hacking group APT1, which made several OPSEC blunders:

One member, Wang Dong, signed his malware code with the nickname "Ugly Gorilla".
This nickname was linked to programming forum posts associated with his real name.
The group used predictable naming conventions for users, code, and passwords.
Their activity consistently aligned with Beijing business hours, making their location obvious.
These failures provided enough information for cyber security researchers and law enforcement to publicly identify group members.
