## Retrovert Musicplayer 

Retrovert is a music player for macOS, Windows, and Linux that primarily focuses on music made for systems such as the Amiga, C64, and various gaming consoles. While Retrovert supports MP3, FLAC, Ogg Vorbis, and other formats, these are not the main focus.

## Motivation

Over many years, I have tried various players, and while some of them hold up, none have been what I was looking for. Before starting this project, I looked around quite a bit for alternatives, but nothing really fit the bill.

The closest option is likely [XMPlay](https://www.xmplay.com/), but it is only available for Windows and is closed-source, which isn't what I want either, although feature-wise, it's fairly good. 

I started this project about seven years ago (then named HippoPlayer). I did some work in a private repository and had something very basic up and running. Then, other things came up, and the project has been on ice for many years, but I always had it in the back of my mind that I wanted to return to it.

The aim I have with Retrovert is "a modern music player for your old-school needs." This means it should feel nice and great to use, with features that you can expect from a modern player, but also allow you to play older formats in the best way possible.

Over many years I tried various players and while some of them hold up none of them has been what I been looking for. Before starting this project I looked around quite a bit for alternatives and nothing really fit the bill.

# Repository structure

Retroverts is a highly modular project, and the repository is structured as such. The idea is that the core player can be used from other projects, and the UI can be replaced with something else if desired.

## core

https://github.com/RetrovertApp/retrovert-core

The core is the main part of Retrovert. It contains the loading of files, plugins, handling of playlists, and decoding the audio. Output of the audio is done through a plugin system, and can target different outputs such as regular audio output or writing to a file.

## core-loader

https://github.com/RetrovertApp/core-loader

This is used by the frontends to load the core dynamic library. It sets up the interface to make it easier to call functions in the core. 

## retrovert

https://github.com/RetrovertApp/retrovert

This is the main graphical user interface for Retrovert (currently under heavy development). It uses the core and core-loader to play music.

## retrovert-console

https://github.com/RetrovertApp/retrovert-console

This is the terminal interface for Retrovert. It uses the core and core-loader to play music.
