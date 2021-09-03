# Scheduled-builds-Jenkins

Steps to configure a scheduled build in Jenkins-

```

1. Create two empty temporary files to be used in a directory.

$ mkdir Trash-files
$ cd Trash-files
$ vi file1
$ vi tempo.txt

2. In Jenkins dashboard create a freestyle Job.

3. Confgigure the build=
- Enter job details like description and select the Discard old builds option.
- Scroll down to the Build Triggers section and select the Build periodically option
- In the box that appears, enter the cron syntax to schedule a build every day at 11 in the morning and at night (0 11,22 * * *)
- Scroll down to the Build section and click on Add build step
- Select Execute Shell from the drop down that appears
- Enter the command to delete the files in the temp folder in the textbox that appears - sudo rm -rf <path to your temporary folder>/{*,.*}
- Click Save

4. Testing the build
- Run the build and view the output.

```





