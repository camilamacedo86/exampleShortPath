#############################################################################
#                       About Solution                                     #
#############################################################################

This is a solution for finding the shortest path between points using a graph 
database (Neo4J) with Meteor JS.

#############################################################################
#                   Installation and Configuration                          #
#############################################################################

Observation : The following commands are using the Apple operating system, but you can perform the same procedure on any other operating system.

# Install the meteor JS

Command Line: $ curl https://install.meteor.com/ | sh

About how to install Meteor JS : [https://www.meteor.com/install](https://www.meteor.com/install)

# Install Neo4J

Command Line: $ brew install neo4j

About how to install Neo4J : [http://neo4j.com/developer/get-started/](http://neo4j.com/developer/get-started/)

# Configuring Neo4J

Command Line: $ neo4j start

In your browser : http://localhost:7474/

Set the password : teste

The project is set to run on the user Neo4j and password test
( http://neo4j:teste@localhost:7474 )


# Clone this project:

$ git clone https://camilamacedo@bitbucket.org/camilamacedo/shortpath.git


# StartUP :

Go to the root folder of the project and run:

$ meteor

Ready to default port 3000. Therefore the application is running at http://localhost:3000/

########################################################################
#                        API REST                                     #
########################################################################

### To register points:

http://localhost:3000/api/create/locations/origin/{origin}/destination/{destination}/distance/{destination}

{origin} = Origin point
{destination} = Destination point
{distance} = KM distance from one point to another

Call example :

http://localhost:3000/api/create/locations/origin/A/destination/B/distance/10

### To find the smallest route and the amount that will be charged:

http://localhost:3000/api/short/location/origin/{origin}/destination/{destination}/autonomy/{autonomy}/price/{price}

{origin} = Origin point
{destination} = Destination point
{autonomy} = KM distance from one point to another
{price} = Value Charge

Call example :

http://localhost:3000/api/short/location/origin/A/destination/B/autonomy/10/price/200.50

### To clean the database:

http://localhost:3000/api/clear/locations