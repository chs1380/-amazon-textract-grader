# Amazon Textract Grader
This project uses AWS AI services to speed up grading task.

# AWS Cloud9 Setup Environment
```
git clone https://github.com/wongcyrus/amazon-textract-grader
cd amazon-textract-grader/  
npm i nvm  
nvm install 14
nvm alias default 14  
npm install -g yarn  
npm install -g --force npx  
echo "" >> ~/.bash_profile   
echo "alias pj='npx projen'" >> ~/.bash_profile
alias pj='npx projen'
bash <(curl -sL https://gist.githubusercontent.com/wongcyrus/a4e726b961260395efa7811cab0b4516/raw/490162cebcaa44210bb2eab0e6883e57fd880a27/resize.sh) 50
```

## Source Code Folder
src/
Don't touch code in lib/ which generates by projen.


## Cloud9 TypeScript Formatter
Follow
https://gist.github.com/wongcyrus/4e8a2e78045e11f7c5a55e4e244fe3d2


### Auto compile
You need to run TypeScript compiler at the background with new terminal.
pj watch
### Install all node packages
./install_all_packages.sh
### Upgrade all node packages
./upgrade_all_packages.sh
### Set your email in environment variable and run projen to update cdk.json.
export email=cywong@vtc.edu.hk
pj
### Deployment
pj deploy
### Deployment hotswap
pj deploy-hotswap

#### Checkout projen documentation
https://github.com/projen/projen


Input format for AssignmentsTextractStateMachine

<code>{
"standardAnswerKey": "cywong@vtc.vtc.edu.hk/IT41213TestAnswer.pdf",
"scriptsKey": "cywong@vtc.vtc.edu.hk/IT41213Testscript.pdf"
}</code>
