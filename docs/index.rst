.. CovertUtils documentation master file, created by
   sphinx-quickstart on Sun Jul 23 17:17:59 2017.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.


	 .. moduleauthor:: John Torakis <john.torakis@gmail.com>


Welcome to `CovertUtils`'s documentation!
=========================================

This Project is free and open-source, available @ Github_

.. _Github : https://github.com/operatorequals/covertutils.


A Blog post about it, explaining *motivation* and *implementation internals* is located in my personal blog: Securosophy_

.. _Securosophy : https://securosophy.com/2017/04/22/reinventing-the-wheel-for-the-last-time-the-covertutils-package/


Not a Backdoor!
---------------

Well, `almost` not a backdoor. This project is a `Python2 package` containing enough modules for implementing custom backdoors.
Everything, from file transferring to customized shells are included.

It is not a backdoor ready to be planted (well, most of the :ref:`programming_examples` are). If you are looking for backdoors, RATs and such stuff in `Python` there are some awesome projects already:

 - Weevely_
 - Pupy_
 - Stitch_
 - Empire_ (most of it in `PowerShell`)

.. _Weevely : https://github.com/epinna/weevely3
.. _Pupy : https://github.com/n1nj4sec/pupy
.. _Stitch : https://github.com/nathanlopez/Stitch
.. _Empire : https://www.powershellempire.com/


This package contains most **Building Blocks** of a backdoor. it covers the most common coding tasks when creating anything from a simple `reverse TCP shell` to a full-blown feature-rich `Agent`.

It also uses a simplistic approach of what a backdoor is, breaking it down to its basic components:

 - Agent
 - Handler
 - Communication Channel
 - Protocol


Currently, `covertutils` package provides API for:

 - Encryption
 - Chunking
 - Separate Streams (almost like `meterpreter`'s channels)
 - Compression before transmission
 - Packet Steganography
 - Customized Shell
 - Message Handling

And most of those features are used under the hood, without writing any additional line of code (e.g. `encryption`, `compression`, `streams`).


No Networking code included
---------------------------

The package provides a generic wrapper for networking, without implementing internally even the simplest of networking possibilities (e.g. `bind TCP`).

This design decision broadens the possibilities for `Communication Channels` that differ a lot from just layer 4/5 solutions. This way, there is space for `Packet Steganography` or even time-based `Covert Channels`.

And all that with the abstraction of **Object Oriented Programming**, as this package depends on it heavily (`makes multiple-inheritance an everyday thing!`).


.. toctree::
 :maxdepth: 1
 :caption: Contents:

 installation
 package_structure
 components
 prog_examples
 shells
 native_execs
 stages
 stage_api

.. toctree::
 :maxdepth: -1
 :caption: Basic Blocks:

 covertutils.handlers
 covertutils.orchestration



As the *covertutils API* Toc-Tree is **huge** (due to the code organizing, see: :ref:`package_structure`), it is really handy to use the **search page** of **Sphinx**.
