# Git-GitHub_Basics
Learn How To Use Git and GitHub on 64bit Windows-OS

# Sample

![Work-flow](https://user-images.githubusercontent.com/40707958/94034460-b25a0600-fddf-11ea-931a-4874f4215392.png)

- **Final Layout :**
![layout](https://user-images.githubusercontent.com/40707958/94036804-5349c080-fde2-11ea-85d9-bc71ef23bde5.png)

___________________________________________
## Working Rule
-------------------------------------------

- **Installing Extensions in VSCode** 
  - Step 1: Open VSCode (_Visual Studio Code_)

  - Step 2: Press CTRL+Shift+X

  - Step 3: Just copy_paste the [_extension-identifiers_], provided below:
    - **Extensions (version) [_extension-identifiers_] :** 
      - Github Pull Requests and Issues (v 0.20.0)
        > _github.vscode-pull-request-github_
      - Live Share (v1.0.2740)
        > _ms-vsliveshare.vsliveshare_

  - Step 4: Click **install** button, after complete installation, **uninstall** button will be replaced with _install_ Button.

- **All About GitHub :**
  - [Labels & Milestones](https://youtu.be/ukYSRu4k0gs)
  - [Complete Video on Github](https://www.youtube.com/watch?v=IG8_1W0a28E&list=PLWjCJDeWfDdcj8_NSNFfsbHrjCfetYJWJ)
  - [Adding images in "READ.md"](https://youtu.be/vB_Z3JjkVwU)
  - Method & Rules to write on Markdown file "README": 

     [Writing Rules](https://guides.github.com/features/mastering-markdown/)
------------------------------------------

### **USING GITHUB (via Terminal)**
------

**_Coordination between_**
  (Git hub online or remote system) and local system_ :
  
  - **Important Steps for Repository setup**
    - Press `Win` + `R` and press "Enter"
    - Type `cmd` and press "Enter"
    - Go to the directory where you want to make the folder of "Repository"
    - Use `cd` and `cd..` to move to the required directory
    - **Open github and copy the repository link**
    - Go back to "cmd prompt" and type:
    
          git clone paste_the_https_link_of_repository
  
  - **Setting Terminal in VSCode**
    - Click _code_ option and copy the link
    - Press Ctrl + ` (keyboard button above "TAB"): To open the terminal in VSCode.
    - In "Terminal" write:
          
          > git add origin "Paste the link you copied"

          > git config global user.email "email-ID"

          > git config global user.name "Profile-name" 

          > git remote

      > Here you will get the "Origin name" as remote.

    - Pull the files from remote to your directory:
            
          > git pull origin_name master

  - **Write your  codes** on the editor (Visual Studio Code).
  - **Check "git status" in Terminal** for files "_highlighted in red_"
    
        > git status 

  - **Add the "_Modified files_"** to your local system.
    
        > git add file_name.extension

    or,
        
        > git add .

  - Add message or comment "_between the double quotes_" then, **"commit" / save your changes**
    
        > git commit -m "Write the 'changes' that you made"

  - When you are done with your coding and willing to upload/ **PUSH on "_Remote system_"**
    - _Remember to **make your new branch** and always "_push your changes_" on it, **avoid direct pushing to master branch.**_

          > git push -u Origin_name Branch_name

    > **Note :** _To know / get your "origin_name" and "branch_names"_ type this code in the terminal.

  - **PULL** / download the updated file from **master-branch** or **particular-branch** to make changes in it.
        
        > git pull Origin_name Branch-name
  
    Or,

        > git pull Origin_name master

-------------------------------------
### **Keypoints**
  - Download code.
  - Make changes in it.
  - Pull Requests or make a new-branch
  - Pull the required file from the master branch
  - Write your codes
  - Commit your changes
  - Push it on your **new-branch**
  - Put a pull request and you are done.
  
  >  **Reference for pull request :**(Video)  
  >[Pull Request](https://youtu.be/e3bjQX9jIBk)


### **_You can handle these methods directly on git-hub site, manually without any coding_**
  - Make new-branch.
  - Click on file you want to make changes and select _"Edit / Pencil - symbol"_
  - Make required changes and commit the changes you made to new-branch "_In statement similar to pseudo code_".
  - When your final product is ready, that is ready to add your code to main file. 
    
    > Then, _**Pull Request to master**_ on combining with master, _you would be ready to publish your new patch file or your new version of file_.

- **While in cmd prompt or Git Bash, to access your editor** enter the code:
        
       > ./

-------------------------------------
# ERRORS in Code Execution

## **Push and Pull Rejection**
 (Error type: Rejection)
--------------------------
- _For Rejection of Push or Pull request, either do as asked in hints or enter the following codes:_
    
      > git pull --rebase origin_name master

      > git push origin_name master

- For Git 2.6+ after executing above code once, execute given code:
  > Here, **autoStash** is **correct**, _"autostash" is wrong_

      > git config --global pull.rebase true
    
      > git config --global rebase.autoStash true

- Now, simple pull command will be enough

      > git pull

  >**Note :** for regular pull without rebase, we can use:

      > merge.autostash

   > **Reference :** https://www.oreilly.com/#pull-rebase

## **Error "_credential-osxkeychain_"**
-------------------------------------
  
  Possible error is "comparision issue":    
  - There is a conflict between your old and new code, "either **compare** or **overwrite** your changes".

  - Either fix it on V.S Code as specified.
  
  Or,

  - Fix it manually on the github.
__________________________________________
## Git/Github Basics:
- **Understanding the terms in github:**

  - **Origin_name :**
    
        > git remote
    
  - **Branch_names :**
      
        > git branch

  - **Create new branch :**

        > git branch branch_name

  - **Push :** Sending our changes _from our machine_ to the **remote machine**.
      
        > git push -u origin master

  - **Pull :** Taking the changes _from remote machine_ made by other developers to _our local system_ and applies the changes.

        > git pull origin master

  - **Checkout** / switch to a branch (other than master):
        
        > git checkout branch_name

  - **Clone :** Make copy of repo present on remote system to local. _It is used when we losses or accidentally delete our entire local file and want to fetch it again to work on._
  It will fetch the last commit on remote system.

        > git clone paste_link_of_the_repository

  - **Fetch :** Downloads the updated file from remote system but doesn't apply the changes unless it's merged, unlike **pull**.

        > git fetch origin_name

  - **Merge :** Applies the changes made in remote system to local system.
        
        > git merge origin_name/branch_name

    Or,

        > git merge origin_name/master


  - **Commit :** _Comment or message_ you would like to type for the changes that you made.

        > git commit -m "comment the lastest changes"
  
   >**Reference :** [Complete Detailed Video on 'Git'](https://youtu.be/H63nJJhoiMw)

___________________________________________
## Source File

- **REQUIRED SOFTWARES :**
  - **Git** 
    > [Download link](https://git-scm.com/downloads)

    - Click or **select your _Operating system_** to start downloading

    - **Remember:** Select "_cmd prompt and git bash_" both interface to run Git, while installation.
  
  - **GitHub Desktop**
    > Available only for 64 bit OS :
    [Download GitHub Desktop](https://desktop.github.com/)

  - **Visual Studio Code**
    > Windows : 
     [64-bit OS](https://code.visualstudio.com/docs/?dv=win64user)


- **Accessing Files**
  - Click at **"Code"** on **top left corner** 
  - Same interface will be available with several files in it.
  - Click the **File name** or **Folder name** that you want to access.
  - Make Required changes and **"Pull Request"**

- **IMPORTANT LINKS**
  
  - **Templates :**
    > Webpage Creation : [Wordpress](https://wordpress.com/create/?utm_source=bing&utm_campaign=bing_wpcom_search_brand_desktop_row_en&utm_medium=paid_search&keyword=wordpress&creative=76759747017204&campaignid=282011434&adgroupid=1228154574804979&matchtype=e&device=c&network=o&targetid=kwd-76759730299059&msclkid=87188cdfd0fb19ca25e9d3806e41e0b0)

  - **Image Source**
    > Free images: [PIXABAY](https://pixabay.com/)

    > Free .png images: [freepngs](https://www.freepngs.com/)
    
  - **Important Links**
    - For In-built features: [Bootstrap 4](https://getbootstrap.com/)
    - For icons: [fontawesome](https://fontawesome.com/v4.7.0/)

## Disclaimer (_optional_)
_Can be included in the footer section._

------------------------------
# Some Awesome Extensions for VS Code
------
## **PACKS :-**

> **ANGULAR :** *loiane.angular-extension-pack*
1. Angular Files : *alexiv.vscode-angular2-files*
1. Angular Language Service: *angular.ng-template*
1. Angular Material 2, Flex layout : *1tontech.angular-material*
1. Angular Schematics : *cyrilletuzi.angular-schematics*
1. Angular Snippets (Version 9) : *johnpapa.angular2*
1. Angular2-switcher : *infinity1207.angular2-switcher*
1. Arrr : *obenjiro.arrr*
1. Auto Close Tag : *formulahendry.auto-close-tag*
1. Auto Import : *steoates.autoimport*
1. Auto Rename Tag : *formulahendry.auto-rename-tag*
1. Bracket Pair Colorizer 2 : *coenraads.bracket-pair-colorizer-2*
1. Debugger for Chrome : *msjsdiag.debugger-for-chrome*
1. EditorConfig for VS Code : *editorconfig.editorconfig*
1. Karma Problem Matcher : *rctay.karma-problem-matcher*
1. Move TS - Move TypeScript : *stringham.move-ts*
1. Paste JSON as Code : *quicktype.quicktype*
1. Path Intellisense : *christian-kohler.path-intellisense*
1. Prettier - Code formatter : *esbenp.prettier-vscode*
1. Simon Test : *simontest.simontest*
1. TSLint : *ms-vscode.vscode-typescript-tslint-plugin*
1. TypeScript Hero : *rbbit.typescript-hero*

---
> **PYTHON :** *donjayamanne.python-extension-pack*
1. Magic python : *magicstack.magicpython*
1. Python : *ms-python.python*
1. Jinja : *wholroyd.jinja*
1. Django : *batisteo.vscode-django*
1. Visual Studio IntelliCode : *visualstudioexptteam.vscodeintellicode*

--------
## **INDIVIDUALS :-**

**BASIC :** (Snippets & Live Preview **VVI Extensions**)
1. Django (Auto-complete codes) :*batisteo.vscode-django*
1. HTML Snippets (Auto-complete codes) : *abusaidm.html-snippets*
1. GitHub Pull Requests and Issues : *github.vscode-pull-request-github*
1. Live HTML Previewer (Opens side preview) : *hdg.live-html-previewer*
1. Live Server : *ritwickdey.liveserver*
1. Live Share : *ms-vsliveshare.vsliveshare*

**THEME :**
1. Henna Color Theme : *httpsterio.henna*
1. Julia Color Theme : *cameronbieganek.julia-color-themes*
1. Midnight-color : *lucabockmann.midnight-color*
1. Neon Vommit Color Theme : *ghgofort.neon-vommit*

**BOOTSTRAP :**
1. Bootstrap 4, Font Awesome : *thekalinga.bootstrap4-vscode*
1. Bootstrap v4 Snippets : *zaczero.bootstrap-v4-snippets*
1. NgBootstrap Snippets (Angular) : *ktriek.ng-bootstrap-snippets*
1. Font Awesome Auto-complete : *janne252.fontawesome-autocomplete*
1. IntelliSense for CSS class name : *zignd.html-css-class-completion*

**JavaScript & Express :**
1. Emmet JSS (Auto-completes the JS code): *carbonid1.emmet-jss*
1. ExpressJs 4 Snippets : *gurayyarar.expressjs-4-snippets*

**IOT (Internet Of Things) :** 
- (Auto-complete codes for Aurdino, IOT, CMSIS, ESP-IDF, FreeRTOS, libOpenCM3, mbed OS, Pulp OS, SPL, etc)

- Platform IO IDE: *platformio.platformio-ide*

----
