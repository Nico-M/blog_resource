---
title: markdown之图表
date: 2018-01-25 10:34:18
tags: markdown
typora-root-url: ..
---

{% note primary %} [Typora](https://typora.io) 这个软件真心 **太好用** 了,像我这么不喜欢写作的人都觉得这款软件十分的方便.不由得让我想要多多的利用好这款app了.  {% endnote %}

之前用的时候一直有种感觉是,启动反应时间有点长,最近貌似进行过比较大的改版,启动速度更快了,而且还加入了新的图表功能.今天,就做一下{% label primary@图表 %}怎么用的笔记吧! ![img](/images/typora.png)

<!--more--> 

## flow

这个应该是 流程图 吧,个人感觉还是蛮有用的.

先介绍格式,当当当...

```
//新定义 st:开始  e:结束  
st=>start: Start
op=>operation: Your Operation
cond=>condition: Yes or No?
e=>end

//注意按照顺序,条件判断
st->op(right)->cond
cond(yes)->e
cond(no)->op
```

```flow
st=>start: Start
op=>operation: Your Operation
cond=>condition: Yes or No?
e=>end

st->op(right)->cond
cond(yes)->e
cond(no)->op
```



## sequence

这个叫什么来着也不知道,就是觉得有用,先备着再说

```
//适合描述通讯   ->> 实线  -->>虚线
alice->>joun: hello,how are you
joun-->>alice: grea
```

 ```sequence
alice->>joun: hello,how are you
joun-->>alice: grea
 ```

## 其他

今天也学了不少新东西,第一个就是内建标签,就是开头的这个,详细可以参考 [内建标签](https://almostover.ru/2016-01/hexo-theme-next-test/#) 

![ ](/images/callout.png)

```
//class为boostrap的几个属性 primary default success danger info
//里面内容可以用Markown格式
{% note class %}
内容
{% endnote %}
```

另一个是标签label,可以给字体表色: {% label primary@红色 %}

```
//class同上
{% label class@content %}
```

另外对于给字体上色,typora还有特殊的办法 `$\color{red}{red}$` 这样就会显示为红色字.  

## <mark>标记</mark>

```
//标记
<mark>esse</mark>
```


...先记录这么多吧,未完待续!