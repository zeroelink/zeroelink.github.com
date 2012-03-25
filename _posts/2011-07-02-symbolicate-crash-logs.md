--- 
layout: post
title: Symbolicate Crash Logs
tags: 
- symbolicate
- crashlogs
---
Found myself  in a situation where I didn't save the build file, but still
have the code from that build and needed to symbolicate some crash logs. You
can use that code to generate an archive, extract the .dYSM file and use the
atos command to symbolicate:

    
    atos -o TheApp.app.dSYM/Contents/Resources/DWARF/TheApp -arch armv7 0x0000409e

