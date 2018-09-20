# OSCP_Review
Penetration Testing: a legal and authorized attempt to locate and successfully exploit computer system for the purpose of making those systems more secure. The process includes probing for vulnerabilities as well as providing proof of concept attacks to demonstrate the vulnerabilities are real. Proper penetration testing always ends with specific recommendations for addressing and fixing the issues that were discovered during the test.

OSCP - Offensive Security Certified Professional: It's a completely hands-on offensive information security certification. The OSCP challenges the students to prove they have a clear and practical understanding of the penetration testing process and life-cycle through an arduous twenty-four (24) hour certification exam.

-------------------------------

Despite the fact that OSCP is for beginners, a lot of people having problems to pass the exam. That's why I decided to write a review.

Note: Anything I will say in this review is from my point of view, and how I experienced the OSCP.

# First - Preparation for OSCP:

The way I see it, almost every concept you will need to pass the Exam is already explained in the Material of OSCP.

# References:

1- Escaping Restricted Shell: https://pen-testing.sans.org/blog/2012/06/06/escaping-restricted-linux-shells

2- Privileges Escalation (Most Common): 

2.1 - https://blog.g0tmi1k.com/2011/08/basic-linux-privilege-escalation/

2.2 - https://www.rebootuser.com/?p=1623

2.3 - Misconfigured NFS: https://www.youtube.com/watch?v=FlRAA-1UXWQ&feature=youtu.be

2.4 - Misconfigured NFS: http://www.abatchy.com/2016/10/walkthrough-vulnix-vulnhub-vm.html (Vulnix CTF).

2.5 - Memodipper Exploit: https://gist.github.com/karthick18/1686299 (This is a custom version of the original Exploit because the original exploit never worked for me).

2.6 - SudoEdit: https://www.exploit-db.com/exploits/37710/

3- Cheat Sheets: http://pentestmonkey.net/category/cheat-sheet (SQL Injection and More..)

4- https://labs.detectify.com/2015/10/02/how-patreon-got-hacked-publicly-exposed-werkzeug-debugger/ (Notable News)

5- Path Traversal Cheat Sheet: https://www.gracefulsecurity.com/path-traversal-cheat-sheet-windows/ (Windows)

6- Path Traversal Cheat Sheet: https://pentestlab.blog/2012/06/29/directory-traversal-cheat-sheet/  (Linux)

7- Msfvenom cheat sheet: http://security-geek.in/2016/09/07/msfvenom-cheat-sheet/

8- Command Injection Cheat Sheet: http://ferruh.mavituna.com/unix-command-injection-cheat-sheet-oku/ (Unix)

9- Command Injection: https://www.owasp.org/index.php/Command_Injection

# Tips:

1- robots.txt

2- Page source

# Recommended Tools:

1- Dirb

2- Nmap

3- Nikto

4- Wfuzz

5- searchsploit

6- enum4linux

# Recommended Commands:

1- ls -la

2- chmod

3- chown

4- find

5- sudo -l

6- ps aux

7- sudo su

# Recommended Scripts:

1- https://github.com/MistSpark/Scripts/blob/master/Enumeration.py

2- https://github.com/rebootuser/LinEnum

3- http://www.securitysift.com/download/linuxprivchecker.py

Final Note on preparation phase: UNDERSTANDING THE MATERIALS OR PASSING THE EXAM DEPENDS ON YOUR EXPERINCE IN THE FIELD, GOING THROUGH SOME OF THE MACHINES IN VULNHUB WOULD BE GOOD IDEA BEFORE SIGNING UP.

# Recommended Vulnhub Machines:
01- SickOS

02- Lord of Root

03- Tr0ll 1

04- Tr0ll 2

05- Darknet

06- Owl Nest

07- VulnOS

08- Sidney

09- Null Byte

10- Vulnix

# OSCP Materials and Studying:

I find the materials and course amazing, Mati was a very good instructor.

1- Go through the Videos along with the PDF or you will waste a lot of time.

# After finishing the materials, these are the modules I want you to focus on if you want to pass the Exam:

1- Windows Buffer Overflow.

2- File Transfer.

3- Privileges Escalation.

# Labs:

I can't talk much about the labs because I didn't hack any of them, I only took 1 month in the labs but I wasted the whole month without trying to enter the labs.

# Exam - How to pass OSCP Exam in less than 5 hours:

It took me only 3 hours to pass the Exam. I was already comfortable with every aspect of OSCP before signing up so I didn't have a problem passing the exam.

So, If you took my advice on reading the references and reading about the tools and commands I mentioned you will have no problem passing the exam.
You only have 24 hours to pass the exam, and another 24 to write your report:

# Exam:

You will find 5 machines in your VPN range, you don't need to hack them all, you need 70 point to pass the exam:

5 Machines:

- One machine with 10 points.

- Two Machines with 20 points.

- Two machines with 25 points (One of them is the Buffer Overflow Machine).

# Here is my methodology on passing OSCP Exam:

[+] Start with Buffer Overflow Machine.

My notes on Buffer Overflow Machine:

1- You don't need to write the exploit from scratch, you will find the script you will use in the experimental machine they provide you in the exam.

2- Don't waste your time by rebooting the program every time you find a bad character! Just send all of the possible character to the program without the null of course and examine which characters is doing weird behavior or missing.

It took me 30 minutes to hack the Buffer Overflow machine, you don't need more time because you already have everything in place and you didn't waste time rebooting the program every time you find a bad character.

[+] While working on Buffer Overflow Machine, you can simply do nmap scan on the other 4 machines. REMEBER YOU DON'T NEED TO PERFORM UDP SCAN( IT WILL WASTE YOUR TIME AND YOU WILL FIND NOTHING)

[+] ONLY PERFORM UDP SCAN WHEN YOU ARE IN A DEAD END.

OKAY, TO TELL YOU THE SECRET BEHIND OSCP EXAMS, IT'S ALL ABOUT WEB APPLICATIONS. IF YOU FOUND A WEB APPLICATION, IT'S YOUR TARGET, THIS IS HOW YOU WILL HACK THE MACHINE, IF YOU DIDN'T FIND YOUR WAY THROUGH THE WEB APPLICATION, ONLY THEN YOU CAN TRY SOMETHING ELSE, BUT MOST LIKEY YOU WILL FIND THE OTHER WAY TO HACK THE MACHINE IS SOMETHING RELATED TO WEB APPLICATION BUT WORKING ON A DIFFERENT PORT.

[+] IF YOU FOUND A WEB APPLICATION, START BY FUZZING IT TRYING TO FIND A NEW PATHS. YOU CAN DO THAT USING WFUZZ OR DIRB.

[+] IF YOU FOUND A NEW PATHS, START BY EXAMINING IT AND SEARCHING FOR PUBLIC EXPLOITS TO EXPLOIT IT.

# I hope this review helps a lot of people to pass their exams.
# This review is for My Late Grandmother - May Allah Rest Her Soul.
