# HSD

Scripts from <a href="http://jonrohan.me/guide/git/dead-simple-git-workflow-for-agile-teams/">Jon Rohan</a>

I tweaked them a little bit in order to play with other branches than master.

## Installation

1. Download the files. You should have all the scripts in a folder named 'scripts'.
2. Move that folder wherever you want.
3. Edit your '.bash_profile' file in order to add the 'scripts' path to your PATH environment variable (just add `:scripts_path` at the end of the line `export PATH=$PATH:...` to get something like this : `export PATH=$PATH:/Users/gilp/dev/scripts`)
4. Save and close the '.bash_profile' file
5. You should be good!

## Usage

### Checkout a new branch to work on a feature

```
gcb new_feature
```

### HSD

This script executes the hack & ship & dwf scripts.

```
hsd
```

or

```
hsd dev
```
if your main branch is 'dev'

### Hack

This script gets commits from the main branch (master if not set) and rebases the feature branch to the main branch.

```
hack
```

or

```
hack dev
```
if your main branch is 'dev'

### Ship

This script merge commits from the feature branch to the main branch (master if not set) and pushes the main branch.

```
ship
```

or

```
ship dev
```
if your main branch is 'dev'

### Done With Feature

This script deletes the feature branch and checkouts the main branch (master if not set).

```
dwf
```

or

```
dwf dev
```
if your main branch is 'dev'