### a. How much data your publisher program will send to the message broker in one run?

From the code implementation, the publisher sends 5 data messages that contain a user ID and a name which total up to 5 total user records.

### b. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?

It means they are both connecting to the same RabbitMQ server. If they didnt use the same urls they might not be able to communicate unless those settings still point to the same RabbitMQ server. 

### Terminal images after making a connection with RabbitMQ

![Docker Terminal](images/docker_terminal.png)

![Publisher Terminal](images/publisher_terminal.png)

![Subscriber Terminal](images/subscriber_terminal.png)

### RabbitMQ after running publisher twice

![Spikes in RabbitMQ](images/spike_website.png)

The monitoring chart shows only two visible purple spikes and no yellow spikes, indicating that two messages were successfully delivered to and acknowledged by the consumer. This confirms that the subscriber received and processed them. The lack of yellow spikes implies that either very few messages were published or the publishing activity wasn't recorded within the chart's displayed time range.