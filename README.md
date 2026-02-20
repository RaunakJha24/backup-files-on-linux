# Back Up Tools on Linux

It can be a herculean task if you have a large number of files and you want to back them up once a year. To avoid such scenarios, there are commands that can aid you in back up of your files  on Linux, In the following paragraphs, we will look at some of the popular commands that make the backup process easier. 

## rsync

It is one of the most popular commands that makes the backup process easier. It has the benefit of copying only the changes of a file. So, it is highly appropriate for those who prefer incremental backups.

Command for full backup:

```
rsync -av --delete /home/user/ /backup/
```

Here, source folder is ``/home/dircetory/`` and destination folder is ``/backup/``.

Command for incremental backup:

```
rsync -av --link-dest=/backup/last_full /home/user/ /backup/incremental/
```

## tar

It is another command that allows the vantage of saving backups in compressed format. 

Command for backup using ``tar``:

```
tar -czvf backup.tar.gz /home/user/
```

## Deja Dup Backups

The final backup option is Deja Dup Backups. It is specifically for those, who are uncomfortable with terminal. It can be used to backup files on a schedule and also, with option for encryption. You can find it in app store of your distribution and install it.

