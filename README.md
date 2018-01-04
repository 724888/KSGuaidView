# KSGuaidView
![License MIT](https://go-shields.herokuapp.com/license-MIT-blue.png)
![Pod version](http://img.shields.io/cocoapods/v/KSGuaidView.svg?style=flat)
![Platform info](http://img.shields.io/cocoapods/p/KSGuaidView.svg?style=flat)
***
## 简介

KSGuaidView是APP初次安装或者版本更新时候用了展示新特性的工具。
<br/>

![图一](https://github.com/iCloudys/KSGuaidView/blob/master/Gif/QQ20170531-143315.gif)
![图二](https://github.com/iCloudys/KSGuaidView/blob/master/Gif/QQ20170531-143634.gif)<br/><br/>


## CocoaPods
通过CocoaPods集成

    pod 'KSGuaidView'      

## 使用方法
在AppDelegate 导入头文件
    
    #include <KSGuaidViewManager.h>
 
    - (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {
    
    KSGuaidManager.images = @[[UIImage imageNamed:@"guid01"],
                              [UIImage imageNamed:@"guid02"],
                              [UIImage imageNamed:@"guid03"],
                              [UIImage imageNamed:@"guid04"]];
    
    /*
     方式一:
     
     CGSize size = [UIScreen mainScreen].bounds.size;
     
     KSGuaidManager.dismissButtonImage = [UIImage imageNamed:@"hidden"];
     
     KSGuaidManager.dismissButtonCenter = CGPointMake(size.width / 2, size.height - 80);
     */
    
    //方式二:
    KSGuaidManager.shouldDismissWhenDragging = YES;
    
    [KSGuaidManager begin];
    
    return YES;
}


***
## 注意事项


