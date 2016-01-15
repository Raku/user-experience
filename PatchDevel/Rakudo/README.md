# Developing and testsing patches to Rakudo

This is how one casual rakudo without much development experience
has gone about hacking on rakudo to fix/enhance stuff.  Others may
have better advice.

# Developing from a rakudobrew tree

After fighting a while with developing from inside a rakudo tree
(details too long ago to remember) I found that nowadays the full-build
time is short enough that it was less frustrating to just develop
inside rakudobrews repository.

Once built/installed from rakudobrew the subdirectory git_reference/rakudo
has a clone of rakudo.  I edit that and then:

    cd rakudobrew/git_reference/rakudo
    git pull # if you do not this now, might get a merge commit when building
    git add # any added files
    git commit -a
    # cut the hash 

Since I do not push from this clone, I feel free to be casual about commit
comments here -- they are for my own use only.

Note that if you pull, you are combining your patch with recent upstream
changes.  It's actually hard not to, and probably a good idea to do so anyway
so haven't tried to figure a way around this.  Note that if you let the pull
happen during build, because you are building from the hash of your head,
the new changes will not be rolled in unti your next 'commit -a' even though
they are pulled into git_reference/rakudo.

# Building/installing your patched rakudo

Now we build the commit that has your patch.
Personally I use triple in case I want to set the moar and nqp versions.

    cd ../..
    rm -rf moar-one_or_more_old_builds_because_they_accrue
    ./bin/rakudobrew triple <hash_from_last_section>

(...actually I have a heavily patched rakudobrew that allows me to use
"--configure-opts=--prefix=/home/username/.local" which means my
rakudobrew is usually a little stale.  Hopefully tooling will catch
up)

# Testing the patch

After checking via the CLI that my changes are working, running test suites.

    cd moar-hash_of_this_build
    make spectest
    cd t/spec
    git checkout 6.c # even more importantly, check that 6.c tests work
    cd ../..
    make spectest

These days the first one is usually clean and the second one may have a few
failures that do not involve your subject matter -- hopefully that situation
will get cleaned up soon.  If you develop patches frequently enough you get
used too what to expect to fail, if not ask on IRC for someone to gist the
current failures.  Or do a clean build without your patch.

