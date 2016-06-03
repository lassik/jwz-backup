# jwz-backup #

## What's this? ##

This is a script to backup your computer to an external hard drive.

It's basically <https://www.jwz.org/doc/backups.html> with a little
convenience:

* Checks that your backup drive is mounted properly. (I disconnect mine during
  the day.)
* Collects error and warning messages from rsync and shows them all at once
  when the backup is done. (These tend to be harmless messages about browser
  cache files vanishing mid-backup, but it's nice to see them for peace of
  mind.)
* Keeps stats of how long your backups take.
* Runs at minimum priority in case you want to browse the web or watch a movie
  while it's backing up.

## OS support ##

Mac only.

Porting to Linux and BSD should be easy. PRs welcome.

## Environment variables ##

`BACKUP_MOUNT` -- Directory where your backup disk is mounted. No slash at the
end! The default is `/Volumes/Backup`.

`BACKUP_LOGDIR` -- Directory where logs will be written. The default is
`~/.backup`.
