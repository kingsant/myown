https://my.oschina.net/u/3247574/blog/1475190

*/1 * * * * /hello.sh

#!/bin/sh  

TomcatID=$(ps -ef|grep crond| grep -v grep |awk '{print $2}')
StartTomcat=/startTom.sh
TomcatMonitorLog=/TomcatMonitor.log
Monitor()  
{
  echo "[info]start monitor tomcat...[$(date +'%F %H:%M:%S')]"  
  if [[ $TomcatID ]];then
    echo "[info]current tomcat pid ID is:$TomcatID,go on check page..."  
  else
    echo "[error]tomcat process in not exist! tomcat auto restart..."  
    echo "[info]$StartTomcat,please in wait......"  
    $StartTomcat
  fi
  echo "------------------------------"  
}
Monitor>>$TomcatMonitorLog

