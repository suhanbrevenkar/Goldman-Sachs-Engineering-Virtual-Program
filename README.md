# Goldman-Sachs-Crack-Leaked-Passsword-Database
Virtual Internship by Goldman Sachs to Analyze and report uplifts to controls and policies.

# Overview
  As a governance analyst it is part of your duties to assess the level of protection offered by implemented controls and minimize the probability of a successful breach. You often need to know the techniques used by hackers to circumvent implemented controls and propose uplifts to increase the overall level of security in an organization. Gaining valid credentials gives the attackers access to the organization’s IT system, thus circumventing most of perimeter controls in place.
  
# Project Objective
    • What type of hashing algorithm was used to protect passwords?
    • What level of protection does the mechanism offer for passwords?
    • What controls could be implemented to make cracking much harder for the hacker in the event of a password database leaking again?
    • What can you tell about the organization’s password policy (e.g. password length, key space, etc.)?
    • What would you change in the password policy to make breaking the passwords harder? 

The passwd_dump.txt file contains the leaked hash of passwords


# Observations
    Observations :
    HASH                                              -  HASH ALGORITHM
    experthead:e10adc3949ba59abbe56e057f20f883e       -  MD5
    interestec:25f9e794323b453885f5181f1b624d0b       -  MD5
    ortspoon:d8578edf8458ce06fbc5bb76a58c5ca4         -  MD5
    reallychel:5f4dcc3b5aa765d61d8327deb882cf99       -  MD5
    simmson56:96e79218965eb72c92a549dd5a330112        -  MD5
    bookma:25d55ad283aa400af464c76d713c07ad           -  MD5
    popularkiya7:e99a18c428cb38d5f260853678922e03     -  MD5
    eatingcake1994:fcea920f7412b5da7be0cf42b8c93759   -  MD5
    heroanhart:7c6a180b36896a0a8c02787eeafb0e4c       -  MD5
    edi_tesla89:6c569aabbf7775ef8fc570e228c16b98      -  MD5
    liveltekah:3f230640b78d7e71ac5514e57935eb69       -  MD5
    blikimore:917eb5e9d6d6bca820922a0c6f7cc28b        -  MD5
    johnwick007:f6a0cb102c62879d397b12b62c092c06      -  MD5
    flamesbria2001:9b3b269ad0a208090309f091b3aba9db   -  MD5
    oranolio:16ced47d3fc931483e24933665cded6d         -  MD5
    spuffyffet:1f5c5683982d7c3814d4d9e6d749b21e       -  MD5
    moodie:8d763385e0476ae208f21bc63956f748           -  MD5
    nabox:defebde7b6ab6f24d5824682a16c3ae4            -  MD5
    bandalls:bdda5f03128bcbdfa78d8934529048cf         -  MD5
Use tools to identify the type of Hash Algorithm used

# Procedure Followed
   Carried out password cracking using Hashcat and various wordlist like rockyou.txt and many more.
   Password cracking is usually time consuming if one doesn't have GPU in such case, one can use Google Colab but be sure that you don't violate their policy
   
# Result
    HASH                                              -  CRACKED HASH
    experthead:e10adc3949ba59abbe56e057f20f883e		    -  123456
    interestec:25f9e794323b453885f5181f1b624d0b		    -  123456789
    ortspoon:d8578edf8458ce06fbc5bb76a58c5ca4 		    -  qwerty
    reallychel:5f4dcc3b5aa765d61d8327deb882cf99		    -  password
    simmson56:96e79218965eb72c92a549dd5a330112		    -  111111
    bookma:25d55ad283aa400af464c76d713c07ad		        -  12345678
    popularkiya7:e99a18c428cb38d5f260853678922e03	    -  abc123
    eatingcake1994:fcea920f7412b5da7be0cf42b8c93759	  -  1234567
    heroanhart:7c6a180b36896a0a8c02787eeafb0e4c		    -  password1
    edi_tesla89:6c569aabbf7775ef8fc570e228c16b98	    -  password!
    liveltekah:3f230640b78d7e71ac5514e57935eb69		    -  qazxsw
    blikimore:917eb5e9d6d6bca820922a0c6f7cc28b		    -  Pa$$word1
    johnwick007:f6a0cb102c62879d397b12b62c092c06	    -  bluered
    flamesbria2001:9b3b269ad0a208090309f091b3aba9db	  -  Flamesbria2001
    oranolio:16ced47d3fc931483e24933665cded6d 		    -  Oranolio1994
    spuffyffet:1f5c5683982d7c3814d4d9e6d749b21e 	    -  Spuffyffet12
    moodie:8d763385e0476ae208f21bc63956f748 		      -  moodie00
    nabox:defebde7b6ab6f24d5824682a16c3ae4  		      -  nAbox!1
    bandalls:bdda5f03128bcbdfa78d8934529048cf      	  -  Banda11s
    
# Findings
   • a careful look over the recovered passwords we find users are reusing their username as part of the password which is very risky and a cake-walk to crack
   • No strict password ppolicy implemented.
   • MD5 hash algorithm which is not that strong is used. SHA256/SHA512 is recommended.
   • Salting.
   • Avoid common words and common passwords
   • Longer the passwords, the better they are.
   • Don’t allow reusing of passwords.
   • Mandate use of combinations of special character, Capital and Small letters, numbers in your password.
   • Don’t let users include their personal information like username, actual name, date of birth and others while creating a password.
   • Mandate MFA (Multi-Factor Auth) so that it can prevent account compromise in situations of password breaches.
