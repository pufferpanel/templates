Lets you create a 7 Days to Die Server with Console
Requirements:
Ubuntu/Debian (x86-64): lib32gcc1 telnet
RedHat/CentOS (x86-64): glibc.i686 libstdc++.i686 telnet

Dont touch the kill button this will messup the console and the server keeps running
if you really have to kill it use "pgrap -av 7DaysToDieServer" and "kill -9 $PID"
output of the Startserver.sh is located in nohup.out

Edit those lines in serverconfig.xml

property name="TelnetEnabled"					value="true"

property name="TelnetPort"						value="8081"

property name="TelnetPassword"					value="CHANGEmeTOaSTRONGpassword"

property name="TelnetFailedLoginLimit"			value="10"

property name="TelnetFailedLoginsBlocktime"	value="120"
