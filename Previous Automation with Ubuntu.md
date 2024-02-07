# Automation work, previously using ubuntu 


My Automation Project: A Notification to remind me to take my vitamins! (at a certain time during the day.)

Problem and Context of the Automation:
To begin the "Creating a reminder system on Ubuntu," I use a combination of a command-line tool on Ubuntu and the ssh command to trigger a notification, to notify me on my Mac.

Screenshot 2024-02-02 at 15 06 52
For the next process I needed to "Create a script for the reminder": The script i chose was called "vitamin_reminder.sh" using a text editor:

Screenshot 2024-02-02 at 15 09 01
Next I used "osascript" on macOS, it is a command-line tool that allows you to run AppleScript commands from the terminal.

Screenshot 2024-02-02 at 18 48 48 Screenshot 2024-02-02 at 18 49 02
To Make the script executable:

Screenshot 2024-02-02 at 18 50 31
Lastly I used the "at" command to Schedule the reminder and to schedule the script to run at a specific time:

I had to manually install the command "at" on to my ubuntu using: "sudo apt-get install at" on my Terminal. This command allows you to schedule a one-time job to be executed at a specific time in the future. In case, I wanted to schedule my vitamin reminder script to run at a specific time.

Screenshot 2024-02-02 at 18 51 44
The Time I set it to was 15:30🕞 every day!

To make sure that my automation was running properly, there were three ways that I used to check:

The first way was to wait for the Time: 15:30 for a notification to pop up on my screen.

The second was to check, I opened Terminal on my Ubuntu and typed the command 'atq'to "view scheduled jobs" for the day. Just like the 'at' command, I also had to manually install this: for which I used the command -

Screenshot 2024-02-02 at 19 22 54
This 'atq' command displayed the job numbers and the times they are scheduled to run. Since my vitamin reminder was scheduled, I was able to see it in the list.

The Third way I could Manually Trigger the Reminder:
I wanted to quickly test my script without waiting for the scheduled time, so I learned how to execute it manually. I went to the script's directory and typed the command:

Screenshot 2024-02-02 at 19 21 41
I did encounter several problems along the way. Many times when i tried to execute a certain command, I had recieved alot of "Syntax Error" while trying to run the script. So I had to go back many times and check any mistakes I have made. I had to check for Errors in the message, and review the script. Also when I was checking to see if the project was working and I typed the "at" command, it showed me a pop up that said "Garbled Time" indicating that something was wrong, so I also had to research ways to avoid this. The "garbled time" error with the "at" command occurs when there's an issue with the time format tha I was providing. The "at" command needs the time to be specified in a specific format in order to work. In Ubuntu, the time format should be in HH:MM (24-hour clock), which is a mistake I made in the beginning not using 24 hour time format. I had to make sure my Ubuntu system was up to date, so I used the command "sudo apt-get update" and "sudo apt-get upgrade." Another problem I ran in to was connecting my work on Ubuntu to my mac. To do this I had to Enable "SSH" on Ubuntu. To make sure my Ubuntu machine had the SSH server installed and running following command:

Screenshot 2024-02-03 at 13 53 09 Screenshot 2024-02-03 at 13 53 14
Next was a very Important step with connecting my mac with ubuntu. I learned about a website cal "Todoist.com." With this website I made an account, and also made an account through Ubuntu. I was able to connect and sync both devices together, so that whatever I do on my mac, also happens on my ubuntu software, and vice versa.

Screenshot 2024-02-04 at 18 59 06
The photo above is a screenshot of my mac in the process of connecting my ubuntu automation, to my regular desktop.

I also wanted to connect the reminder to a sound, or a chime. So I not only see the message, "take your vitamins" but also to hear it. I was able to add the sound by using the terminal on my ubuntu. I used the following commands:

Screenshot 2024-02-04 at 18 32 37
The "paplay" I had to install in order to start choosing what sound I want to hear. While adjusting the sound settings on my terminal to make it audible.

Screenshot 2024-02-04 at 17 31 53
I also wanted to make sure that my automation was able to run automatically everyday at the same time. After searching online, I found a command called "cron." This enabled me to have the reminder message pop up automatically every day at the same time. 'cron' allows you to schedule tasks at predefined times. The command I used: crontab -e. And I had to find a command to let me adjust the time that I wanted the chime to go off, so I used the command "echo."

Screenshot 2024-02-04 at 18 27 53 Screenshot 2024-02-04 at 18 27 57
