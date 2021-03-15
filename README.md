# CERN Computing Account
> How to request a computing account for a new student.

1. Go to `https://cms.cern.ch/iCMS/jsp/secr/reg/regCMS.jsp` and fill the form.

- **Email:** any email you're mostly using: hotmail, gmail etc. you'll contact with the CMS secretariat from this email address. 
- **Name:** Your family name (surname)
- **First Name:** your name
- **Institute:** Cukurova University
- **Institute Representative:** Isa Dumanoglu
- **Activity:** (Should be **CMS User**, not sure)


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



# How to connect to your lxplus area

**Step-1:** Login to your lxplus area:

***For Windows:***
**Download & install:**
- **Putty (putty-64bit-0.74-installer.msi) or newer version:** https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html
- **Xming:** https://sourceforge.net/projects/xming/
- **Winscp:** https://winscp.net/eng/download.php

## Putty Settings

![Putty Settings](https://raw.githubusercontent.com/asimsek/CERNComputingAccount/main/putty.png "Putty Settings")

> ps. lxplus6 is an old version and lxplus.cern.ch will direct you to latest version. (picture is old)

**Host name:** username@lxplus.cern.ch

**Port:** 22

**Connection Type:** SSH

**Saved Sessions:** lxplus


- Save the settings.
- Go to: Connections >> SSH >> X11
- Enable X11 forwarding
- X display location: localhost:0.0

go back to **Session** tab on left side (first category), and save the session again (to save the ssh settings to your profile). Now you can double click on it or click to load while its selected.

This will open a terminal window and use your new cern account password. (you'll not see any character while you typing your password. Hold the backspace for a while if you type your password wrong). It's same with you email. (Btw, to see your e-mails: https://mmm.cern.ch/owa/). Now you're able to use your lxplus account. (list your folders with **ls -lhtr** when you login and use private folder for your analysis. **cd private**)

> ps. open xming and you should see the icon on right bottom:

![Xming](https://raw.githubusercontent.com/asimsek/CERNComputingAccount/main/xming_exit.png "Xming")



------------


***For Mac & Linux:***

- Download & Install: XQuartz -- https://www.xquartz.org/
- Open a new terminal window
- type `ssh -Y username@lxplus.cern.ch` and hit enter
- type your new cern account password and hit enter. (you'll not see any character while you typing your password. Hold the backspace for a while if you type your password wrong).
- Now you're able to use your lxplus account. (list your folders with **ls -lhtr** when you login and use private folder for your analysis. **cd private**)


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



------------

------------

------------



# CERN Data Analysis 

Log-in to your lxplus account and go to your `private` folder.

```bash
cd private
mkdir CMSDataAnalyzerStudy
cd CMSDataAnalyzerStudy
echo $0
```

`echo $0`command will show your shell type. Use one of the following command lines appropriate for your shell type.


```bash
# for Bash User
source /cvmfs/cms.cern.ch/cmsset_default.sh

# for csh user
source /cvmfs/cms.cern.ch/cmsset_default.csh
```

Create a new CMSSW version.
```bash
cmsrel CMSSW_10_2_5_patch1
```


You'll see a warning as following:

> WARNING: Release CMSSW_10_2_5_patch1 is not available for architecture slc7_amd64_gcc820.

> Developer's area is created for available architecture **slc7_amd64_gcc700**.


This means, you need to change your architecture with the following command line.


```bash
export SCRAM_ARCH=slc7_amd64_gcc700
cd CMSSW_10_2_5_patch1/src
cmsenv
mkdir DataAnalyzer
cd DataAnalyzer
```

> ps: **cmsenv** command is crutial for usage of all cms functions. Don't forget to use it before using the cms commands ( root, cmsRun, edmProvDump, edmDumpEventContent, etc. )

Create a new EDAnalyzer:
```bash
mkedanlzr DemoAnalyzer
cd DemoAnalyzer
scram b -j 4
```


Now we need to change & add some code lines into `plugins/DemoAnalyzer.cc`

```bash
vi plugins/DemoAnalyzer.cc
```

```cpp
#find
using reco::TrackCollection;

#replace
using namespace std;
using namespace edm;
using namespace reco;
using namespace trigger;
using namespace l1t;
```

```cpp
#find
// ----------member data ---------------------------
edm::EDGetTokenT<TrackCollection> tracksToken_;  //used to select what tracks to read from configuration file

#replace
// ----------member data ---------------------------
EDGetTokenT<HBHERecHitCollection> hbherechit_;
```

```cpp
#find & Delete (with : sign)
:
tracksToken_(consumes<TrackCollection>(iConfig.getUntrackedParameter<edm::InputTag>("tracks")))
```

```cpp

```

```cpp
#find
//now do what ever initialization is needed

#replace
//now do what ever initialization is needed
hbherechit_ = consumes<HBHERecHitCollection>(iConfig.getParameter<edm::InputTag>("HBHERecHitCollection"));
```


```cpp
#find
   Handle<HBHERecHitCollection> hbhehits_;
   iEvent.getByToken(hbherechit_, hbhehits_);

#replace
   Handle<HBHERecHitCollection> hbhehits_;
   iEvent.getByToken(hbherechit_, hbhehits_);
```

```cpp
#find
    Handle<TrackCollection> tracks;
    iEvent.getByToken(tracksToken_, tracks);
    for(TrackCollection::const_iterator itTrack = tracks->begin();
        itTrack != tracks->end();
        ++itTrack) {
      // do something with track parameters, e.g, plot the charge.
      // int charge = itTrack->charge();
    }

#replace
	const HBHERecHitCollection* hbhe_hits = hbhehits_.failedToGet () ? 0 : &*hbhehits_;
	if (hbhehits_.isValid()) {
		for (HBHERecHitCollection::const_iterator j=hbhe_hits->begin(); j!=hbhe_hits->end(); j++) {
			// This for loop is looping in each event!


		}
	}
```


------------

------------



For more, please follow this twiki page:
https://twiki.cern.ch/twiki/bin/view/CMSPublic/WorkBookWriteFrameworkModule?LOCALSHELL=bash
