# docker-test
## Trying out "Dockerize Airflow" - How to add a docker image

## 1: Make a repo on GitHub (skip if you already have one, like if you forked someone elses repo)
# (covered elsewhere, but remember the link!)

## 2: Get your local workspace ready

    # Create a directory somewhere on your computer. I chose the desktop
        cd Desktop 
        mkdir docker-test

    # Enter the directory and initialize it as a git repo 
        cd docker-test 
        git init 

## 3: Connect your local repo with the repo on GitHub

    # Add your link as the `origin`
    git remote add origin https://github.com/lshawa/docker-test
    
    # Pull down the code that's at your new `origin` 
    git pull origin master 

##5: Create a new folder docker-test:
	# mkdir docker-test
	
	# Create a src folder inside of docker-test:
	
	# mkdir docker-test/src
	
	# Save the Dockerfile inside of the docker-test
	

## 4: Create index.html to create external source 
	
	# Add content to index.html --> Basic "Hello World!"

	# Save index.html inside of src

## 5: Create a Dockerfile 
	# Make sure the file name is capitalized

	# Start from the nginx image--nginx is a modern server
		FROM nginx

	# copy the contents of src to where nginx looks for static files
		COPY src /usr/share/nginx/html

## 6: Navigate into the my_project directory and build the file
	
	# cd my_project

	# docker build myProject .

	# Grab docker container ID 


## 7: Run the docker on port 8080 and then curl 127.0.0.1:8080
	docker run -d -p 8080:80 [containerID]
	curl 127.0.0.1:8080

## 8: Run localhost:8080 on the browser 
	# Expect to see your index.html printed in the terminal


