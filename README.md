Hazelcast_SecondLevelCache_modified
===================================

Issue 4017 of hazelcast reproduced.
In order to reproduce the issue on Linux or Mac easily,

1) Run the build-script <br>
2) Run the start-db script in order to start Derby inside project <br>
3) Run the create-db script to create a db to work on derby <br>
4) Run the run-script twice and create two hazelcast instance, when second one 
   starts you can see the exception on the first node on cluster <br>
   
 <br> <br>
   The issue arises when you use Long for version in Product which is the child entity for Supplier. If version is null Hibernate ComparableComparator method throws null poiner exception when onMessage method of MessageListener in LocalRegion cache class in Hazelcast Hibernate 4. There is an issue on hibernate jira about this issue, but its status seems to be rejected, they think it is not a bug.<br>
https://hibernate.atlassian.net/browse/HHH-1866

  
