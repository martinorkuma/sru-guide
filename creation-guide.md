# Creation Guide 
A guide detailing the steps I took to create the repo and sru-guide.

Platforms used:
- GitHub
- Bash
- Python

## Create the project skeleton  
I began by creating a repo in my GitHub profile and then cloning it: https://github.com/martinorkuma/sru-guide 

```Bash
git clone https://github.com/martinorkuma/sru-guide.git
cd sru-guide

python3 -m venv .venv
source .venv/bin/activate

pip install zensical
zensical --version
```

Update the .gitignore with documents and directories I don't want to appear online.
```Bash
.venv/
site/
```

## Create Workflow:  
1. Create requirements.txt: Add this: zensical==0.0.73

2. Git general workflow:

```Bash
git status

git add .
git commit -m "Initial site skeleton"
git push origin main
```

3. Write the workflow that publishes the site. 

```Bash
mkdir -p .github/workflows
```

- Create .github/workflows/deploy.yml 

4. Adding guardrails to the site. 
- Disclaimer on the home page (docs/index.md)
- A crisis support page (docs/crisis-support.md)
- 

5. Adding theme colors and a light/dark toggle

## "First 72-Hours"  

