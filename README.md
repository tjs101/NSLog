# NSLog
项目使用NSLog

    #if DEBUG
    #define NSLog(format, ...) NSLog(@"\n✅文件: %@ \n方法: %s \n内容: %@ \n行数: %d", [[[NSString stringWithFormat:@"%s",__FILE__] componentsSeparatedByString:@"/"] lastObject],  __FUNCTION__, [NSString stringWithFormat:format, ##__VA_ARGS__], __LINE__);
    #define NSLogWarning(format, ...) NSLog(@"\n⚠️文件: %@ \n方法: %s \n内容: %@ \n行数: %d", [[[NSString stringWithFormat:@"%s",__FILE__] componentsSeparatedByString:@"/"] lastObject],  __FUNCTION__, [NSString stringWithFormat:format, ##__VA_ARGS__], __LINE__);
    #define NSLogError(format, ...) NSLog(@"\n❌文件: %@ \n方法: %s \n内容: %@ \n行数: %d", [[[NSString stringWithFormat:@"%s",__FILE__] componentsSeparatedByString:@"/"] lastObject],  __FUNCTION__, [NSString stringWithFormat:format, ##__VA_ARGS__], __LINE__);
    #else
    #define NSLog(format,...)
    #define NSLogWarning(format, ...)
    #define NSLogError(format, ...)
    #endif
