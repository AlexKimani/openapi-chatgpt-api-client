## Building the Application
### Logging
- For local deployment, it is available on STDOUT using the format configured in [logback-spring.xml](../src/main/resources/logback-spring.xml)

## Setup Guide
### Requirements

For building and running the application you need:

- [JDK 17](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html)

### **Here is our quickstart guide.**
* Clone the repo
```shell  
git clone git@github.com:AlexKimani/openapi-chatgpt-api-client.git  
```  
* When you attempt to clone the repository, you receive the error message. [Fix – git@github.com : permission denied](https://dev.classmethod.jp/articles/fix-gitgithub-com-permission-denied-publickey-fatal-could-not-read-from-remote-repository/)
* [Install docker](https://docs.docker.com/get-docker/). Ensure that docker is always running.

## Running and testing
* via IDE for local debugging (recommended)
* Run all the required Services on Docker `docker-compose up`.  
  Please follow the troubleshooting section if you are facing any issue
* Start app via IDE (SpringBoot: `com.kimani.chatgptclient.ChatGptClientApplication`). [Not Recommended]
* Build and Test
* `./mvnw clean package`
* Integration tests will use test configs
* Run
* via Docker
* `docker-compose build service-openai`.

### How to test the service
* Run the application via command: `docker compose up`, this will create the ChatGPT Application on docker

### Available Service Endpoints
All endpoints are documented on Swagger API: `{base-url}/swagger-ui.html`
* Create Card: [POST] `{base-url}/v1/openapi/ask`


### Testing the application
* You can run all the unit and integrations tests by running the command `mvn clean test`

### API Testing
* Open the SwaggerUI endpoint: eg `http://localhost:8080/swagger-ui/index.html#/`
* Sample view: ![img.png](img.png)