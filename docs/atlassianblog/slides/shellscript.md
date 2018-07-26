##  Shell Script

To make it more fun: pull data from Github too

```
#!/bin/bash
echo "Building master branch"
git clone https://$GIT_CREDENTIALS@github.com/Stwissel/stwissel.github.io.git
echo "Building blog output"
java -jar bin/blogrenderer-fat.jar
echo "Result to blog transfer"
now=$(date +"%m_%d_%Y")
message="Commit from CI ${now}"
cd stwissel.github.io
git config user.email "stw@linux.com"
git config user.name "Stephan H. Wissel"
git add --all
echo "Commiting to git"
git commit -m "$message"
echo "Commit complete, pushing to github"
git push origin master
echo "Rsync to host"
mkdir -p ~/.ssh
ssh-keyscan -t rsa wissel.net >> ~/.ssh/known_hosts
rsync --ignore-times --recursive --copy-links --exclude '.git' -e "ssh -o 'StrictHostKeyChecking no' -o 'BatchMode true'"  . stw@wissel.net:/home/stw/www
echo "Done!"
```
