# GPUImage滤镜实现分析


- 原图

  ![原图](https://huang-typora-image-1257956766.cos.ap-chengdu.myqcloud.com/blog/GPUImageFiltersAnalyse/origin.png)
  
- 前言

  本文主要学习GPUImage滤镜算法，并进行实践。网上有很多介绍GPUImage的文章，这里就不再赘述。GPUImage内置100多种滤镜，其中有简单的，也有复杂的。为了节约大家的阅读时间，简单的滤镜只介绍原理，不放效果图；如果大家对着色器编程感兴趣，推荐大家去[ShaderToy](https://www.shadertoy.com/)这个网站(能快速的预览渲染效果)。因为实践是在ShaderToy上进行的，这里简单介绍一下一些内置变量和内置函数。
   
   - 内置变量:
   
     >`fragCoord`:二维变量，表示画布的宽高;`iResolution`:二维常量，也表示画布的宽高。`texture(通道，纹理坐标)`函数:读取通道中的纹理，类似GLSL中的`sample2D`函数。
  - 内置函数:
  
     > `length(x)`:获取向量x的模长;
     




