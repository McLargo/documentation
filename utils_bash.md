#### zip - compress command
`zip -r /path/blabla.zip mydir/*`

### list volumns
`lsblk`

### unmount USB
`udisksctl unmount -b /dev/$VOLUMENAME`

### delete type extension
`find . -name "*.pyc" -type f -delete`

### find type extension
`find . -name "*.pyc" -type f`

### redirect output to file
`cat scripts/dump/*.sql  > scripts/db/name.sql`

### rsync
`rsync -avzh --include '*.csv' --include '*.log' --exclude '*' user@ip:/or_path/ destination_path/`

### ag - search command (with/without extension)
`ag something`
`ag something --py`

##### search ignoring extension/Pattern
`ag columns_authentication_user --ignore "*.py"`

### how to dump a mysql database
`mysqldump {database} -u{user} -p{password} > ~/.mysqldumps/{filename}.sql`

### aws sync, using aws or s3cmd

`aws s3 sync /local_path s3://bucket_name/ --dryrun --exclude="filesOrFolders"`

`s3cmd sync --dry-run --exclude-from='/exclude_files' --delete-removed /local_path s3://bucket_name/`


#### check number of parameters
```
if [ "$#" -ne 2 ]; then
    echo "[ERROR] Illegal number of parameters. Aborting..."
    exit 1
fi
```

#### check variable is integer
```
function check_version_is_integer(){
    re='^[0-9]+$'
    if ! [[ $version =~ $re ]] ; then
        echo "[ERROR] Version is not a number. Aborting..."
       exit 1
    fi
}
```

#### load in .zshrc or .bashsrc
```
if [ -f ~/.bash_aliases ]; then
    . ~/.bash_aliases
fi
```

#### for samples below, server_list is a file with content
`server-1 server-2 server-3 server-4 server-5 server-6`

#### copy public key to server list
```
#!/bin/bashg
for ip in `cat servers_list`; do
    ssh-copy-id -i ~/.ssh/id_rsa.pub $ip
done
```

#### do scp of folder to server list
```
for server in $(cat servers_list)
do
  scp folder/* "$server":/path/dest_folder
done
```