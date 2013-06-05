mylog

A level based logging package for go.

Source -> https://github.com/jcelliott/lumber

Design is same as the original author's. Most of the code might be same. However, I re-did the filelogger.go, it didn't work with my system and I don't yet have the expertise to deal with goroutines and channels, so I couldn't fix it. 
Hence, 'filelogger.go' is a highly simplified version. 
Also, I added a 'multilogger.go' as I needed the output at both console and in a log file.


Installation:
To install type this in your terminal
    
            go get github.com/n-o-m-a-d/mylog

This should create a repo named '/n-o-m-a-d/mylog' inside "$GOPATH/src/pkg/github.com/".

Usage:
Example:

import "mylog"

mylog.DisplayLevels()                                               // displays the levels used by the logger

mylog.Info("This is the default level of default logger")

level := mylog.CurrentLevel()                                       // spits out the current level of the logger

mylog.Level(level - 2)

mylog.Trace("Now this should be displayed")

mylog.Fatal("Program exits after this")

mylog.Error("Program has already exited. This won't be printed")

// To create your own loggers
log := mylog.NewFileLogger("filepathname",level)                    // see level output from DisplayLevels()

// Now use the same functions as above. Output will be logged to the "filepathname" file.


log := mylog.NewLogger("filepathname" string,level)                 // creates a multiwriter that writes to both  "filepathname" and "os.Stdout"

