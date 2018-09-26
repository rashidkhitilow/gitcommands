# gitcommands
using git commands
git server: 10.110.20.136

##########generate public key and send to administrator#######
ssh-keygen -t rsa -C "rashid.khitilov@gmail.com"

edit config file
Host 10.110.20.136
	User git
	Hostname 10.110.20.136
	IdentityFile ~/.ssh/id_rsa_gn
##########generate public key and send to administrator#######

##########copy project to your local folder, . is important#######
git clone rashid@10.110.20.136:spm.git .
git checkout production
##########create new branch and make it active#######

.gitignore //files not to be tracked

##########create new branch and make it active#######
git branch rashid
git checkout rashid //go to rashid branch
##########create new branch and make it active#######

##########name for commit log#######
git config --local user.name "Rashid Khitilov"
git config --local user.email rashid.khitilov@gmail.com
##########name for commit log#######

##########commit changes to local branch#######
git add .
git commit -m "message"
##########commit changes to local branch#######


##########create new reference to git server repository#######
git remote add r_spm rashid@10.110.20.136:spm.git
##########create new reference to git server repository#######


##########upload updated branch to git server, all make pull before push#######
git pull r_spm rashid //mandatory before push
git push r_spm rashid
##########upload updated branch to git server#######


##########add changes from rashid branch to production branch#######
git checkout production 
git merge rashid 
##########add changes from rashid branch to production branch####### 

##########go to specific commit#######
git checkout [commit hash] 
##########go to specific commit#######





git pull r_spm production 
git push r_spm production

git remote add r_spm rashid@10.110.20.136:checklist.git

git clone rashid@10.110.20.136:checklist.git .
