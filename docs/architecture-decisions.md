## Decisions Justifications
__Justifications Message Passing Strategy__

1. Event Location Microservice will process user location coordinates, this message communication is using gRPC. This decision was made cause of the project requirements, a lot of users sending data continuously, and how the communication is woth kafkka directly and not another service used by users its much better and has better performance when internal services used gRPC.

---

2. Event Location microservices has a Kafka cluster that receives location data that is consumed by the Processing Location Microservice. This data is stored in the postresql DB for Location data.

---

3. Location service interacts through the communication of a RESTFul API with the Reactt frontend.

---

4. Person microservice has the communication of a RESTFul API this microservice keeps user data.

---

5. Location service gets data from the Person Microservice when there is a request about a new connection.
