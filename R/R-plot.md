# 图形参数
par中的设置项
```R
use as follows:
par(opt1=st,opt2=st2,opt3=opt3...)
plot(data, opt1=st, opt2=st2...)
```

## 符号和线条
```R
- pch  # plot char, dot symbol
- cex   #symbols size
- lty   # line type
- lwd   # line width
```
## 顔色
```R
- col.[axis|lab|main|sub] #color
- fg                      # front ground
- bg                        # back ground
```

## 文本属性
```R
- cex.[axis|lab|main|sub]   #scale 
- font[axis|lab|main|sub]   #
- ps                        #pound size
- family                    #font family
```

## 图形尺寸与边界尺寸
```R
- pin #pic size c(w,h)
- mai #margin size in inche
- mar   # margin size in cent
```

# 添加文本、自定义坐标轴和图例
```R
- title()   # title, main and sub
- axis()    # should set axes=FALSE
    side    #side of axis, (1=down, 2=left, 3=up, 4=right)
    at      #where ticks place
    labels  # label of ticks
    pos     # value of corss axis
    lty     # line type
    col     # color
    las     # label postion, 0=parallel, 2=perpendicular 
    tck     #tick length, +number:above the axis, -number:down, 0:no ticks
    ...
- abline()  # 回归线
- legend（location, title, legend）# 图例
- text()
- mtext()

```

# 图形组合
```r
par(mfrow=c(nrows,ncols))

layout(mat)
fig=c(a,b,c,d) #精细控制图形布局
```

