## How linux file/directory permissions work?
To understand this better, lets start creating the user/groups.
```
for i in abc1 abc2 abc3
do
	useradd $i
	# OR adduser $i
done

groupadd acl
```

## How default file/directory permissions are calculated?
```
chetan@99devops:/run$ umask
0002
```
## What does *chmod* does?
This command sets the file/directory permission as given. Use *-R* switch for *recursive* subdirectories.
```
chmod 777 file.txt
```

## What does *chown* does?
This sets the owner of the file/directory.
```
chown -R chetan.chetan  file.txt
```

## What does *setfacl* does?
Below command adds *rwx* permission to user *chetan*.
```
setfacl -m u:chetan:rwx file.txt
```

## What does *usermod* does?
This command adds a user to the existing group.  
```
usermod -G groupname username
```
