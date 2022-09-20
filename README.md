# whm-Proxy-Script

######### Issue ###############

I am getting en error in Apache since long time. And the issue is that after some time,
reverse proxy rules removed from Apache virtual host automatically.

########## Cpanel_Reply ##############

The most common reason that a configuration setting would get removed from WHM/Cpanel when rebuilding the httpd.conf file is because the modification was done directly to the configuration file. When cPanel rebuilds the apache conf, it does so using template files and any configuration not in those templates are not included.

################ Solution_cPanel Apache Reverse Proxy ##################

Step 1. Download The Proxy Script

wget https://raw.githubusercontent.com/varunsridharan/cpanel-apache-proxy/main/proxy.sh

Step 2. Run To Create A New Proxy

sh proxy.sh "cpanelAccountName" "blog.example.com" "http://192.168.1.41:32000"

Step 3. Rebuild & Restart HTTP /scripts/rebuildhttpdconf && service httpd restart
 
