## Week 16 Homework Submission File: Penetration Testing 1

#### Step 1: Google Dorking


- Using Google, can you identify who the Chief Executive Officer of Altoro Mutual is:
  
  
      Karl Fitzgerald 

- How can this information be helpful to an attacker:
      
      
      The attacker can target their victim by phishing and social engineering 

#### Step 2: DNS and Domain Discovery

Enter the IP address for `demo.testfire.net` into Domain Dossier and answer the following questions based on the results:

  1. Where is the company located: 
   
    Sunnyvale, CA 

  2. What is the NetRange IP address: 
     
     
    65.61.137.64 - 65.61.137.127

  3. What is the company they use to store their infrastructure: 
  
  
    Rackspace Backbone Engineering 

  4. What is the IP address of the DNS server: 
  
    65.61.137.117

#### Step 3: Shodan

- What open ports and running services did Shodan find: 

      The open ports are 80, 443, and 8080. 
 ![Week_16_part_1](https://user-images.githubusercontent.com/77870466/124793955-82b65d80-df1c-11eb-9c64-05294fed00a3.jpg)


#### Step 4: Recon-ng

- Install the Recon module `xssed`. 
- Set the source to `demo.testfire.net`. 
- Run the module. 

Is Altoro Mutual vulnerable to XSS: 
            
        Yes, this is the only vulnerability that is found

![Week_16_part_2](https://user-images.githubusercontent.com/77870466/124801669-1855eb00-df25-11eb-9247-5ec4ddb9dda8.jpg)

        This is when I use results.html which shows only one vulnerability. 
![Week_16_part_3](https://user-images.githubusercontent.com/77870466/124803849-9dda9a80-df27-11eb-8b61-b2add637b04e.jpg)



### Step 5: Zenmap

Your client has asked that you help identify any vulnerabilities with their file-sharing server. Using the Metasploitable machine to act as your client's server, complete the following:

- Command for Zenmap to run a service scan against the Metasploitable machine: nmap -sV 192.168.0.10
 
- Bonus command to output results into a new text file named `zenmapscan.txt`: nmap -sV -oN zenmapscan.txt 192.168.0.10

- Zenmap vulnerability script command: nmap --script ftp-vsftpd-backdoor, smb-enum-shares 192.168.0.10

- Once you have identified this vulnerability, answer the following questions for your client:
  1. What is the vulnerability: 
          
          The vulnerabilities in in smb which allows unauthorized access. 
          
![Week_16_part_4](https://user-images.githubusercontent.com/77870466/124809891-a5517200-df2e-11eb-9323-0d55e688514f.jpg)
![Week_16_part_5](https://user-images.githubusercontent.com/77870466/124809893-a5517200-df2e-11eb-8f22-d9da9c080014.jpg)
![Week_16_part-6](https://user-images.githubusercontent.com/77870466/124809894-a5ea0880-df2e-11eb-8294-dfb0ccbb9cb1.jpg)

  2. Why is it dangerous: 
          
           SMB allows for exfiltration of data and also allow their payloafs to spread through connected systems. 

  3. What mitigation strategies can you recommendations for the client to protect their server: 
          
          The client just have to update/patch the SMB. 

---
© 2020 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.
