---
layout:     post
title:      "ImageMagick Usage"
subtitle:   " \"图片处理的小魔法\""
date:       2018-07-07 12:00:00
author:     "247RPA"
header-img: "img/in-post/imagemagick_pic_1.png"
catalog: true
tags:
    - Image Processing
---

#### Image magick 

**Magick 脚本用于图片处理非常高效有用**
在RPA的过程中有很大机会需要进行图片文本信息提取的操作，这时候通常使用OCR（光学字符识别）技术，但OCR作为一种较为成熟的识别技术并不是无所不能的，甚至有时候识别率会让人及其失望，尽管目前很多OCR厂商都宣称其识别已增强了Machine Learning(机器学习)算法和其他AI人工智能算法。随着识别技术越来越好，但不可否认的是一张高质量的源图片是及其重要的！理想情况下，源图片的字符越是清晰可见越是能被识别出来。 

基于这种设定，那么在我们进行OCR之前，我们有必要对图片进行优化调整的处理，在机器学习中被称为 **pre-pocessing**
那么Image magick在OCR中可以提供哪方面的帮助呢？
* 调整色阶
> * 色阶： 色阶是表示图像亮度强弱的指数标准，也就是我们说的色彩指数，在数字图像处理教程中，指的是灰度分辨率（又称为灰度级分辨率或者幅度分辨率）。图像的色彩丰满度和精细度是由色阶决定的。色阶指亮度，和颜色无关，但最亮的只有白色，最不亮的只有黑色。
> * 为什么是色阶？经验告诉我们，通过让要识别的字符与背景区分开来，通过调整色阶可以让黑更黑，让白更白，那字符是更加凸显的。
好，现在直接贴脚本代码：
```
 #magick source_pic  -level a,b  result_pic
  magick test.png  -level 35%,75%  test_level.png
```
Tip: 当a值变大时，图片变黑； 当b值变小，则图片变白。

* 去掉指定颜色

* 抹掉线条

* 图片合成及修改图片尺寸





