Step 2: Why test container
=============

Spring boot project we can take the following advantage which will make integration test easier when we will do integration testing user test container.

###1. Data Access Layer integration test
By using of containerized database instance (i.e. MySQL, PostgreSQL, Oracle database), we can do an integration test easily Data access layer. However, to test the Data Access Layer, we may be required to make some complex setup on our development machine. Additionally, we can customize our containerized database type whenever we need it.
###Application integration test: 
We can do tests in a short-lived test mode with required dependencies such as message queues or web services for our application.
###2. UI/Acceptance test: 
we can conduct automated UI testing by containerized web browsers that are compatible with selenium. It will provide us always a fresh instance of the browser in each test with no browser state, plugin variation, or automated browse up-gradation.

