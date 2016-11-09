# Parallel Test Execution

## Pre-requisites

In order to run parallel tests, you will need to create multiple runner classes. Each runner class points to a portion of the tests
that are partitioned either by tags or features. 

Then specify the number of threads to run in parallel. This is provided by the maxParallelForks property in build.gradle. 
The max number of maxParallelForks should be less or equal to the number of runner classes. 

## Running the tests

To run the test, execute the following command that creates four threads to run the tests partitioned by the runner classes in parallel.

`gradle clean test aggregate -DmaxParallelForks=4`
