# Week 6 Lab Report
## Streamlining ssh Configuration
>Finding the hidden .ssh folder by searching for it using Cmd + Shift + G:
![Image](/L3_screenshots/sshfolder.png)

>### Adding the config file
![Image](/L3_screenshots/configlocation.png)

>### Editing the config file by using the TextEdit application (Default text editor for MacOS)
![Image](/L3_screenshots/editconfig.png)

>### Logging into the remote server (ieng6) with new alias
![Image](/L3_screenshots/sshcommand.png)

>### Copying a file using the new alias
![Image](/L3_screenshots/sshscp.png)

## Setup Github Access from ieng6
>### The public key's location is shown below:
![Image](/L3_screenshots/sshgit.png)

>### The private key's location on ieng6 is shown below:
![Image](/L3_screenshots/sshieng6.png)

>### Running git commands to push a change (in the repo used for the skill demonstration):
![Image](/L3_screenshots/changepush.png)

>### Link to the resulting commit:
[Here](https://github.com/ohuynh21/skill-demo-real/commit/af418b55b8f7a36f248fa272968e582c27bc94dc)

## Copy whole directories with scp -r
>### Copying the markdown-parse directory:
![Image](/L3_screenshots/copymdparse.png)

>### Running the tests (via. Makefile) on ieng6:
![Image](/L3_screenshots/mdparsetestonieng6.png)

>### Putting it all together to copy and run the tests in one line:
![Image](/L3_screenshots/inoneline.png)