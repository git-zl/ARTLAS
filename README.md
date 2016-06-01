<h1>ARTLAS Apache Real Time Logs Analyzer System</h1>

<p>
Real time  Apache log analyzer, based on top 10 OWASP vulnerabilities, identifies attempts of exploration in your web application, and notify you or your incident team on Telegram.
</p>
<p>
ARTLAS uses the regular expression from the PHP-IDS project, to identify the attempts of exploration, download link to the latest version of the file
https://dev.itratos.de/projects/php-ids/repository/raw/trunk/lib/IDS/default_filter.json
</p>
<h3>Installation</h3>
<pre>
<b>Clone project</b>
git clone https://github.com/mthbernardes/ARTLAS.git

<b>Install dependencies</b>
pip install -r dependencies.txt
python version 2.7.11(lastet)
</pre>

<h3>Configuration</h3>
<pre>All your configurations will be made in <b>etc/artlas.conf</b> file.

<b>TELEGRAM INTEGRATION</b>
<i>[Telegram]
api = Your Token API
group_id = Group/User ID that will receive the notifications
enable = True to send notificantions or False to not send.</i>

<b><font color="red">**ZABBIX INTEGRATION NOT WORKING YET**</font></b>
<i>[Zabbix]
username = Zabbix Username
password = Zabbix Password
server = http://127.0.0.1/ - Zabbix Server
enable = True to enable  or False to disable

<b>GENERAL CONFIGURATION</b>
[Files]
apache_log = Full path apache access.log
rules = default_filter.json It's the file that contains the OWASP filter <b><i>[Do not Change]</i></b>
</pre>

<h3>Telegram Notification example</h3>

<img src="https://raw.githubusercontent.com/mthbernardes/ARTLAS/master/img/notification.png" width="350"/>
