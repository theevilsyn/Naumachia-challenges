====================
Naumachia Challenges
====================

Welcome to the open-source repository for `Naumachia <https://github.com/nategraf/Naumachia>`_ challenges! If you have
some challenge ideas and/or code to contribute, I would love to see it!

All of the challenges in this repository can be played live at `naumachiactf.com <https://naumachiactf.com>`_, and you
can join the `Discord <https://discordapp.com/invite/gH9ZgeT>`_ channel to chat!

The challenges in this repository are challenges I have written for past CTFs and open-sourced after. It's my hope that
this is helpful to developers who are interested in writing their own challenges or just curious as to how it all works.

Challenges:
 * `Stop and Listen <listen>`_
 * `Stuck in the Middle <middle>`_
 * `Straw House <straw>`_
 * `Stick House <sticks>`_
 * `Brick House <brick>`_
 * `Segal's Law <segal>`_
 * `A Rose by Any Other IP <rose>`_
 * `Secret Recipe <recipe>`_
 * `Open Letter <letter>`_
 * `Table Scraps <scraps>`_
 * `Calculator <calculator>`_
 * `Clock <clock>`_
 * `Homework Help <homework>`_
 * `AltF4 for Ops <altf4>`_
 * `J. Schmidt <schmidt>`_

**Writeups** written by players can be found in the `writeups folder <https://github.com/nategraf/Naumachia-challenges/tree/master/writeups>`_

Hosting
-------

You can host these challenges for your own competition or class with the following steps:

1. Clone `Naumchia <https://github.com/nategraf/naumachia>`_ to your machine (``git clone https://github.com/nategraf/naumachia.git``)
2. Install the dependencies listed in tHe Naumachia README and the network drivers below.
3. Clone these challenges into the `challenges` subdirectory. (``git clone https://github.com/nategraf/naumachia-challenges.git naumachia/challenges``)
4. Copy config.yml into your Naumachia directory.
5. Run `configure.py`
6. `sudo docker-compose up`!

These challenges make use of custom libnetwork (Docker networking) driver including:
  * `l2bridge <https://github.com/nategraf/l2bridge-driver>`_ - Networking driver focused on providing (only) layer 2 connectivity
  * `static <https://github.com/nategraf/static-ipam-driver>`_ - IPAM driver designed to work with overlapping and static IP assignemnts
  * `mini <https://github.com/nategraf/mini-ipam-driver>`_ - IPAM driver designed to allocate small subnets for lots of little networks

It is recommended that you install and run these with these challenges and any you write, as they are designed to
sidestep some of the hair-pulling long days and nights I spent working around the design choices of libnetwork.
