# kinesit
This project aims at making it easier to test integrations with Kinesis, 
it contains a docker image that has both [kinesalite](https://github.com/mhart/kinesalite) 
and [dynalite](https://github.com/mhart/dynalite), and a junit rule that can be used in your tests, 
a simple String record processor is also included in the repository, 
I also tried to make it easy to create different processors, 
extend RecordProcessor and override the single method there.

To run a docker container with kinesalite and dynalite:

**docker run -e STREAM_NAME='test-stream' shadi/kinesis-junit-rule**

This will create a container with the stream 'test-stream' ready to receive and send records