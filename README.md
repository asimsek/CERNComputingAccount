# CERN Computing Account
> How to request a computing account for a new student.

1. Go to `https://cms.cern.ch/iCMS/jsp/secr/reg/regCMS.jsp` and fill the form.

- **Email:** any email you're mostly using: hotmail, gmail etc. you'll contact with the CMS secretariat from this email address. 
- **Name:** Your family name (surname)
- **First Name:** your name
- **Institute:** Cukurova University
- **Institute Representative:** (should be İsa Dumanoglu but i'm not sure)
- **Activity:** (Should be **User** or **CMS**, not sure)


2. Click on `Ask CMS secretariat` button.

> After the form, you'll receive an email with your **HRPersonID** as:

    Dear XX YY (ADANA-CUKUROVA),
    You are now registered in CMS as 'Non-Doctoral Student' from your institute (ADANA-CUKUROVA) .

You will use the **HRPersonID** number in the next mail.
When you receive the mail above, send an email to `cms.people@cern.ch` as below.


***Mail Subject : CERN Account***
> Dear Sir / Madame,
>
>	I'm now registered in CMS as 'Non-Doctoral Student' from my institute (ADANA-CUKUROVA). Could you provide my "Username" and "Initial Password", please.
>
>	Thank You.
>
> Surname, Name
> 
> HRpersonId:

***For Step-1:***
They will ask you to upload a copy of your ID (english) or passport to the system.

***For Step-2:***
Also they'll ask you to fill another form that your team leader (Isa Dumanoglu for CU) will approve your account.


After these steps, they should send you your username. Probably they'll **not** send your initial password. You'll get an email as:

> Welcome to CERN. Your Primary Account was automatically created.
> 
> Name: XXX YYY
> 
> Login: xxxxx
> 
> Email: your initial email address (hotmail, gmail etc.)

------------



## If they won't send you an initial password:
For the initial password, you should send another email to `service-desk@cern.ch` as:

***Mail Subject: CMS Account Activation & Initial Password***

> Dear CERN People,
>
> My account "xxxxx" is now added to the CMS (zh) group, however it's currently disabled. Could you activate my account and send my initial password, please?
>
> Thank you.
>
> Best regards,
>
> Surname, Name
>
> HRpersonId :



They'll activate your account and send you an email including your initial password. Please follow the required actions section in your mail and change your account and EDH passwords in 3 days.


ps. these steps can be changed partly but more or less the process is the same.



For more information: https://twiki.cern.ch/twiki/bin/view/CMSPublic/WorkBookGetAccount


------------
------------
------------



# How to start data analysis

**Step-1:** Login to your lxplus area:

***For Windows:***
**Download & install:**
- **Putty (putty-64bit-0.74-installer.msi) or newer version:** https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html
- **Xming:** https://sourceforge.net/projects/xming/
- **Winscp:** https://winscp.net/eng/download.php



------------


**Basic Linux commands:**

- **ls** -- lists your files
- **ls -lhtr** -- list your files (newer at bottom)
- **mv filename1 filename2** -- moves a file (i.e. gives it a different name, or moves it into a different directory.
- **cp filename1 filename2** -- copies a file
- **rm filename** -- removes a file. It is wise to use the option **rm -i**, which will ask you for confirmation before actually deleting anything.
- **diff filename1 filename2** -- compares files, and shows where they differ
- **chmod options filename** -- lets you change the read, write, and execute permissions on your files. For example, **chmod o+r filename** will make the file readable for everyone, and **chmod o-r filename** will make it unreadable for others again.
- **mkdir dirname** -- make a new directory
- **cd dirname** -- change directory. You basically 'go' to another directory, and you will see the files in that directory when you do 'ls'.
- **cd** -- without arguments, will let you to go home directory.
- **cd ..** -- this command will get you one level up from your current position.
- **pwd** -- tells you where you currently are.
- **vi filename.xxx** -- vi is a text editor for your scripts. when you open the editor you can activate insert mode with pressing **i** on your keyboard and you can press **esc** to deactivate. You can see the current mode on left-bottom side. To save the file you can press **esc** first, they type **:w** and hit to **enter**. To quit from vi editor press **esc** first, type **:q** and hit **enter**. If you want to quit without saving your changes, press **esc** first, type **:q!** and hit **enter**. If you would like to save & exit, press **esc** first, type **:wq** hit **enter**.









For more: http://mally.stanford.edu/~sr/computing/basic-unix.html


https://twiki.cern.ch/twiki/bin/view/CMSPublic/WorkBookWriteFrameworkModule?LOCALSHELL=bash
