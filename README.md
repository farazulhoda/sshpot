# SSHPOT


Description: 

    An ssh server that never authenticates. Instead, it logs the username,
    password, IP address and time of every login attempt.


Installation:

    1. Generate an RSA public key for use by the server:
        > ssh-keygen -t rsa 

    2. Edit config.h to set the desired options. In particular, you must set
       RSA_KEYFILE to the path to the public key generated in step one. LOGFILE 
       must be set to a location where the user running sshpot can write.

    3. Compile the software:
        > make
        # make install (optional, but necessary to listen on ports < 1024.)


Usage:

    sshpot [-h] [-p <port>]
        -h  --help          Display this usage information.
        -p  --port <port>   Port to listen on; defaults to 22.
        
       

<img width="1440" alt="Screenshot 2023-04-24 at 06 49 20" src="https://github.com/HaroonArif1/sshpot/assets/99000767/3fb7c1dd-bf93-492b-8207-ab28bcd24427">
<img width="1440" alt="Screenshot 2023-04-24 at 06 49 52" src="https://github.com/farazulhoda/sshpot/assets/99000767/3be16239-a637-4af5-88f5-f92475d4fe96">
<img width="1440" alt="Screenshot 2023-04-24 at 06 51 35" src="https://github.com/farazulhoda/sshpot/assets/99000767/0ff286c0-b7dc-4ef9-a9c6-c78569a528f6">
<img width="845" alt="Result" src="https://github.com/farazulhoda/sshpot/assets/99000767/f2e8b0ee-0016-4205-87c3-bc36f03cc214">
<img width="1440" src="https://github.com/HaroonArif1/sshpot/assets/99000767/aecbb7bf-ec35-44a9-a06c-a6bd93c73e2f">



Dependencies:

    libssh http://www.libssh.org/
