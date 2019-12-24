# apache_storm_demo_program

# SpoutOutputCollector

In one terminal, start the nimbus server.
./bin/storm nimbus

In another terminal, start the supervisor.
./bin/storm supervisor

In the 3rd terminal, start the Storm Web UI.
./bin/storm ui
The above command will start the Storm UI. You can visit
http://localhost:8080/index.html
to view the Storm cluster.
Run the example WordCount¶
Now open another terminal to run the Storm example WordCount.

mvn clean install
This will build the jar file inside target folder.
cd ../storm
./bin/storm jar ../../examples/storm-example/target/storm-example-1.0-jar-with-dependencies.jar admicloud.storm.wordcount.WordCountTopology WordCount

To kill the topology, use the following command:
./bin/storm kill WordCount
