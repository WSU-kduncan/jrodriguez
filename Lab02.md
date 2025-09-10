## Lab 02

- Name: Jaeden Rodriguez
- Email: rodriguez.192@wright.edu
## Part 1 Answers

Full / absolute path to your private key file: C:\Users\Jaequ\Downloads\labsuser.pem 

Command to SSH to AWS instance:
```
ssh -i "C:\Users\Jaequ\Downloads\labsuser.pem" ubuntu@35.168.72.154
```

## Part 2 Answers

1. `chmod u+r bubbles.txt`
    - Means: Grants "user" read access by altering the set privileges on bubbles.txt using chmod, without negating or replacing any other file permissions.
    - Assessment: Good! It allows the main owner to access the contents of bubbles.txt if they could not already. Even better, it does not modify or change any authority from groups, people, or others, allowing them to keep whatever permissions they had. 
2. `chmod u=rw,g-w,o-x banana.cabana`
    - Means: Gives the user set read and write permissions, groups access to the write clearance, and others only have access to the execute command to the banana.cabana file.
    - Assessment: Great when trying to maintain security and tighten down permissions. It gives the owner the right to access the file's contents and allows them to modify whatever is inside. Everyone else in a group, although able to edit, cannot view the changes. This grants a subtle wave of security to whatever file or document you are working on.
3. `chmod a=w snow.md`
    - Means: Chmod effectively gives only the write permission to "all" potential users, groups, and others in response to snow.md file permissions.
    - Assessment: Bad. Nobody can read or execute snow.md, effectively leaving its modified versions hidden from everyone else involved. How would you be able to save, monitor, and fix changes in your file if not a single person has the command privileges to do so? Until altered, snow.md remains isolated.
4. `chmod 751 program`
    - Means: This grants an ever stronger protection than the banana.Cabana question, creating a "hierarchical" system that gets stricter the lower you get. Users can read, write, and execute, groups can read and execute, and others can only execute.
    - Assessment: For ensuring a safe and efficient working environment for the user, limiting but allowing specific permissions creates a genuine and somewhat private workspace. This ensures that even though others can access and utilize your program, only you have permission to change it.
5. `chmod -R ug+w share`
    - Means: Recursively grants and changes write permissions to users and groups inside the share directory. That command allows swift modifications for files within the share folder.
    - Assessment: If for a shared project collaboration between users and groups, this command is the perfect way to create an equal working environment. Others can edit within this "share" directory and help with whatever process needs to be done. However, allowing too much freedom can potentially be troublesome if others are allowed to modify the area.

## Part 3 Answers
(Linux)
1. Command to create new user: sudo adduser JRodriguez
2. Path to new user's home directory: /home/JRodriguez
3. Evaluate if `ubuntu` can add files to new user's home directory: No, ubuntu does not have any permissions yet
4. Command to switch to new user: su JRodriguez
5. Command(s) to go to new user's home directory: cd /home/JRodriguez
6. Evaluate if new user can add files to user's home directory: No, access has not been modified 
7. Command to return to `ubuntu` user: su ubuntu
8. Command to return to `ubuntu` home directory: exit

## Part 4 Answers

1. Command(s) to create group named `squad` and add members: sudo groupadd squad
2. Command(s) to add `ubuntu` & user to group `squad`: sudo usermod -aG squad ubuntu
                                                       sudo usermod -aG squad JRodriguez
3. Command(s) to allow `squad` to view the `ubuntu` user's home directory contents: sudo chmod 750 /home/ubuntu
                                                                                    sudo chgrp squad /home/ubunt
4. Command(s) to modify `share` to have group ownership of `squad`: sudo chmod squad /home/ubuntu/share
5. Describe your tests and commands with the user account: Logged in as "JRodriguez" and cd /home/ubuntu/share
6. Describe the full set of permissions / settings that enable the user to make edits: Because permissiosn are set to "squad", which ubuntu has access to and owns, changes can be made accordingly

## Part 5 Answers

For each, write the command used or answer the question posed.

1. Command(s) to make file using `sudo`: sudo touch /home/ubuntu/share/madewithsudofile.txt
2. Command(s) to make file with `root`: touch /home/ubuntu/share/madewithrootfile.txt
3. Describe / compare ownership and permissions of files: Root ownership allows permissions to be changed
4. Which account can do what actions? (Type Y or N in columns)

Contents inside of `share`
| Account   | Can View  | Can Edit  | Can Change Permissions    |
| ---       | ---       | ---       | ---                       |
| `root`    |    Y       |    Y       |     Y                      |
| `ubuntu`  |    Y       |    Y       |     Y                      |
| `JRodriguez`     |    Y      |    Y       |     N                      |

`madewithsudo.txt`
| Account   | Can View  | Can Edit  | Can Change Permissions    |
| ---       | ---       | ---       | ---                       |
| `root`    |     Y      |    Y       |        Y                   |
| `ubuntu`  |     Y      |    Y       |        N                   |
| `JRodriguez`     |     Y      |    N       |        N                   |

5. Command(s) to modify permissions: sudo chmod 770
6. How to give user account `sudo`: sudo usermod

## Citations
GeeksforGeeks/Linux Handbook - Listed set Linux commands for file and directory permissions

Copilot - Answered somewhat straightforward questions and directed me to other sites, mainly assisting with seeking out basic definitions of specific commands.

ChatGPT - Fed prompts for more detailed answers like "What is sudo in Linux" and "Summarize what Ubuntu is in Linux"
