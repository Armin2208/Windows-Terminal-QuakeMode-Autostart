# Windows-Terminal-QuakeMode-Autostart
This is a tutorial on how to start the Quake Mode of Windows Terminal at user logon, without noticing it.

#Tutorial

## Set up PowerShell
First we need to allow PowerShell to run scripts. Open Windows PowerShell as Administrator. Run the command "Set-ExecutionPolicy 1".

## Download the PowerShell Script
Go to the [releases page](https://github.com/Armin2208/Windows-Terminal-QuakeMode-Autostart/releases) and download the latest .ps1-file.
Store it into a folder of your choice where it can lay down for the next months. Like your documents folder.

## Setting up Task Scheduler
Search for "Task Scheduler" and open the application. An old computer management windows opens now. Click on "new simple task" at the right side.
Choice a name of your liking, I name it "Windows Terminal QuakeMode Autostart". Then click next.
Now you can choice when to run the task. I recommend using the second last option "at login". Click again on next.
Choose start program. Next.
Now the setup asks you for a program or script. Click on browse and select the .ps1-script you downloaded earlier.
On the last page you can control your settings. Just click on finish.

Now you have everything set up! At the next PC start the Quake Mode will start automatically at logon and hopefully hide itself right after that.

## Troubleshooting
### Task doesn't run
Maybe on some notebooks the task will not run under some conditions.
Open again the "Task Scheduler. Search at the upper list of tasks our created task. Double click it to see more options.
In the tab "Conditions" uncheck all checkboxes. Then click on okay.

### Quake Mode doesn't hide at startup
Right click the download .ps1-file and choose "Edit". PowerShell ISE will open. At the second line you will see the code "-Milliseconds 300". Sometimes it helps to set the number a little bit lower or higher, depending on your machine.
This script can only hide the Terminal if it's in focus. Maybe some startup application steal it.

### Delete task
Just again open the "Task Scheduler", search for our created task on the upper list, right click and choose delete.
