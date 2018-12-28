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
