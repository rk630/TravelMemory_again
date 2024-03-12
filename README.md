## Travel Memory

- The TravelMemory application has been developed using the MERN stack. The application consists of frontend & backend which are developed using JavaScript programming language.

### Objectives :
- Set up the backend running on Node.js.
- Configure the front end designed with React.
- Ensure efficient communication between the front end and back end.
- Deploy the full application on an EC2 instance.
- Facilitate load balancing by creating multiple instances of the application.
- Connect a custom domain through Cloudflare.
### Backend Configuration
- Access the complete codebase of TravelMemory Application from the GitHub link. https://github.com/UnpredictablePrashant/TravelMemory
- Clone the complete repository and navigate to the backend directory of the TravelMemory application.
- Make the necessary changes into the codebase as mentioned in the README.md file in the repository.

![image](https://github.com/rk630/TravelMemory_again/assets/139606316/423237e5-2d32-45d4-ac2d-aac1d3b1c743)
- Update the .env file in the backend directory of the application to incorporate with the database connection details and port information.
- To connect the backend with the database utilize Mongo DB compass and enter the Mongo DB URL and the port number in the .env file.
- Configure the backend to run on PORT=3000 and set up the reverse proxy by installing Nginx and run it on PORT=80.
- To set up the reverse proxy make the necessary changes in the /etc/nginx/sites-available/default file with the details of the subdomain and the proxy_pass = http://webserver.
- ![Screenshot 2024-02-02 125003](https://github.com/rk630/TravelMemory_again/assets/139606316/3594e4ae-cf12-4d4d-8a4f-59861b5b69c2)

- ![Screenshot 2024-02-15 154818](https://github.com/rk630/TravelMemory_again/assets/139606316/072eb6b5-db8e-4655-bb7c-2d743a828459)
### Frontend And Backend Connection
- Navigate to the frontend directory of the application and in the url.js file update it with the subdomain of the backend application.
- Also make the necessary changes in the package.json file, so that the frontend application runs on the preferred port number when the servers are up.
- Follow the same steps for the reverse proxy setup as done in the backend application.
- ![Screenshot 2024-02-01 170537](https://github.com/rk630/TravelMemory_again/assets/139606316/ea156444-138c-4f79-a64c-a3abdf521632)
![Screenshot 2024-02-02 122158](https://github.com/rk630/TravelMemory_again/assets/139606316/7b3870b1-45a4-407c-91be-5c6ade18ed4f)
![Screenshot 2024-02-01 183316](https://github.com/rk630/TravelMemory_again/assets/139606316/f09e103d-fd82-4cba-a3c1-c9cfc53e4483)
![Screenshot (27)](https://github.com/rk630/TravelMemory_again/assets/139606316/304a5e8f-484c-458c-82be-5f815c254699)

- If the reverse proxy setup for the frontend is done successfully, this is how the frontend application with the subdomain looks.
![Screenshot (28)](https://github.com/rk630/TravelMemory_again/assets/139606316/53831179-2088-4493-be12-0082a86f3041)
### Scaling the Application
To scale the application, we need to create multiple instances with the same configurations by creating the snapshots of the frontend and backend application.
We need to create the AMI and launch new instances using the AMI.

We need to create a load balancer to ensure the efficiency of incoming traffic.
Create the application load balancers by specifying the instances into their respective target groups.


### Domain Setup with CloudFlare
Connect your custom domain to the application using Cloudflare.
Create a CNAME record pointing to the load balancer endpoint of the backend.
Create an A record with the IP address of the EC2 instance hosting the frontend.


### Successful Deployment

