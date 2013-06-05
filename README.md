mylog

A basic level based logging package for go.

Source -> https://github.com/jcelliott/lumber

Design is same as the original author. Most of the code might be same. However, I re-did the filelogger.go, it didn't work with my system and I don't yet have the expertise to deal with goroutines, so I couldn't fix it. 
Hence, 'filelogger.go' is a highly simplified version. 
Also, I added a 'multilogger.go' as I needed the output at both console and in a log file.


