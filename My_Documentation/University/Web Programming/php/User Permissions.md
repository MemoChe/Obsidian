So that in our web page it can have permissions it is necessary to offer to the user http of group http permissions of writing and reading. However we can make it easier and change the user and group of the configuration (/etc/httpd/conf/httpd.conf) of apache to our main user of linux that is to say memo of group memo to not have problems at the time of modifying and uploading file to /home, however if it is necessary to put permissions to enter to root.

sudo chown -R memo:otrogrupo /home/memo/Documents
sudo chown -R memo:memo /home/memo/Documents



