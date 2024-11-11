# Project templates

What it says on the box! This is just a repository for our project templates, to initialise any new repository from.

## Quick start

- Clone this repository if you haven't already. If you want any specifics aside from the most generic and code-agnostic version, check out the appropriate branch (see below for the currently supported branches).
- Make an empty repository on GitLab / GitHub and name it as you wish, e.g. `spam-eggs-and-ham`.
- On your machine / locally, change the root name of **this** repository from `project-templates` to the name you've given to your repository, e.g. `spam-eggs-and-ham`
- In git bash, run these commands (anything within <> is to be replaced with actual content):
  - `rm -rf .git` (that wipes git history)
  - `git init` (that re-initialises under the new repository name and with a clean slate; if you want the main branch to have a specific name other than default you can add `--initial-branch=<main-trunk-or-top-dawg-or-whatnot>`)
  - `git remote add origin <URL-of-spam-eggs-and-ham>` (that tells git to now link the empty repository with this folder)
  - `git add -A .` (that tells git to commit everything in the folder to memory / take a snapshot of everything, no filters :P)
  - `git add -f data/.gitignore` (that allows git to keep the folder, despite ignoring everything in it)
  - `git commit -m '<here goes your first commit message, e.g. 'look at me, brand new and full of promise of the bestest code practices'>'`
  - `git push origin <main-trunk-or-top-dawg-or-whatnot>`


### Branches

#### Currently supported

- `trunk` (that is the main branch with a bare minimum of structure or pre-configuration)
- `dev` (that's a branch to test-drive new components)

#### Near future

- `py-project`
- `R-project`

#### Wishlist

- `py-package`
- `py-project-buff`

### Dear reader...

Although you're _technically_ good to go now and can go off and code... 
Please please please read also _Good practices_ just below. 

## Good practices

- **modularise**: whatever language you may be using, if you need to do something twice in different parts of workflow, make it a function, don't copy-paste code;
- for the love of all that is holy, **comment**! 
- group related things together in a logical **hierarchy**, even if it's just two or three files; e.g. source code folder separate from scripts folder and (always) data a separate non-commitable folder.

Which brings me to...

### Data

Actual data should not be stored on git, aside from a handful of exceptions:
- if you're publishing a dataset, such as a benchmark (and it is not v big, otherwise use dedicated servers); **however** any data that needs to be published and versioned should live in its own repository - even better, it could be a `huggingface` dataset;
- if it is some reference / lookup data that is required by the code, e.g. a conversion table; 
- if it is a small sample for use with a demo to illustrate the working of the code and / or structure of the data.

## Repository structure

It isn't necessary and not that many people keep an up-to-date repo structure, but it helps *so so much* for collaboration (rather than hunting down through the imports). 

* * *
    project-templates          --> root folder **Change it to the name of your project!** 
    │ 
    ├── data                   --> **empty** folder for data 
    │   │   
    │   └── .gitignore         --> making sure no data is stored on git, just the folder
    │ 
    ├── src                    --> code base, **you might also want to change this..?**
    │   │   
    │   └── TBD?               --> _To Be Developed_ submodules?
    │
    ├── README.md
    │ 
    └── .gitignore
* * *