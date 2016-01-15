# Submitting Patches to Rakudo

This is how one casual rakudo without much development experience
has gone about sending patches to rakudo.

# If not done so already, fork Rakudo

The first thing required to submit a patch to rakudo is a fork
of rakudo/rakudo under your own github user account, done by going
to https://github.com/rakudo/rakudo and click on the fork button.

Then cloning your fork of rakudo to your local machine.  It can be easier
to have a separate clone/direcory for committing PRs than you did your
development work in, unless you have a very solid familiarity with git
and the rakudo toolchain.

    git clone 'git@github.com:your_username/rakudo.git'
    cd rakudo

Then adding the upstream repository as a remote tracking branch

    git remote add upstream 'git@github.com:rakudo/rakudo.git'
    git remote -v # shows your fork as "origin" and rakudo/rakudo as "upstream"

# Freshen up rakudo from upstream and create a branch for your patch

    git stash # in case you had uncommitted changes in your current branch
    git fetch upstream
    git checkout upstream/nom
    git branch myfirstPR   # choose a descriptive name for your branch
    git checkout myfirstPR
    git log -1 # Cut the first 7 or so leters of the hash into your clipboard

# Generating the patch from your development/testing tree.

Now going to the rakudo tree containing modifications, collapsing the
commits in that git tree, so as not to push every little edit made to add or
remove debug statements.  In my case I developed the patch by editing and
committing to rakudobrew's clone in git_reference/rakudo.

    cd whatever/rakudobrew/git_reference/rakudo
    git diff # <- paste in the commit hash from above (head of rakudo/rakudo nom)
    # redirect that to a file e.g. > myfirstpatch.diff

Now, if the patch does multiple things, sometimes I take the time to
chop it up a little into multiple patch files.  In case there is a problem
with the entire commit, the good bits can be cherrypicked if they are
separate.

# Apply the patches in the PR tree

    # cd back to your clone
    patch -p1 < myfirstpatch.diff
    git add # any new files made by the patch
    git commit -a # one line comment, then if needed one blank line and more comment
    # repeat for any other patch sections

# Push the new branch to your fork

Wait to do this until right before doing the next section, for best convenience.

    git push origin myfirstPR:myfirstPR

# Go to the github UI and submit the PR

Go there right away, and you will get convenient "compare and pull request"
bars that show your recent pushes.  Make sure before submitting the PR
that you are submitted from the correct branch, and to the correct branch
of rakudo/ (usually rakudo/nom).

# Adding to a PR after time has passed or for a merge conflict

TODO this is a general github PITA thing that deserves a recipe
