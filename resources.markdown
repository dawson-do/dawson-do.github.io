---
layout: page
title: Resources
permalink: /resources/
---

## Transportation Software

### Aimsun Scripts

{% highlight python %}
# This script prints the section Id and the section name.

destination_file_path = "C:/Nodes.txt"
file = open( destination_file_path, 'w' )

file.write( "ID,xPos,yPos" )
file.write("\n")

# Iterate over all the nodes in the network.
sectionType = model.getType( "GKNode" )
for types in model.getCatalog().getUsedSubTypesFromType( sectionType ):
	for node in types.values():
		#calculate the coordinates of the centroid of the nodes
		coord = node.getPolygon().centroid()
		xPos = coord.x
		yPos = coord.y
		file.write( "%i,%s,%s" % (node.getId(), xPos, yPos) )
		file.write("\n")
file.close()
print ("Done")
{% endhighlight %}
