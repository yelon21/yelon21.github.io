---
layout: post
title: "Yelon's First Blog"
date: 2015-10-27 15:31:47 +0800
comments: true
categories: 
---
#iOS上的图形和动画处理

##1.    绘制字符串

<pre><code>
    UIFont *font = [UIFont systemFontOfSize:10.0];
    UIColor *color = [UIColor redColor];
    [color set];
    [@"112233" drawAtPoint:CGPointMake(0.0, 20.0)
            withAttributes:@{NSFontAttributeName:font,
                             NSForegroundColorAttributeName:[UIColor whiteColor],
                             NSBackgroundColorAttributeName:[UIColor blueColor]}];
    </code></pre>
    
##2.    颜色
<pre><code>
        CGColorRef colorRef = [UIColor blackColor].CGColor;
    
    const CGFloat *components = CGColorGetComponents(colorRef);
    
    NSUInteger componentsCount = CGColorGetNumberOfComponents(colorRef);
    
    for (NSUInteger i = 0; i < componentsCount; i++) {
        
        NSLog(@"%@=%@",@(i),@(components[i]));
    }
</code></pre>
    