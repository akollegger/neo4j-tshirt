Neo4j T-Shirts
==============

Neo4j topples the square stacks of uniform records, recognizing the unique character
of individual data and the value in relationships among them. Naturally, when considering
a t-shirt for our community, we wanted to acknowledge each person who would wear one,
and how they are related to Neo4j.

Simple. We'll create a social graph of t-shirts. To become part of the social graph, 
someone already connected just has to acknowledge that they KNOW you. If that person
is authorized to grant shirts, we'll print up a personalized Neo4j T-Shirt commemorating
the acknowledgement.

You may not know which mug is yours, but your shirt will be unmistakeable.

Singin'

    This shirt is my shirt, that shirt is your shirt, 
    from California to the British Island
    From the Swedish Forest to Mediterranean waters
    This shirt was made for you from me

How this all works
------------------
The shirts mark members of a social network. The network starts with Neo4j's founders, then ripples out.
The founders are the only people with automomatic shirt granting powers. They also have the 
ability to promote other members to become shirt-granters. 

See the
[t-shirt model](https://github.com/akollegger/neo4j-tshirt/wiki/T-Shirt-Model) for details


*NOTE*: for now, this is managed through a manual process. Just send an email to
andreas@neotechnology.com with the details about who you want to grant a shirt
and your choice of shirt design (color, graphics, message). 

The lab-day (Saturday-night) project will eventually support...

*Acknowledge a graphista*:

1. Tweet "@graphista paints a pretty picture #neo4j #tshirt #ack"
   - prefer to phrase as if talking about, rather than to, them
2. This will create a KNOWS relationship in the graph, annotated with the tweet

*Granting a T-Shirt to a graphista*:

1. Tweet "@graphista is a Bobby Fischer of graph-like thinking #neo4j #tshirt #grant"
2. This will create a `KNOWS` relationship in the graph, annotated with the tweet
3. Also, a `GRANTS` relationship will be created to indicate that the graphista gets a shirt
4. Production of the t-shirt is a devoted, hand-crafted process (see below)

*Promote a graphista*:

1. Tweet "@graphista should spread the love #neo4j #tshirt #promote 10"
2. This will create a `CAN_GRANT_SHIRTS` auth relationship to the graphista
  - annotated with a `allocation=10` property indicating how many shirts they can give out


Creating a shirt
----------------
Every shirt is a custom, one-of-a-kind. 

The shirt shepherd will work with the grantor to select a shirt, get sizing, and choose
or design a shirt just for that recipient. 

Like so:

1. Shirt shepherd receives notification about grant
2. Shepherd contact grantor to figure out the details
3. (optional) Grantor designs a shirt
4. Shepherd orders shirt, gets it delivered to recipient

Designing a shirt
-----------------
We have some basic designs of shirt, from which a grantor may choose. You can check
out the [mock-ups](https://github.com/akollegger/neo4j-tshirt/wiki/T-Shirt-Examples) for
some pret-a-porter shirts, or design your own. 

Design whatever you'd like, however you must include these common elements:

1. Placement of the quoted tweet
  - this is the essential first-order relationship within the graph
2. A Neo4j logo somewhere
  - perhaps a mini-logo on the neckline
3. Cypher query on the hemline with terms that bind the person into the graph
  - position and size are fixed, but you can decide on the query
4. Single-color (for now) graphics
5. Shirt color & style

Recommended, but not required, is to use common elements derived from our logo. There is
an [OmniGraffle Stencil](https://github.com/akollegger/neo4j-tshirt/downloads) available
which makes it easy to play with ideas. Also in the 
[downloads area](https://github.com/akollegger/neo4j-tshirt/downloads), you'll find eps 
outlines of the logo, node and relationships which provide stylistically consistent building-blocks. 

Have fun!

