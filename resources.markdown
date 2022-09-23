---
layout: page
title: Resources
permalink: /resources/
---
## Notebooks

### Demos

WIP

## Transportation Software

### Aimsun Scripts

A WIP collection of (trivial and non-trivial) scripts I have written that help me run research experiments.

{% highlight python %}
# This script exports the ID and positions of all nodes in the network.

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

{% highlight python %}
destination_file_path = "C:/Users/dawso/Desktop/Sections.txt"
file = open( destination_file_path, 'w' )

file.write( "Id,O_id,D_id" )
file.write("\n")

# Iterate over all the sections in the network.
sectionType = model.getType( "GKSection" )
for types in model.getCatalog().getUsedSubTypesFromType( sectionType ):
	for section in types.values():
		# find the origin and destination of each section
		orig = section.getOrigin()
		dest = section.getDestination()

		# cases for sections on the edge of the network
		if orig is None:
			origId = -1
		else:
			origId = orig.getId()

		if dest is None:
			destId = -1
		else:
			destId = dest.getId()

		file.write( "%i,%i,%i" % (section.getId(), origId, destId))
		file.write("\n")
file.close()
print ("Done")
{% endhighlight %}
