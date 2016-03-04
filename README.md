

### MAHUDTool 

`MISSAJJ`自己写的一个基于`MBProgressHUD`为内核的HUD工具类 



###更新日期


更新日期: 16-03-04 13:03:43

上传MAHUDTool



###前言



午后的阳光，

惊艳了时光，明媚了岁月……

那些镌刻在心底的心心念念，

婉约在文字里，书写在回忆里……


花儿开的那一刻，

不去追离开的，不等待承诺中会来的，

只把握现在的那一抹暖暖的阳光……



面朝阳光，春暖花开，约吗？[偷笑]


_____________MISSAJJ on 16/3/4.




###Why?为什么要写这个工具类？


用代码分层的理念和方案，将HUD提示框单独抽出一个单例工具类`MAHUDTool`,用于调用`MBProgressHUD`显示提示框，后期如果项目需要换SVProgressHUD,JGProgressHUD等其他HUD,就只需要在这个工具类里改写和调试，不用在整个项目里批量寻找再一段一段改写代码了，提高了效率。
  
  


###Void＃请求方法################################################

```objective-c

//显示HUD
- (void)showHUDInView: (UIView *)view withString:(NSString *)string;

//隐藏HUD
- (void)hideHUD;

```

###Void＃使用方法################################################


```objective-c

//显示HUD  如果设置view=nil,默认会将HUD创建在window
[[MAHUDTool sharedMAHUDTool]showHUDInView:nil withString:@"努力加载中..."];

//显示HUD  如果设置view,将HUD创建在self.view 
[[MAHUDTool sharedMAHUDTool]showHUDInView:self.view withString:@"努力加载中..."];

//隐藏HUD 
[[MAHUDTool sharedMAHUDTool]hideHUD];

```


###Other其他
 

很希望能和大咖们一起快乐地奔跑,不再是一个孤独的攻城狮，
希望能有更多的狮子一起共勉探讨学习，共同进步！

我的联系方式 ： QQ   996174446  ［验证：IOS攻城狮］
