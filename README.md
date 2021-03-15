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


#### Basic Linux commands:

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
>
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


Now we need to change & add some code lines into `plugins/DemoAnalyzer.cc` . For the usage of `vi` editor, see [basic linux commands](https://github.com/asimsek/CERNComputingAccount/blob/main/README.md#basic-linux-commands "basic linux commands") section above.

> ps: This tutorial & general CMS data analysis needs basic c++ and python knowledge. Also, you should be familiarized with the linux commands.

```bash
vi plugins/DemoAnalyzer.cc
```


**We're defining the header files:**
```cpp
#find
//
// class declaration
//

#replace
//
// class declaration
//
#include "DataFormats/HcalDetId/interface/HcalDetId.h"
#include "DataFormats/HcalRecHit/interface/HcalRecHitCollections.h"
#include "DataFormats/HcalDigi/interface/HBHEDataFrame.h"
#include "DataFormats/HcalRecHit/interface/HBHERecHit.h"
#include "DataFormats/HcalDetId/interface/HcalSubdetector.h"
#include "Geometry/CaloGeometry/interface/CaloSubdetectorGeometry.h"
#include "Geometry/CaloGeometry/interface/CaloCellGeometry.h"
```

**Define the namespaces:**
```cpp
#find
using reco::TrackCollection;

#replace
using namespace std;
using namespace edm;
using namespace reco;
```

**Replace the token to analyze HCal-Barrel & HCal-EndCap:**
```cpp
#find
// ----------member data ---------------------------
edm::EDGetTokenT<TrackCollection> tracksToken_;  //used to select what tracks to read from configuration file

#replace
// ----------member data ---------------------------
EDGetTokenT<HBHERecHitCollection> hbherechit_;
```

**Delete unnecessary part:**
```cpp
#find & Delete (with : sign)
:
tracksToken_(consumes<TrackCollection>(iConfig.getUntrackedParameter<edm::InputTag>("tracks")))
```

**Initialize the HBHE collection:**
```cpp
#find
//now do what ever initialization is needed

#replace
//now do what ever initialization is needed
hbherechit_ = consumes<HBHERecHitCollection>(iConfig.getParameter<edm::InputTag>("HBHERecHitCollection"));
```

**Get the data from root file by token:**
```cpp
#find
   Handle<HBHERecHitCollection> hbhehits_;
   iEvent.getByToken(hbherechit_, hbhehits_);

#replace
   Handle<HBHERecHitCollection> hbhehits_;
   iEvent.getByToken(hbherechit_, hbhehits_);
```

**Replace the track loop with HBHE loop:**
```cpp
#find
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
			HcalDetId id = (*j).id();
			int ieta= id.ieta();
			float energy = (*j).energy();
			cout << "ieta: " << ieta << "  --  Energy:" << energy << endl;
		}
	}
```

Now, you can press `esc`to deactivate insert mode in `vi` editor and save&quit with typing `:wq`. (for more information see: [basic linux commands](https://github.com/asimsek/CERNComputingAccount/blob/main/README.md#basic-linux-commands "basic linux commands"))

------------
**Before the config file, we need to create another file which is necessary:**
```bash
vi python/CfiFile_cfi.py
```

Activate the `vi` editor with pressing `i` on your keyboard and paste the following command lines:

```python
import FWCore.ParameterSet.Config as cms

demo = cms.EDAnalyzer('DemoAnalyzer'
)
```

press `esc` and type `:wq` to save&exit. (For more vi commands, please see: [basic linux commands](https://github.com/asimsek/CERNComputingAccount/blob/main/README.md#basic-linux-commands "basic linux commands"))


------------

We need to create a config file in python folder and add some code lines into `ConfFile_cfg.py` file.
```bash
vi python/ConfFile_cfg.py
```

**Activate the insert mode and add the following commands**
```python
import FWCore.ParameterSet.Config as cms
import datetime
import PhysicsTools.PythonAnalysis.LumiList as LumiList
from FWCore.ParameterSet.VarParsing import VarParsing

options = VarParsing ('python')


options.register('reportEvery', 1,
    VarParsing.multiplicity.singleton,
    VarParsing.varType.int,
    "Report every N events (default is N=1000)"
)

options.register('process', '146908',
    VarParsing.multiplicity.singleton,
    VarParsing.varType.string,
    "MC-simulated event type"
)

options.register('wantSummary', False,
    VarParsing.multiplicity.singleton,
    VarParsing.varType.bool,
    "Print out trigger and timing summary"
)

options.parseArguments()


process = cms.Process("Test")


process.load('Configuration.StandardSequences.Services_cff')
process.load('SimGeneral.HepPDTESSource.pythiapdt_cfi')
process.load('FWCore.MessageService.MessageLogger_cfi')
process.load('Configuration.StandardSequences.GeometryRecoDB_cff')
process.load('Configuration.StandardSequences.MagneticField_AutoFromDBCurrent_cff')
process.load('CommonTools.RecoAlgos.HBHENoiseFilterResultProducer_cfi')
process.load("RecoJets.Configuration.CaloTowersES_cfi")
process.load("Configuration.StandardSequences.RawToDigi_Data_cff")
process.load("RecoLocalCalo.Configuration.hcalLocalReco_cff")

# report every #1 hit! You can change it to any number you like.
process.MessageLogger.cerr.FwkReport.reportEvery = 1

# How many event you want to analyze. To analyze all events change 1000 with -1
process.maxEvents = cms.untracked.PSet( input = cms.untracked.int32(1000) )

process.source = cms.Source("PoolSource",
    fileNames = cms.untracked.vstring(  *(
        # Add your root files here! (don't forget to add comma for the end of each line!)
        'file:/eos/cms/store/user/asimsek/Run2018E/023F1B34-4E2E-A343-8E2C-09C411E86530.root',
        #'file:/afs/cern.ch/cms/Tutorials/TWIKI_DATA/TTJets_8TeV_53X.root',
        )
    )
)

# Give any output name you like ( it's better to end with .root )
OutputFileNames = "Results2018.root"

process.TFileService = cms.Service("TFileService",
    fileName = cms.string(OutputFileNames)
)


process.options   = cms.untracked.PSet(
    wantSummary = cms.untracked.bool(options.wantSummary),
    allowUnscheduled = cms.untracked.bool(True),
    #SkipEvent = cms.untracked.vstring('ProductNotFound')
)


from Configuration.AlCa.autoCond import autoCond
process.load("Configuration.StandardSequences.FrontierConditions_GlobalTag_condDBv2_cff")
# You can change the global tag here but you need to find spesific global tag for each dataset, run number or root files.
process.GlobalTag.globaltag = '101X_dataRun2_Express_v8'



process.demo = cms.EDAnalyzer('DemoAnalyzer',
        HBHERecHitCollection = cms.InputTag("hbhereco"),
)


process.p = cms.Path(process.demo)
```


When you make any change in `plugins/DemoAnalyzer.cc` file, you need to re-compile the file:

```bash
cd $CMSSW_BASE/src/DataAnalyzer/DemoAnalyzer
cmsenv
scram b -j 4
```

Now you can run your scripts with `cmsRun` command.

```bash
cmsRun python/ConfFile_cfg.py
```


You should see some output including ieta and energy values of the #hits.
It's very hard to understand the detector with infinite number of entries. We're using histograms to understand the numbers and detector. Now let's plot these numbers in a histogram.

```bash
vi plugins/DemoAnalyzer.cc
```

**Define the header files:**
```cpp
#find
#include <map>

#replace
#include <map>
#include <string>
#include <fstream>
#include <iomanip>
#include <locale>
```

**And also:**
```cpp
#find:
#include "Geometry/CaloGeometry/interface/CaloCellGeometry.h"

#replace with:
#include "Geometry/CaloGeometry/interface/CaloCellGeometry.h"

#include "FWCore/ServiceRegistry/interface/Service.h"
#include "CommonTools/UtilAlgos/interface/TFileService.h"
#include "TH1.h"
#include "TH1D.h"
```




**We need to define histogram iteration to create histograms:**
```cpp
#find
// ----------member data ---------------------------

#replace
	// ----------member data ---------------------------
	map<string, TH1D*> histo1D;
	map<string, TH1D*>::iterator histo1Diter;
```


**We need to define histograms in beginJob() class:**
```cpp
#find
DemoAnalyzer::beginJob()
{
}

#replace
DemoAnalyzer::beginJob()
{
	cout<<"Begin Job"<<endl;
	edm::Service<TFileService> fs;

	histo1D["HEiEta"] = fs->make<TH1D>("HEiEta", "iEta vs Number Of Hits",60,-30,30);
	histo1D["HEiEta"]->GetXaxis()->SetTitle("i#eta");
	histo1D["HEiEta"]->GetYaxis()->SetTitle("Number of Hits");

	histo1D["HERecHitEnergy"] = fs->make<TH1D>( "HERecHitEnergy", "HE: Energy Distibution",300,0,300);
	histo1D["HERecHitEnergy"]->GetXaxis()->SetTitle("GeV");
	histo1D["HERecHitEnergy"]->GetYaxis()->SetTitle("Number of Hits");
}
```

**Let's comment the cout with adding `//` on the beginning of the line and add the commands for the filling histograms:**

```cpp
#find
		cout << "ieta: " << ieta << "  --  Energy:" << energy << endl;


#replace
		//cout << "ieta: " << ieta << "  --  Energy:" << energy << endl;

		 if(id.subdet() == HcalEndcap){
			histo1D["HEiEta"]->Fill(ieta);
			histo1D["HERecHitEnergy"]->Fill(energy);
		}
```


Save the file and quit with pressing `esc`and typing `:wq`.


**Now let's make necessary changes in `plugins/BuildFile.xml ` file:**

```bash
vi plugins/BuildFile.xml
```


```bash
#find
<use name="FWCore/Framework"/>
<use name="FWCore/PluginManager"/>
<use name="FWCore/ParameterSet"/>
<use name="DataFormats/TrackReco"/>
<flags EDM_PLUGIN="1"/>

#replace
<use name="FWCore/Framework"/>
<use name="FWCore/PluginManager"/>
<use name="FWCore/ParameterSet"/>
<use name="DataFormats/TrackReco"/>
<use name="CommonTools/UtilAlgos"/>
<flags EDM_PLUGIN="1"/>
```

**For more statistic, we need to set -1 for the `maxEvents` in `python/ConfFile_cfg.py` file.**

```bash
vi python/ConfFile_cfg.py
```


```bash
#find
process.maxEvents = cms.untracked.PSet( input = cms.untracked.int32(1000) )

#replace
process.maxEvents = cms.untracked.PSet( input = cms.untracked.int32(-1) )
```

save&quit with pressing `esc` and typing `:wq`.


**Since we made changes in cc file (plugins/DemoAnalyzer.cc), we need to re-compile:**
```bash
cd $CMSSW_BASE/src/DataAnalyzer/DemoAnalyzer
cmsenv
scram b -j 4
```

**Let's run it again with `cmsRun`:**

```bash
cmsRun python/ConfFile_cfg.py
```

**You should see some text as below:**


    =============================================
    
    MessageLogger Summary
    
     type     category        sev    module        subroutine        count    total
     ---- -------------------- -- ---------------- ----------------  -----    -----
        1 fileAction           -s file_close                             1        1
        2 fileAction           -s file_open                              2        2
    
     type    category    Examples: run/evt        run/evt          run/evt
     ---- -------------------- ---------------- ---------------- ----------------
        1 fileAction           PostGlobalEndRun                  
        2 fileAction           pre-events       pre-events       
    
    Severity    # Occurrences   Total Occurrences
    --------    -------------   -----------------
    System                  3                   3
    
    dropped waiting message count 0
    


**Now you can check your results:**

```bash
root -l Results2018.root
```

This will activate the root with your result file.

**Open a `TBrowser` to see the results:**

```bash
TBrowser b
```

**This command line will open a new browser window:**

When you see the browser, (be patient, it can be slow) double click on your root file `Results2018.root` on the left side, then `demo` and `HEiEta` histogram to see the results on the right side.

![Root Usage](https://raw.githubusercontent.com/asimsek/CERNComputingAccount/main/root.png "Root Usage")


To save the plot as `pdf` or `png`, click the `File` on top and click on `save as`. Give a name and click on `save` button. Now you can close the TBrowser and check the pdf or png file in your directory. To do that, you need to quit from root with typing `.q` and press enter. Then use the `ls -lhtr` command to list your directory.

To display your png or pdf file use `display` command:

```bash
display FileName.png
```

> ps. display shows both png and pdf. You can also use `evince` command for only pdfs. The usage is same, just replace `display` with `evince`.

------------

> **Congratulations!! From now, you can easily analyze the CMS data.**

------------

------------



For more, please follow this twiki page:
https://twiki.cern.ch/twiki/bin/view/CMSPublic/WorkBookWriteFrameworkModule?LOCALSHELL=bash
