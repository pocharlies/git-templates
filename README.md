git-templates
=============

to use this templates:

1. Clone this proyect in any directory you want.

2. Enable git templates:

git config --global init.templatedir '{repository-folder}'

3. Make sure the hooks are executable

chmod -R a+x ~/.git-templates/hooks/

4. Re-initialize git in each existing repo you'd like to use this in:

git init

NOTE if you already have a hook defined in your local git repo, this will not overwrite it.

NOTE2 if you want to initialize all your proyect in a folder like "Workspaces" use this:

find . -type d -depth 1 -exec git --git-dir={}/.git --work-tree=$PWD/{} init \;

5. Take all hooks necessary with helpers 

This tells git to copy everything in ~/.git-templates to your per-project .git/ directory when you run git init



 just put clone this repository into ~/.git-templates
templates to git

php-cs hook in pre-commit:
  - It requires https://github.com/fabpot/PHP-CS-Fixer installed
