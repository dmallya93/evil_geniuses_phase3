
The Source code has a code called org.datasyslab.geospark.spatialOperator.SpatialStatistics2

which does the work of computing the spatial statistics. The method signature for the function doing spatial statistics is,

public static void SpatialStatistics(JavaSparkContext sc, String InputLocation,String outFile)

We can import this jar and do computations as required.
We assume that the input CSV has data headers and ignore the first line of the while reading from the input file. 

To run from jar file,

Run the following command, changing the input file and output directory.

./spark-submit --class org.dds.mainpack.MainClass /JAR_PATH/geospark-0.5.2.jar /INPUT_DATA_PATH/yellow.csv  /OUTPUT_FILE_PATH/out.txt

The result CSV file is generated. The output is as follows:
Cell_x, Cell_y, time_step, zscore

Assumptions:
We assume Hadoop server is up and running and we are loading data in the following address to load data into Hadoop cluster

the address is hdfs://master:54310/data.csv