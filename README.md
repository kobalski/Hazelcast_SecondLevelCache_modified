Hazelcast_SecondLevelCache_modified
===================================

#4017 issue of hazelcast reproduced.
In order to reproduce the issue on Linux or Mac easily,

1) Run the build-script <br>
2) Run the start-db script in order to start Derby inside project <br>
3) Run the create-db script to create a db to work on derby <br>
4) Run the run-script twice and create two hazelcast instance, when second one 
   starts you can see the exception on the first cluster <br>
   
   
The issue arises when you use Long for version in Product which is the child entity for Supplier 

