A person's experience with a programming language involves many aspects: how
a user first learns that a language exists, their first steps in that language,
their process of learning more about it, developing in it, contributing
to it, and spreading the word about it are all part of that experience.
In short, it's a huge swath of elements, which is why it's important to
have a means to efficiently identify any issues in that experience, so that it can be
improved.

I'd like to announce the creation of [The Raku User Experience
Repository](https://github.com/raku/user-experience). Its main page
enumerates various aspects of the Raku User Experience and the
sub-pages will outline plans to overcome any of the identified problems,
or perhaps serve as a documentation repository for protocols, lists
of contacts, or other additional files.

A valuable aspect of that repository is the
[Issues tab](https://github.com/raku/user-experience/issues) where
anyone can bring up an issue with any aspect of the Raku User
Experience, for possible consideration and improvement. A set of Issue
labels corresponding to main sections listed on the main page has been
created, so the Issues can be tagged approprietly.

Having a centralized place to raise such issues should prove
more useful than an occasional grumble on an IRC channel, a blog
post, or [a Reddit comment](https://www.reddit.com/r/perl/comments/40m42l/why_in_the_world_would_anyone_use_perl_6/cyvu4yp).
Those things tend to slip through the cracks and get forgotten.

## Main Sections

Here are the main sections currently available. At the moment,
they're the result of one mind's work, and thus I fully expect
changes: more sections added, sections removed, changed, or
expanded. <abbr title="GitHub Pull Requests" style="border-bottom: 1px dotted #888">PRs</abbr>
are welcome.

#### Finding Out Raku Exists

The rest of the User Experience can never exist if no one knows
Raku exists. Are there any issues that need to be addressed
when it comes to people finding out Raku is a thing? Do the
marketing materials deliver their point? Do blog articles,
social media posts, and news items about Raku ever reach
the ears and eyeballs of those who aren't familar with Raku?

#### Getting Raku

Once interest sparks up, how does a person get to the point
where they can run some Raku code and have it work? If they care, can the
person understand the difference between, say, Raku 6.c the language,
Rakudo 2015.12 the compiler, and Rakudo Star the distribution? And
if they don't care, is it still easy for them to "install Raku"?

At the time of this writing, this is a section where a definite problem
has been identified and a plan of action has been put in place.

#### Running Raku

Installation is just one step. How easy is it for a user to run
a Raku program? Such a program may require the functionality
offered by a module in the Ecosystem. Is the search feature
functional enough to find such a module? Is the toolchain
usable enough to correctly install that module?

#### Developing in Raku

A Raku programmer produces modules and programs. Is there
a toolset available to simplify that process (e.g. a
dist-minting toolkit like
[Dist::Zilla in Perl](http://metacpan.org/pod/Dist::Zilla))?
Is it easy to package a Raku program so that it can be
sold to a customer or deployed by someone not knowledgeable
about Raku?

#### Getting Help and Training

Efficiently programming in Raku is tough if you can't get
help when you run into issues or don't receive proper training.
Do Raku **and its ecosystem modules** offer useful and complete
documentation? Do Raku users know where to ask for help?
Can they easily access those channels, even if they don't have
experience with things like, say, IRC? Is it easy for them to find out
about and attend Raku conferences and workshops?

#### Reporting Problems

If a user has any issues with Raku or its compilers or modules,
or even something else, how easy is it for them to report those
problems? Will they get notified when the reported problems get resolved?

This is an area where The Raku User Experience Repository
itself falls under and can itself have issues to be addressed.

#### Contributing to Raku

Should a user wish to give back to the Raku community, how easy
is it for them to find out what needs to be done and to contribute
their work? Is it easy for them to get commit bits, if their
work is of stellar quality? Do contributors get proper recognition?

#### Interacting with the Community

A strong community doesn't just talk code all the time. They chat
about other things and go out for a drink. Is that available
in a Raku community?

Are there any community participation
barriers—whether deliberate or accidental—for persons of
a particular gender, sexual orientation, race, age, creed,
nationality, or physical, mental, or technical abilities?

Is there a Standard of Conduct that sets the bar for the expected way the
members of the Raku Community treat others? Is there a particular person one
can safely contact in private, when that Standard of Conduct is violated, or when
other members of the community are being abusive?

####  Being a Raku Programmer

The last section completes the circle the first section started.
A Raku Programmer exists in a larger world and tells that world
about Raku; whether it is by working at a job that involves Raku,
by interacting with communities of other languages, or by simply
spreading the word about Raku on blogs, social media, and conferences.

Are there resources allowing to post or search for Raku job offerings?
Are there any issues with other communities? Do Raku marketing
materials—like printable brochures or a well-written "sales pitch"—exist
and is it easy to obtain them? Is there Raku-styled merchandize, like
mugs, pens, or shirts, one could either get to keep for themselves or to
hand out at some event? Are there places someone can blog about Raku,
if they don't have a blog space of their own?

## The Frustrated Reporter

The nature of what this repository wishes to address begs an obvious
question: won't we end up with a whole bunch of low-quality Issues created
by frustrated users banging on their keyboards while foaming at the
mouth?

Well, we probably will. If I spent "three f#$(!ng hours" trying to install
a Raku compiler just to get "this stupid script" to run, I'll be quite
angry, I'll use colourful terms in the Issue I create, and I'll likely blame
the creators of whatever I tried to use for my frustration. Those
responding to such Issues must be aware of where The Frustrated Reporter
is coming from. Something made that user this aggravated and it's possible
that something can be improved.

## *"So little time, so many things undone..."*

The Raku User Experience covers a lot of things. Big things. Huge things!
I suspect most Issues won't be closed with a simple and quick one-line fix.
Some will require an extra army of Volunteers. This is what this blog
post—and, indeed, the repository itself—is all about: inviting people to
pitch in. Not only to report the issues,
but to attempt to resolve them, and... to become a part of The Raku User Experience itself.
