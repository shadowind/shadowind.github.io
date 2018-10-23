---
layout: post
title: "Excel chart"
date: 2014-09-30 23:26:16 -0500
comments: true
categories: viz
---
Here I got a table, several criteria are in Chinese characters, like performance rating etc. I would record a fancier way to viz this in EXCEL, combing line chart with bar chart in vertical direction.
	
|  |Brand A |&nbsp;&nbsp;|Brand B |&nbsp;&nbsp; |Brand C | &nbsp;&nbsp;|Avg 
|--|:--------:||:--------:||:--------:||
|经销店易于搜索，信息明确|82.51||77.71	||72.22	||77.84
|主动提供优惠信息并邀请到店|81.07||	78.39||	74.38||	78.17
|进入经销店后得到充分的关注和指引|	83.30||	80.53||	75.61|	|80.04
|等候被接待的时间	 |81.80	||79.77||	76.27||	79.46
|销售人员礼貌友善，平等对待每位顾客|	86.35||	83.45||	80.20|	|83.54
|销售人员在您未决定购买时能专心接待您|85.53	||82.80||	80.51	||83.13
|展厅内环境轻松舒适|	84.53||	78.58	||75.11	||79.79

This is what it looks like:  
![image](http://i.imgur.com/FyeSgTK.png)  
Step1：在原表后面加两列，一列为Bar，用于做数据的背景色，通过观测数据，最大考虑到数据的取值范围，最大不超过90，所以bar长度设为90；一列为Y轴，用于排版横bar的位置，从最后一行记录为0.5起，每行+1递增  
Add a new column called Bar, as the backgroud bar.  We can observe maxium number in this table is less than 90, so use that as our range. Also add a Y-axis to help disply the value vertically. So it ranging from 0.5 to n+0.5.

| | Brand A  |&nbsp;&nbsp;|Brand B |&nbsp;&nbsp;|Brand C  |&nbsp;&nbsp;|Avg  |&nbsp;&nbsp;&nbsp;&nbsp;|Bar  |&nbsp;&nbsp;&nbsp;|Y axis  |
|-|:----:|--|---|-----|-----|:-----:|
|经销店易于搜索，信息明确|82.51	||77.71	||72.22	||77.84||90.00	||6.5
|主动提供优惠信息并邀请到店|81.07||	78.39||	74.38||	78.17||90.00	||5.5
|进入经销店后得到充分的关注和指引|	83.30||	80.53||	75.61||	80.04||90.00	||4.5
|等候被接待的时间	 |81.80	||79.77||	76.27||	79.46||90.00	||3.5
|销售人员礼貌友善，平等对待每位顾客|	86.35||	83.45||	80.20||	83.54||90.00	||2.5
|销售人员在您未决定购买时能专心接待您|85.53	||82.80||	80.51	||83.13||90.00	||1.5
|展厅内环境轻松舒适|	84.53||	78.58	||75.11	||79.79||90.00	||0.5  
  
Step2：选择插入条形图，可以看到距离我们的目标还是很远的。  
Insert bar chart for all the data.  

![image](http://i.imgur.com/2Wgtxzk.png)

Step3：分别选中图例中A  B  C  整体，单击右键，更改图表类型为带连线的散点图，同时将Y轴和Bar的图例删掉，成功的变成乱糟糟的一坨  
Select A, B, C, right click to change chart type to scatterplot, and delete the legend of Bar and Y axis
![image](http://i.imgur.com/bG07vGh.png)

Step4：重新选择数据，在图表上单击右键，找到”选择数据”，在左侧选择编辑，系列名称不变，X轴系列值选择A列的数值，Y轴选择“Y轴”的数据，重复这个过程至B C 整体列，得到下图  
Reselect the data.  
![image](http://i.imgur.com/f5buNkl.png)
![image](http://i.imgur.com/vPVhK5h.png)

Step5： 调整样式
图基本样式已经做出来了，但是比例尺不对，颜色也非常的艳丽，下面来一点点调整。选中下面的坐标轴，单击右键，找到设置坐标轴格式。在坐标轴选项里可以改变最大值最小值等。选中每根线后可以更改线条粗细、颜色和标记等.  
Modify the apperence.

![image](http://i.imgur.com/q4eSzOV.png)