[测试网页](https://southbegonia.github.io/UnityWebGLTest.github.io/)

## 为何要做 Unity WebGL 的测试

根本目的是让Unity项目能被 **在线运行**，而不是简单摆个exe或者B站视频

虽然 [itch](https://itch.io/) 也具备发布Unity WebGL 功能，但流程有点复杂哟（~~梯子梯子还是梯子~~）


## 发布及配置流程

 可参阅大佬文章：
 - [Unity 之 发布WebGL并部署到GitHub供外部访问 (Unity | WebGL | GitHub | 内嵌网页） - 陈言必行](https://blog.csdn.net/Czhenya/article/details/119709396)
 
 > 注意：仓库名最好是以 `.github.io` 作后缀
 
 ## 可能遇到的问题
 
 打开测试网页后有如下报错信息：
 ```
 Unable to parse Build/Build.framework.js.gz! 
 This can happen if build compression was enabled but web server hosting the content was misconfigured to not serve the file with HTTP Response Header "Content-Encoding: gzip" present. 
 Check browser Console and Devtools Network tab to debug.
 ```
 
 解决办法是：
 1. 仓库重命名为带 `.github.io` 后缀
 2. 勾选 Unity->Project Setting->Player->WebGL->Publishing settings 中的 Decompression Fallback （原因参阅：[Unity打包WebGL报Unable to parse Build - 刘建杰
](https://blog.csdn.net/qq_34060370/article/details/122168201)
 
