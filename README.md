# Anope Startup Scripts (1.0.0)
Startup scripts for the Anope IRC services - uses the "screen" command to manage a session. This also restarts the Anope process if it crashes.

Official support sites: [Official Github Repo](https://github.com/fstltna/AnopeStartup)

---
These start up the Anope services at boot time with a "screen" process.

1. Copy **anope** into **/home/ircdaemon/bin** - make sure it is executable
2. Copy **startanope** into **/home/ircdaemon/services** - make sure it is executable
3. Put **@reboot /home/ircdaemon/bin/anope start** into your crontab

When you want to view the Anope console, just enter "**screen -r**" in your shell.

To disconnect from the Anope console just press **CTRL-A CTRL-D**. This will leave it running and you can reconnect to it again.

If you want to turn off the server respawning type "**touch /home/ircdaemon/services/nostart**". To reenable it type "**rm /home/ircdaemon/services/nostart**".

If you need to install the dependancies needed for the utils, just run the AnopeStartup/installdeps before using them. You can also manually install them if you like.
---
Note: If you don't already have the "screen" tool installed you will need to install it by "**sudo apt-get install screen**".
