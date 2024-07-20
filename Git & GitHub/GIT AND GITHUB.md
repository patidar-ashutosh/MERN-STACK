**<ins>What is Version Control System ?</ins>**

**Answer :-** Version Control System hamare code ko track karta hai.
Version Control System yani jiska use karke ham version ko control kar sakte hai.

**IN ENGLISH :-**
Version control, also known as source control, is the practice of tracking and managing changes to software code.

Hamare pass multiple Version Control System hai.
**Like :-** Git, Apache Subversion, Concurrent Versions System, Perforce, Azure DevOps Server Etc..


``Install git in windows.``

**<ins>Git VS GitHub</ins>**

* **Git :-** Git hai wo ek version control system hai. yani ki git ek software hai. joki hamare local computer pe work karta hai.
Git hai wo hamare local repository ko track yani watch karte rehta hai.
GitHub hai wo ek website hai jaha pe ham apne repository ko remotely store karke rakh sakte hai.

* **GitHub :-** GitHub me hamara latest yani ki updated code hota hai.

**<ins>SETUP GIT CONFIG</ins>**

``git config --global user.name "userNameOfGitHub"``

``git config --global user.email "emailOfGitHub"``

``git config --list``


**<ins>Life Cycle Of A Change</ins>**

Yani ki jab ham apne local repository me koi changes karte hai to wo kese save hote hai.

**Git me basically 3 Stages(Steps) Hote hai.**

* **1. Working Directory :-** jab bhi ham apne repository me koi new file add karte hai, kisi existing file ko modifiy karte hai
to wo sab Working Directory me save hota hai.

* **2. Staging Index :-** jab ham apne new files ya modifiy files ko commit karna chahte hai to use pehle hame Working Directory
se Staging Index me move karna padta hai.
Staging Index yani ki usme jitne bhi file hai wo sab woking hai yani ki wo files ab ready hai commit hone ke liye.

* **3. Repository (Commited) :-** jab ham apne files ko permanently git commit command ka use karke commit karva te hai
tab wo files Repository yani ki Commited vale area me aa jaati hai.

**IN SHORT :-** Hamari koi bhi files directly commit nahi ho sakti hai. commit karne ke liye pehle hai files ko working directory se 
staging index me move karna pade ga uske badd ham usse Repository yani ki Commited vale area me move kar sakte hai. 

# MOST POPULAR GIT COMMANDS

``git init`` : git init ka use git ko install karne ke liye hota hai.

---

``git status`` : git status hame current working directoy me kya kya change huve hai means kya koi new file add huva hai,
koi old file modifiy huva hai ya koi file remove huva hai uska status bata ta hai.
git status hai wo working directory and staging index pe watch rakhta hai.

---

``git clone`` : git clone ka use kisi remote repository ko local computer pe copy karne ke liye hota hai.
git clone URLOFGITHUBREPO

---

``git log`` : git log ka use all commit ko dekne ke liye hota hai.

``git log n`` : git log n hame latest n number of commit show kare ga.

**Example :-** git log -3 to ye hame latest 3 commit show kare ga.

---

``git log -p`` : git log -p hai wo hame all commit ka information to show karta hai jo ki hame git log bhi deta hai. lekin git log -p
saath me hame us commit me files me previous commit ki compare me kya change huve hai wo bhi dikha ta hai. yani ki jo hame git diff
command dikha ta hai wese.

yani ki git log -p hai wo git log and git diff ka combination hai.

---

``git log --stat`` : git log --stat hai wo same git log -p jesa hee work hai lekin git log -p me hame content dikhta tha ki kon
sa content change huva hai. lekin jo git log --stat hai wo hame all commit and usme kon konsi files me changes huva hai us files
ke name bata ta hai.

---

``git log --oneline`` : git log --oneline hai wo hame all commit ke SHAID ke first 7 character and us commit ke message dikhata hai.

---

``git show SHAID`` : git show hai wo hame kisi selected commit me kya kya changes huve hai wo show karta hai.

---

``git add fileName`` : git add commit ka use file ko Working Directory se Staging Index me move karne ke liye hota hai.

---

``git add .`` : git add .(dot) hai wo jitni bhi files Working Directory me hogi sabko Staging Index me move kar degi.

**NOTE :-** git add .(dot) ko use karna recommend nahi hai.

---

``git commit -m "message"`` : git commit ka use files ko Staging Index se Repository yani ki final Commited area me move karne ke liye hota hai. git commit hai wo jitni files Staging Index me hogi un sab ko Commited area me move kar degi.

---

``git commit -am "message"`` : git commit -am hai wo ek shorthand command hai jise ham add and commit saath me kar sakte hai.

---

``git diff fileName`` : git diff hai wo hame different bata hai ki previous commit and current working me file me kya different hai.

---

``git restore fileName`` : jab ham kisi file me koi changes kar rahe ho or ab aage jake hame wo changes nahi chahiye or ham ye chahte ho ki jo hamare latest yani ki last commit tha usme us file me jo data tha wo hee data fir se is file me aa jaaye tab ham git restore ka use karte hai. git restore hai wo last commit ka data us file ke liye restore kar ke deta hai.

---

``.gitignore`` : .gitignore hai wo ek file hota hai jis me ham wo files ka name ya files ka format(like .html, .cpp) rakhte hai jo ki ham chahte ho ki Git usse track na kare yani nahi wo files Working Directory me store ho nahi Staging Index me or nahi wo files commmit ho tab ham unse files ko .gitignore file me likh dete hai.
yani ki ham .gitignore file me wo content rakhte hai joki ham chahte hai ki git usse track na kare.

---

**<ins>Branch</ins>**

``git branch`` : git branch ka use hamare pass total kitne branch hai or abhi ham kisi branch pe hai wo dekhne ke liye hota hai.

``git branch newBranchName`` : git branch newBranchName se ham new branch create kar sakte hai.

``git checkout branchName`` : git checkout ka use kisi another branch pe move karne ke liye hota hai.

``git checkout -b newBranchName`` : git checkout -b hai wo hame ek new branch create karke deta or saath me us branch me move bhi ho jaata hai.

``git merge branchNameToMerge`` : git merge ka use two branch ko merge karne ke liye hota hai.

``git branch -d branchName`` : git branch -d ka use kisi bhi branch ko local repository se remove karne ke liye hota hai.

``git push origin -d branchName`` : git push origin -d  ka use kisi bhi branch ko remote repository se delete karne ke liye hota hai.


**<ins>What is Git conflicts ?</ins>**

jab ham kisi two branch ko merge karva rahe ho or dono branch me koi same name ki file ho or us dono file me kisi same line pe koi different code ho tab hame Git conflicts ka error mil ta hai.

**Is error ko solve karne ke liye hame 2 things kar sakte hai :-**

* **1 :-**  ya to git conflicts ko resolve karke use commit kar de. Yani ki hame git ko bata de ki hame konsa code chahiye.

* **2 :-** ya fir ham ``git merge --abort`` command ko run karke ham merging ko abort kar sakte hai..

---

**<ins>Tagging</ins> :-** tagging ka use ham beta version release karne ke liye karte hai jise testing Wale code ko test kar sake..

``git tag -a tagName SHAID -m "message"`` : git tag -a ka use new tag create karne ke liye hota hai.

**Example :-** git tag -a betaV1.0 SHAID -m "My Beta Release"

``git tag -d tagName`` : git tag -d ka use tag ko remove karne ke liye hota hai.

**Example :-** git tag -d betaV1.0

---

**<ins>Git stash</ins>**

Jesi ki ham kisi remote repository ko clone karke uspe work kar rahe hai. Jisme 2 files hai fileA and fileB.

Ab ham local computer pe jo repository hai usme jo fileA and fileB me kuch changes karte hai.

Ussi time pe jo remote pe repository hai usme jo fileA and fileB usme bhi koi second developer hai wo kuch changes karta hai.

Ab yadi ham local pe git pull command ko run karte hai to hame error mile ga kyo ki Hamare local computer pe jo repository hai usme bhi fileA and fileB me changes huve hai or jo remote pe repository hai usme bhi jo fileA and fileB hai usme bhi changes huve hai.

To is error ko solve karne ke liye hame decide karna hoga ki hame remote Wale changes chahiye ya local computer Wale changes chahiye.

Yadi hame local computer ke changes chahiye to ham git commit ka use kare ge OR yadi hame remote wale changes chahiye to ham git stash ka use kare ge.

* **1. SOLVE ERROR USING git commit COMMAND :-** yadi ham git commit ka uske karke solve karna chahte hai to sab se pehle ham files ko working directory se staging area me move kare ge.

    jiske liye ham git add command ka use kare ge.

    fir ham git commit kare ge. ab jab ham git push karne jaaye ge to hame error mile ga ki push karne se pehle tume git pull karna hoga.

    kyo ki remote repository pe bhi fileA and fileB me changes huve hai. to ham git pull command ko run kare ge.

    Ab jab ham git pull command ko run kare ge to hame git conflicts mile ga jise hame resolve karna pade ga.

    git conflicts ko resolve karne ke baad hame firse git add and git commit command ko run karna hoga.

    Fir last me ab ham git push command ka use kar sakte hai.

* **2. SOLVE ERROR USING git stash COMMAND :-**

    **<ins>Why we need to use git stash?</ins>**

    Ab esa bhi ho sakta hai ki hamne jo local computer me fileA and fileB hai usme kuch important code likha ho joki ham chahte ho ki delete na ho.
    Tab ham git stash ka use karte hai.

    ``git stash`` kya karta hai ki wo ek git stash area create karta hai jisme wo working area me jitne files hoge une working area se remove karke git stash area me move karke store rakhta hai.

    Ab jab ham git pull kare ge to jo hamare remote repository pe jo updated fileA and fileB hai wo ab hamare local computer pe bhi aa jaye ge.
    kyo ki jo git hai wo jo remote pe lastest change hai une hai updated manega. Yani ki wo jo remote pe changes huve hoge une hee local computer me bhi save karke dega.

    Ab jo hamari fileA and fileB git stash area me hai une ham ``git stash apply`` command ka use karke working area me laye ge to hame git conflicts dekhne ko mile ga to hame us git conflicts ko resolve karna padega.

    git conflicts ko resolve karne ke baad ham git add and git commit karke fir git push kar sakte hai.

    **STEPS :-**
    1. git stash
    2. git pull
    3. git stash apply
    4. git add
    5. git commit
    6. git push


``git stash list`` : git stash list ka use ye dekhne ke liye hota hai ki hamare pass kitne stash area hai.

To is tarike se ham git stash ka use karte hai.

---

**<ins>Undo Commits :-</ins>** Hamare pass commits ko undo karne ke liye 3 commands hai :-> git revert, git reset and git commit --amend.

``git revert SHAID`` : Git revert hai wo commit ko revert kar deta hai yani ki jo current code hai wo delete ho jaaye ga or jo new head hoga uska jo code hoga commit ke time pe wo wala code aa jaaye ga.

Git revert ka use ham tab karte hai jab ham koi commit by mistake add kar dete hai or fir hame us commit ko undo karna ho.

Git revert hai wo ek safe operations hai kyo ki isme ham commit ki history dikhai deti hai.

Back aane ke liye Esc press karke :(Colon) press karke wq likhe ke enter kare ge.

---

``git reset SHAID`` : Git reset hai wo commit ko hee delete kar deta hai hai.

Yani ki ham git reset me jo bhi SHAID dege wo hamara HEAD bana jaaye ga or uske pehle jitne bhi commit hone wo saare commit delete ho jaaye ge.

**git reset ke saath ham 3 keywords me ke kisi ek key ka use karte hai joki hai :-**

**1. git reset --soft SHAID :-** yadi ham soft likhe te hai to kya hoga ki jab ham git reset command ko run kar rahe honge us time pe yadi working directory me kuch files hogi to wo files move ho jaaye gi staging index me.yank ki jo different hoga wo hame show hoga as a staged.

**2. git reset --mixed SHAID :-** yadi ham mixed likhe te hai to kya hoga ki jab ham git reset command ko run kar rahe honge us time pe yadi working directory me kuch files hogi to wo files hame show hogi as a modified files.

**3. git reset --hard SHAID :-** yadi ham hard likhe te hai to kya hoga ki jab ham git reset command ko run kar rahe honge us time pe yadi working directory me kuch files hogi to wo files delete ho jaaye gi yani ki files discard ho jaaye gi.

**NOTE :-** is liye ham sort and mixed ka hee use karte hai. Ham kabhi bhi hard ka use nahi karte hai kyo ki commit ko delete karna ek bad practice hoti hai or kai company me to git reset command ko run karne ki permission bhi nahi hoti hai.

---

``git commit --amend`` : git commit --amend ka use latest commit hota hai uske message ko change karne ke liye hota hai.
yani ki lastest commit ko amend karne ke liye use hota hai.