<h1>Plex Updater on Ubuntu Linux Server</h1>


<h2>Description</h2>
The project consists of an Bash script that automatically updates Plex Media Server on Ubuntu Linux Server.<br/>

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
