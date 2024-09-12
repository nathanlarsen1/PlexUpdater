<h1>Plex Updater on Ubuntu Linux Server</h1>


<h2>Description</h2>
This project consists of a Bash script that automatically updates Plex Media Server on an Ubuntu Linux server. The script starts by determining the installed version of Plex Media Server. It then downloads a JSON file from the Plex website and processes the data to determine the latest version available. Next, it compares the installed version to the version on the website. If the version on the website is newer, the script downloads the installation file and installs the latest version of Plex Media Server. After the installation is finished, the script deletes the installation file.<br/>

<h2>Language and Applications</h2>

- <b>Bash</b>
- <b>Plex Media Server</b>

<h2>Environments Used </h2>

- <b>Ubuntu 22.04.4 LTS</b>

<h2>Setup</h2>

- Create the plex_updater directory:</br>
  $ sudo mkdir /opt/plex_updater

- Create /opt/plex_updater/plex_updater.sh and copy the contents of 
  plex_updater.sh.txt into /opt/plex_updater/plex_updater.sh:</br>
  $ sudo nano /opt/plex_updater/plex_updater.sh

- Grant the execute permissions to /opt/plex_updater/plex_updater.sh:</br>
  $ sudo chmod +x /opt/plex_updater/plex_updater.sh

- Setup Cron Job to run the plex_updater.sh script at selected time:</br>
  $ sudo crontab -e

- Add the following lines to crontab:</br>
  <span>#</span> Run plex_updater.sh every day at 12:00am.</br>
  0 0 * * * /opt/plex_updater/plex_updater.sh > /dev/null 2>&1
</br>
</br>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
