---
layout: post
title: "Netezza 学习笔记"
description: "这篇是Netezza学习笔记"
category: netezza
tags: [netezza]
---
{% include JB/setup %}



I was also searching for this thing when I was trying to parse a very large XML file. I was trying to parse a file whose size was in GB. And whenever I start my python script, it just gets killed everytime. Then I came across some scholarly article written on efficiently parsing XML files. 

## Tips

_V_QRYHIST view provides access to latest 2000 plan files.


## Query
Code :
SELECT
FROM
SYSTEM .ADMIN._V_QRYHIST q
WHERE
QH_USER = 'ADMIN'
ORDER BY QH_TSUBMIT DESC;


[Link](http://planet.openstreetmap.org/) 


And then you are done. You have all the important information you need out of the OSM data and that too in a fast way. If you wanna get more and more faster you can make the program multithreaded.
	
