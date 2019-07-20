# enable_avscan
Sets up daily, weekly and monthly anacron scripts to scan parts of your system with clamscan. Will attempt to install clamav using apt, so you'll have to install it yourself if you aren't on a Debian based system. Automatic scans output to log files in /var/log, and logrotate configurations are also created to rotate the log files regularly.

First open the script in your editor, scroll down to line 30 and edit the locations for the daily, weekly and monthly scans, respectively. The defaults are:
Daily: home pub
Weekly: bin boot etc lib lib64 opt root run sbin snap usr var
Monthly: media mnt

So, essentially the daily scan checks places I put things regularly, weekly is the whole system and monthly is my backup drive and any other mounted filesystems.

A good place to store my scripts is in the bin subfolder of your home folder ($HOME/bin) just make sure it's in your PATH

As with all my scripts, I advise you to read through it carefully and understand what it does, changing any settings to suit your setup before you run it.
