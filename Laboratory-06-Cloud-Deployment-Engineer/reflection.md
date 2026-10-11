# Mission Reflection

Writing a docker-compose.yml file makes a cloud engineer's job easier because the entire deployment is defined in one place instead of in many long commands. With docker run, I would have to type the image, ports, and environment variables for each container by hand, and one typo could break the setup. With Compose, I wrote the configuration once and started both containers with a single command. The file can also be saved in GitHub, reused, and reviewed, which is the main idea behind Infrastructure as Code.

If I make an indentation error in a YAML file, such as using a Tab instead of spaces, Docker Compose cannot read the file correctly. YAML relies on spaces to show which settings belong under which service, so the deployment fails with a parsing error until the indentation is fixed.

We used environment variables like MYSQL_PASSWORD, MYSQL_DATABASE, and MYSQL_USER so the containers can be configured without changing the images themselves. They allow the database to create the correct user and database, and they tell Nextcloud how to connect to it. They also make it easy to change values for different environments. In a real production setup, sensitive values like passwords should be stored in secrets or .env files instead of being written directly in the Compose file.

Deploying Nextcloud in just a few minutes felt surprising and exciting. I expected a full private cloud storage system to take a long time to install and configure, but Docker Compose did most of the work after I typed one command. It made me realize how powerful automation is in cloud computing.

Since Mission 1, my understanding of cloud computing has grown from simply knowing the definitions to actually deploying and managing real services. I started with basic concepts and cloud providers, then learned containers, storage, and now multi-container deployment. I now see cloud computing as something I can build and automate, not only something I use.
