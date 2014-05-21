Valerie (version 0.1.6)
=====================

Valerie is a friendly English-like interface for your command line.

She translates English-like phrases into commands in case you every run into
situations [like this][xkcd].

[xkcd]:http://xkcd.com/1168/

This means you don't have to leave your command line to look up an obscure but useful command. Just ask Valerie!


By Analogy
----------

iPhone users: it's like Siri for the command line.

Android users: it's like Google Now for the command line. (What's Google Now? It's that thing you talk to that does stuff.)


Set Up
------

Manually:

1. First, git clone this repo with `git clone https://github.com/pickhardt/valerie`
2. Add the following alias to your ~/.bashrc
```alias valerie="~/path/to/valerie/main.rb"```
3. Use it! For instance, you can run commands: "valerie how many words are in this directory" or "valerie uncompress something.tar.gz"

Automatically:

1. First, git clone this repo with `git clone https://github.com/pickhardt/valerie`
2. Run `ruby install.rb` in `valerie/`.
3. Use it! For instance, you can run commands: `valerie how many words are in this directory` or `valerie uncompress something.tar.gz`


Examples
--------

Give Valerie natural language input, for instance `valerie whats my username`, and she'll respond in the most appropriate way.

    > valerie whats my username
    Valerie: Running whoami
    jrp
    
    > valerie whats my real name
    Valerie: Running finger `whoami` | sed 's/.*: *//;q'
    Jeff Pickhardt

If there's more than one way Valerie could respond, she'll ask you to select the one you want.

    > valerie whats my name
    Valerie: Okay, I have multiple ways to respond.
    Valerie: Enter the number of the command you want me to run one, or N (no) if you don't want me to run any.
    [1] whoami
        Gets your system username.
    [2] finger `whoami` | sed 's/.*: *//;q'
        Gets your full name.
    > 2
    Valerie: Running finger `whoami` | sed 's/.*: *//;q'
    Jeff Pickhardt


Mission
-------

The mission of Valerie is to provide a way to use computers through natural language input.

Specifically, the benefit is being able to do things on your computer without leaving the command line or screwing around on the internet trying to find the right command. Valerie just works.


Documentation
-------------

The following is a non-exhaustive list of things you can do:

    Count
    valerie how many words are in this directory
    valerie how many characters are in myfile.py
    valerie count lines in this folder
    (Note that there's many ways to say more or less the same thing.)
    
    Config
    valerie change your name to Joe
    valerie speak to me
    valerie stop speaking to me

    Datetime
    valerie what time is it
    valerie what is todays date
    valerie what month is it
    valerie whats today
    
    Find
    valerie find me all files that contain california

    Internet
    valerie download http://www.mysite.com/something.tar.gz to something.tar.gz
    valerie uncompress something.tar.gz
    valerie unarchive something.tar.gz to somedir
    (You can use unzip, unarchive, untar, uncompress, and expand interchangeably.)
    valerie compress /path/to/dir
    
    iTunes
    valerie mute itunes
    valerie unmute itunes
    valerie pause the music
    valerie resume itunes
    valerie stop my music
    valerie next song
    valerie prev track
    valerie what song is playing
    (Note that the words song, track, music, etc. are interchangeable)

    Fun
    valerie go crazy
    valerie whats the meaning of life
    ...and more that are left for you to discover!

    Map
    valerie show me a map of mountain view
    
    Meta
    valerie what version are you (or just valerie version)
    valerie whats your github again
    
    Permissions
    valerie give me permission to this directory
    valerie give anotheruser ownership of myfile.txt
    
    Process
    valerie show me all processes by root containing grep
    valerie show me all my processes containing netbio
    
    Sizes
    valerie show size for myfile.txt
    
    Spotify
    valerie play spotify
    valerie pause spotify
    valerie next spotify
    valerie previous spotify
    
    User
    valerie whats my username
    valerie whats my real name
    valerie whats my ip address
    valerie who else is logged in
    valerie whats my version of ruby
	
	Web queries
	valerie turn web on
	valerie please tell me what is the weather like in London

Contributing
------------

Contributions are welcome! If you would like to contribute, please issue a pull request against the **dev branch**, not the master branch.


Versioning
----------

Releases will follow a semantic versioning format:

`<major>.<minor>.<patch>`

For more information on SemVer, visit [http://semver.org/](http://semver.org/).

License
-------
Released under the Apache License 2.0. Related link: www.apache.org/licenses/LICENSE-2.0.html
