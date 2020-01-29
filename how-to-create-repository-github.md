# How to create a new repository (repo) in GitHub

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

Here are the steps required to create a new repo in GitHub.

  - Log in to your GitHub account 
  - Click on the Repositories tab from your profile dashboard
  - Click on the green New button, on the right-hand side
  - Choose a descriptive Repository name (using kebab-case)
  - And give an optional Description
  - Choose whether you want your repo to be Public or Private - in this case we're choosing Public
  - Check the box 'Initialize this repository with a README'
  - Click on Add .gitignore
  - And choose Node from the drop-down options
  - Click on the green Create repository button.

# How to create a development branch

  - Create a development branch from the master branch
  - To do this...
    -- Click on the Branch:master drop-down
    -- Type development in the 'create a branch' field
    -- Click on Create branch: development from 'master'
    -- Your development branch has been created.

# How to create a feature branch from the development branch

- Create a feature branch off the development branch
- To do this...
-- Click on the Branch:development drop-down
-- Type feature/the-name-of-the-branch in the 'create a branch' field
-- Click on Create branch: feature/the-name-of-your-branch from 'development'
-- Your feature branch has been created.

# How to clone a branch to your local device

- Choose the feature branch you want to clone
- Click the green Clone or download button
- Copy the URL
- Open Terminal (Mac) or Command prompt (Windows)
- CD in to the directory where you would like to clone your branch
```sh
$ cd /Users/darrenwhatford/Documents/react-project 
$ git clone https://github.com/dpwit/react-project-jan20.git
$ cd cd /Users/darrenwhatford/Documents/react-project/react-project-jan20
$ git fetch
$ git checkout feature/session-one (where feature/session-one = branchname)
// Other useful git commands
$ git status
$ git add
$ git commit // Esc :wq
$ git push origin feature/session-one (where feature/session-one = branch url + name)
// For HD
$ git deploy //includes commit comments and used in place of git commit
$ git pull
touch 'filename' // to create sa new file (on Mac only)
```

# How to add a Collaborator to your repo

- Inviting collaborators to your repo
-- you'll need the username of the person you're inviting as a collaborator
-- In GitHub, navigate to the main page of the repo dashboard
-- Under your repo name, click Settings
-- In the left sidebar, click Collaborators
-- Under 'Collaborators', start typing the collaborator's username
-- Click the Add collaborator button when the desired user is selected
-- An email invite will be sent to the user for acceptance.



