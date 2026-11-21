Meow — Easy

Category: Starting Point
Difficulty: Easy

Overview

This challenge introduces the basic workflow of connecting to and interacting with a target machine on Hack The Box.

Steps

1. Connect to the target
Using Pwnbox (HTB’s browser-based VM) is the simplest way to connect, since it comes pre-configured with the HTB VPN and common tools already installed.

2. Get the target IP
Starting the machine provides its IP address, which is used for all subsequent steps.

3. Enumerate open ports
Run an Nmap scan against the target to identify open ports and the services running on them:

bash
nmap <target-ip>

This reveals which services are exposed (e.g., Telnet, SSH) and can be targeted next.

4. Connect to the open service
Once a relevant service is identified, connect to it directly using its own client, for example:

bash
telnet <target-ip>

5. Find valid credentials
Credentials can sometimes be guessed from a wordlist or inferred from the challenge’s built-in hint. For this challenge use the hint

6. Retrieve the flag
After logging in:

bash
ls          # list files in the home directory
cat flag.txt # view the contents of the flag file

This displays the flag, completing the challenge.
