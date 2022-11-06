# SimpleLogger-go
## Description
SimpleLogger-go is logger library.

## Usage
Examples:

'''
package main

import (
    "github.com/Hakkadaikon/SimpleLogger-go"
)

func main() {
    var log logger.Logger

    // Level      : LoggerDebug/LoggerInfo/LoggerWarnng/LoggerError
    // OutputType : OutputTypeNormal/OutputTypeJson 
    log.Init(logger.LevelInfo, "./test.log", logger.OutputTypeNormal)

    log.Debug("Debug message")
    log.Info("Info message")
    log.Warning("Warning message")
    log.Error("Error message")

    log.Deinit()
}
'''

Output(OutputTypeNormal):

'''
[2022/11/07 01:13:46] [Info] Info message
[2022/11/07 01:13:46] [Warning] Warning message
[2022/11/07 01:13:46] [Error] Error message
'''

Output(OutputTypeJson):

'''
{"level":"Info","message":"Info message","date":"2022/11/07 01:13:46"}
{"level":"Warning","message":"Warning message","date":"2022/11/07 01:13:46"}
{"level":"Error","message":"Error message","date":"2022/11/07 01:13:46"}
'''

# Author
Hakkadaikon

