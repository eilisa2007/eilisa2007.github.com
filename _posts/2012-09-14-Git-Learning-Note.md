---
layout: post
title: "Git 学习笔记"
description: "这篇是Git学习笔记"
category: git
tags: [git]
---
{% include JB/setup %}

Git是Linux下的个版本控制软件。 

I was also searching for this thing when I was trying to parse a very large XML file. I was trying to parse a file whose size was in GB. And whenever I start my python script, it just gets killed everytime. Then I came across some scholarly article written on efficiently parsing XML files. 

## Concept



## Approach





[here](http://planet.openstreetmap.org/) 
Code :

	from lxml import etree
	
	context = etree.iterparse(filename, events=('end',), tag='node')
	
	for event, elem in context:
		Id=elem.attrib['id']	
		lat=str(elem.attrib['lat'])
		lng=str(elem.attrib['lon'])

		for c in elem:
			if c.attrib['k']=='created_by' or c.attrib['k']=='source': # We don't want such tags to keep in our DB.
				continue
			
			key=c.attrib['k']	#These are basically the tags inside the nodes having key and values
			val=c.attrib['v']
			# You can do more filtering here if you want specific keys or values. Like if you want only 'atms' then filter the val with 'atm' using conditions.
			
			# Store the information in file or db or wherever you wanna use it.
			


    	elem.clear()

   	while elem.getprevious() is not None:
        	del elem.getparent()[0]



And then you are done. You have all the important information you need out of the OSM data and that too in a fast way. If you wanna get more and more faster you can make the program multithreaded.
	
