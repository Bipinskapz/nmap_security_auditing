
# OFFICIAL WEBSITE FOR THE BOOK

	[https://nmap-cookbook.com]


# NMAP FROM SOURCE

   1. apt-get install svn
   2. svn co --username guest https://svn.nmap.org/nmap/

  
##	Requirements

	* gcc
	* openssl
	* make
   3. cd to <nmap_folder>
   4. ./configure
   5. make or make install

                             NOTE:
			     -------------
				- Skip the installation of Ndiff by using 	--without-ndiff
				- Skip the installation of Zenmap by using 	--without-zenmap
				- Skip the installation of Nping by using 	--without-nping 

NMAP P R E  C O M P I L E D  P A C K A G E S
---------------------------------------------------

	[http://nmap.org/download.html]



###     Helper Website
     =======================================

	[http://nmap.org/book/man-port-scanning-techniques.html]


				     ****Working of Nmap SERVICE DETECTION****
				-------------------------------------------------- 

					 [http://nmap.org/book/vscan.html]

		* Aggressive Scan

		        +++++++++++++++++++++++++
                         nmap -sA <host_name>                    ** Gives more info but more detectable by the target **
			+++++++++++++++++++++++++
	
				
	
----------------------------------------------------
Aggressive Mode
======================
           - OS detection ( -O ), 
	     - Version detection ( -sV ), 
	     - Script scanning ( -sC ), and 
	     - Traceroute ( --traceroute )
-----------------------------------------------------

		Note:

       			[http://insecure.org/cgi-bin/submit.cgi?]          
			
				** Submissions for correction(to nmap database)





        P O R T    S C A N N I N G   M E T H O D S
	-------------------------------------------------------

	1. Port list:
	   ```console
		foo@bar:~$ nmap -p80,443 localhost
	` ``
		

	2. Port range:

		nmap -p1-100 localhost

	3. All ports:
 
		nmap -p- localhost

	4. Specific ports by protocols:

		nmap -pT:25,U:53 <target>

	5. Service name:

		nmap -p smtp <target>

	6. Service name wildcards:

		nmap -p smtp* <target>

	7. Only ports registered in Nmap services:

		nmap -p[1-65535] <target>


         D I F E R E N T    M E T H O D S   F O R   R U N N I N G    NSE   S C R I P T S
	---------------------------------------------------------------------------------------------

	  1. Run all the scripts in the vuln category:
		
		nmap -sV --script vuln <target>

	  2. Run the scripts in the categories version or discovery :

		nmap -sV --script="version,discovery" <target>

	  3. Run all the scripts except for the ones in the exploit category:

		nmap -sV --script "not exploit" <target>

	  4. Run all HTTP scripts except http-brute and http-slowloris :

		nmap -sV --script "(http-*) and not(http-slowloris or http-brute)" <target>


          NSE  S C R I P T   C A T E G O R I E S
	 ----------------------------------------------------

	  1. auth : This category is for scripts related to user authentication.

	  2. broadcast : This is a very interesting category of scripts that use broadcast petitions to gather information.

	  3. brute : This category is for scripts that help conduct brute-force password auditing.

	  4. default : This category is for scripts that are executed when a script scan is executed ( -sC ).

	  5. discovery : This category is for scripts related to host and service discovery.

	  6. dos : This category is for scripts related to denial of service attacks.

	  7. exploit : This category is for scripts that exploit security vulnerabilities.

	  8. external : This category is for scripts that depend on a third-party service.

	  9. fuzzer : This category is for NSE scripts that are focused on fuzzing.

	 10. intrusive : This category is for scripts that might crash something or generate a lot of network noise. Scripts that system administrators may consider intrusive belong to this category.

	 11. malware : This category is for scripts related to malware detection.

	 12. safe : This category is for scripts that are considered safe in all situations.

	 13. version : This category is for scripts that are used for advanced versioning.

	 14. vuln : This category is for scripts related to security vulnerabilities.	





 



















