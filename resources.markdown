---
layout: page
title: Resources
permalink: /resources/
---
### Notebooks

#### Demos

[FD_demo.ipynb][fd_demo]: Basic 1D finite volume method simulation showing the effect of different Fundamental Diagrams (FD) on traffic waves

### Transportation Software

#### Aimsun Scripts

A WIP collection of (simple and non-simple) scripts I have written to help me run research experiments.

<details>
	<summary>Export the ID and positions of all nodes in the network.</summary>

	{% highlight python %}
destination_file_path = "C:/Nodes.txt"
file = open( destination_file_path, 'w' )

file.write( "ID,xPos,yPos" )
file.write("\n")

# Iterate over all the nodes in the network.
sectionType = model.getType( "GKNode" )
for types in model.getCatalog().getUsedSubTypesFromType( sectionType ):
	for node in types.values():
		coord = node.getPolygon().centroid()
		xPos = coord.x
		yPos = coord.y
		file.write( "%i,%s,%s" % (node.getId(), xPos, yPos) )
		file.write("\n")
file.close()
print ("Done")
	{% endhighlight %}
</details>

<details>
	<summary>Export the ID of all sections, and the ID of Origin and Destination nodes</summary>

	{% highlight python %}
destination_file_path = "C:/Sections.txt"
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
</details>

[fd_demo]: https://nbviewer.org/github/dawson-do/notebook-demos/blob/master/FD_demo.ipynb
