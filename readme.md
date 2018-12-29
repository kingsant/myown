山有木兮木有枝，心悦君兮君不知.
#!/usr/bin/bash
dir | grep test
echo "file:" "$@"
PATH=$@

ls
echo "file2ss:" "$@"
echo $PATH
cd $PATH
pwd




ls -a 

#!/usr/bin/bash
bash start.sh myown 2>&1| tee  tlog.txt 
ls

#!/bin/bash
#print the directory and file
 
for file in /d/Code/*
do
if [ -d "$file" ]
then 
  echo "$file is directory"
elif [ -f "$file" ]
then
  echo "$file is file"
fi
done
