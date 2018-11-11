[![Build Status](https://secure.travis-ci.org/onlyuser/rm-dup.png)](http://travis-ci.org/onlyuser/rm-dup)

rm-dup
======

Copyright (C) 2011-2017 <mailto:onlyuser@gmail.com>

About
-----

rm-dup is a script to remove duplicate files.

A Motivating Example
--------------------

<pre>
bash&gt; rm-dup . mp4
Processing: ./file (5).mp4.. 9.8G
    Info: Found extra copy of file with same size: ./file (4).mp4.. 9.8G
    Info: Deleting duplicate: ./file (5).mp4.. 9.8G
    Info: Ignoring duplicate file with different size: ./file (3).mp4.. 4.2G != 9.8G
    Info: Ignoring duplicate file with different size: ./file (2).mp4.. 3.1G != 9.8G
    Info: Ignoring duplicate file with different size: ./file (1).mp4.. 9.0G != 9.8G
    Info: Ignoring duplicate file with different size: ./file.mp4.. 11G != 9.8G
</pre>

Requirements
------------

    bash find rm du

Limitations
-----------

<ul>
    <li>Duplicate file detection based on filename and file size.</li>
    <li>Duplicate files must match pattern ".* ([0-9)+)\.$EXT", where $EXT is file extension.</li>
</ul>

Installation (Debian)
---------------------

1. git clone https://github.com/onlyuser/rm-dup.git

Usage
-----

<pre>
gen-callgraph &lt;DIR!={$HOME}&gt; &lt;EXT={mp4/mp3/png/jpg/gif/bmp}&gt;
</pre>

References
----------

Keywords
--------

    disk-space, disk-usage, duplicate-files, duplicate-detection
