# coding-project-template

# fullstack_developer_capstone

## Architecture Overview
The final project for this course has several steps that you must complete. The high-level step list given below will help you with an overview of the complete project. The project is divided into smaller labs with detailed instructions for each step. You must complete all labs to complete the project successfully.

## Project breakdown
Fork the GitHub repo containing the project template. The main web application is a predefined Django application. You will need to add some new features, and then build and run your project implementation.

Fork the repository in your account.
Clone the repository in the Cloud IDE environment.
Create static pages to finish the user stories.
Run the application locally.
Add user management to the Django application.

Implement user management using the Django user authentication system and create a REACT frontend.
Implement backend services.

Create Node.js server to manage dealers and reviews using MongoDB and dockerize it.
Deploy sentiment analyzer on Code Engine.
Create Django models and views to manage car model and car make.
Create Django proxy services and views to integrate dealers and reviews together.
Add dynamic pages with Django templates.

Create a page that displays all the dealers.
Create a page that displays reviews for a selected dealer.
Create a page that lets the end user add a review for a selected dealer.
Implement CI/CD, and then run and test your application

Set up continuous integration and delivery for code linting.
Run your application on Cloud IDE.
Test the updated application locally.
Deploy the application on Kubernetes.
Solution architecture
The solution will consist of multiple technologies

The user interacts with the "Dealerships Website", a Django website, through a web browser.

The Django application provides the following microservices for the end user:

get_cars/ - To get the list of cars from
get_dealers/ - To get the list of dealers
get_dealers/:state - To get dealers by state
dealer/:id - To get dealer by id
review/dealer/:id - To get reviews specific to a dealer
add_review/ - To post review about a dealer
The Django application uses SQLite database to store the Car Make and the Car Model data.

The "Dealerships and Reviews Service" is an Express Mongo service running in a Docker container. It provides the following services::

/fetchDealers - To fetch the dealers
/fetchDealer/:id - To fetch the dealer by id
fetchReviews - To fetch all the reviews
fetchReview/dealer/:id - To fetch reviews for a dealer by id
/insertReview - To insert a review
"Dealerships Website" interacts with the "Dealership and Reviews Service" through the "Django Proxy Service" contained within the Django Application.

The "Sentiment Analyzer Service" is deployed on IBM Cloud Code Engine, it provides the following service:

/analyze/:text - To analyze the sentiment of the text passed. It returns positive, negative or neutral.
The "Dealerships Website" consumes the "Sentiment Analyzer Service" to analyze the sentiments of the reviews through the Django Proxy contained within the Django application.


## Project Overview
Project Overview. 
For this Capstone project, you will assume the role of a full stack software developer hired by Best Cars Dealership, a national car dealership with branches all over the US. 

You will create a website that provides a central database of dealership reviews across the country. You will be provided with a project scenario that requires you to develop the website and the required backend services. Ready to see a demo of the website and the various services it will be using? Let's get started. In this project, you will use the following skills to complete the tasks. 

Git, GitHub, and GitHub Actions for version control and continuous integration and continuous delivery or CI/CD. HTML, CSS, and Bootstrap will be used to create a static homepage, About Us page, and Contact Us page for the website. React will be used to create login, registration, dealers view, reviews view and post review components. Python, Django and SQLite for the main application backend for user management and end user views. Python, Flask, and natural language toolkit or NLTK for the sentiment analysis microservice. Node.js, Express, and MongoDB for the dealership and review service. Docker, Kubernetes, Serverless using IBM cloud code engine for deploying various application components and microservices. 
Let us give you a sneak peek of what the application should look like. The screenshots in this video are just an example site. Your implementation might differ from this and the site may look quite different than the screenshots you see in the next few slides. When the users come to the website, they should see the homepage from where they can click About Us, to view the details and description of best cars dealership. And Contact Us, to view the company's contact details. The user should be able to view the branches of the dealership by clicking View Dealership. The user does not need to be logged in to view the dealerships. 

The homepage should also provide options to log in and register. On the homepage, when the user clicks About Us, it should take them to the About Us page, where they can view the details about the company. Such as its mission and values, as well as introduce key members of its leadership team. When the user clicks Contact Us on the homepage, it should take them to the Contact Us page, where they can see the contact details of Best Car Dealership. Including emails, phone numbers, and website. On the homepage, when the user clicks the Register link, they should be taken to the SignUp page. On the SignUp page, the user should have the provision to provide the necessary details and register. 

When the users register, they should automatically get logged in and be taken to the homepage. When the user clicks Login from the homepage, they should see the Login panel. All the registered users should be allowed to login using the Login panel. If the user has not yet registered, they should be allowed to use the link provided to go to the registration page and register. If an unregistered user comes to the homepage and clicks View Dealerships, all the dealerships should be listed, but the Write a review button should not be visible to them. To post a review, the user must be logged in. When the user is logged in, a Write a review option should be available against each dealer to write a review. 

The user should be able to filter the dealerships state-wise, by selecting the desired state from the drop down list. The users should also be able to view reviews of a particular dealership by clicking the name of that dealership. The dealership page should show the reviews for the dealership along with the sentiments. The users who are not logged in should not see the button to post a review, but should be allowed to view all the reviews for the selected dealer. Logged in users should be allowed to post a new review by clicking the Write a review button provided. When the logged in user clicks Write a review, they should see the panel to add the details for the review. They can add the review of the dealership, purchase date, car make, and year of manufacture and then post the review. 

The review added should be reflected on the dealer's specific page, which can be viewed by users. With this, we come to the end of this exemplar demo. Please follow the instructions to complete each task and take screenshots as necessary for final submission. Let's now get started with the project. Before proceeding with the tasks, read the architecture overview to understand the various components of the process. We hope you enjoyed the demo and are looking forward to this Capstone, where you will get the opportunity to build a creative car dealership's reviews website. All the best. 

## Author
IBM

rpal
