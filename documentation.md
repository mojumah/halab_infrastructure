# halab_infrastructure AWS S3 Upload
# Install Jenkins and JDK  
wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add -  
sudo sh -c 'echo deb https://pkg.jenkins.io/debian-stable binary/ > \  
/etc/apt/sources.list.d/jenkins.list'  
sudo apt-get update  
sudo apt-get install jenkins  
apt install default-jre  
apt install openjdk-11-jre-headless  
sudo systemctl start jenkins  
sudo systemctl status jenkins  
# Setup WebHook in GitHub Repo  
http://JenkinsServerIP:8080/github-webhook/  
Content type application/json  
# Configure Jenkins
1- Add Credentials in Jenkins, User Name is AWS ID, password is AWS Secret Key  
2- Install AWS Steps plugin  
3- Create pipeline in Jenkins using Git, Poll SCM, GitHub Repo.  
# To do:
First fix the but, this command is for s3 upload and does not do sync. So for example if a file is renamed or deleted the pipeline will not remove that file.  
1- Using Jenkins UI install BitBucket integration plugin  
2- Test SCM integration with a test Private BitBucket Repo  
3- Test S3 sync to a test S3 bucket  
4- Change the GitHub Repo in Jenkins pipeline configs to the halab.info private BitBucket repo (integrate jenkins with BitBucket)  
5- Change in Jenkinsfile bucket name to halab.info  
6- on Bitbucket halab.info repo Add a web hook to the Jenkins server  
7- Create a branch in the halab.info private repo calling it main  
8- Add Jenkinsfile to main  

Or move all the private BitBucket repo to GitHub  