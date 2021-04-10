# SSHKeysSetup
Documentation for anyone looking to setup SSH keys (on Windows) to work with Github

### SSH Keys are secure way to work with your Github repositories. No need enter your UserName and Password for everytime you connect to Github.

### Requirements
* Windows machine
* Git Desktop installed. (If you have not done this alread, Please install it from [Git Scm](https://git-scm.com/downloads)) 

### Step 1: Generate your SSH keys.
* Open Git Bash.
* Generate your keys using command below,
    ```
    $ ssh-keygen -t ed25519 -C "your_email@example.com"
    ```
    - Just press "Enter" for file location. It will accept default file location for the keys.
    - Enter a strong paraphrase when prompted. This is an additional security on top of the SSH keys. You will be prompted for this paraphrase when you SSH for the first time you       logged into the machine (e.g. after a machine restart).
* Copy the public key to the clip board,
    ```
    $ clip < ~/.ssh/id_ed25519.pub
    ```
### Upload the public key to your Github Acccount.
* From your profile -> Settings -> SSH and GPG Keys -> New SSH Key -> Paste your Public key from clip board

### Test your SSH Connection .
    ```
    $ ssh -T git@github.com
    ```
# You are done with the SSH Setup !!

### Hope this is useful, Your Contributions are welcome.

### References for more in depth understanding
* https://docs.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent
* https://docs.github.com/en/github/authenticating-to-github/working-with-ssh-key-passphrases
* https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/cloning-a-repository
