# DesignDiagramForUnitConverter
This is a repository which would be hoding all the design documents for the problem as mentioned below:
Some Arbitrary System

Functional Requirement:
-----------------------


As a lazy fellow, I need to create a distance conversion utility.

This utility will take a number and two units, source unit and target unit(this is optional).

For e.g I can pass 1000, meter and kilometer, then the utility should return 1 KM.

If I dont pass a target unit, then the utility should intelligently simply the representation by interpreting the input.

For e.g I can pass 9,460,730,472,581 , kilometer and no target unit. The system should intelligently interpret that
the most simplest way this can be expressed is 1 light year and return that as result.

Initially we should support input units as meter, kilometer, centimeter,light year and resulting units as meter, km, cm, light year.

Non Functional Requirement
==========================

Every calculation should be completed within 50ms.(best time)

System should support additional units without need for deployments.

System should charge every calculation request at the rate of 1 bit coin per request and generate an invoice (Payment handling is not in scope).
We need to simply keep track of which user account made how many requests.Initially invoices can be stored in memory (no DB needed).

For every request that is received and failed, system should impose a fine on itself and deduct 1 bit coin from invoice for that user and
apologize to the user.

Every user should be authenticated using basic auth (user name passwd)

Unit tests are expected.

In case of increase in traffic, system should be able to handle multiple requests from multiple users without impacting
performance.

Consider startup with 2 users and scaling ability upto 200000 users.

