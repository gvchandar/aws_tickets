# AWS Tickets
AWS Ticket repo lists common issues and tickets reported in a live enviornment 
  - Common live issues are reported and demonstrated with the fix
  - Recommendation and suggestions are welcome by  submitting a PR
  - Magic starts now

# Prerequistes!
  - Create an AWS accout
  - Install AWS shell and configure the access
 
You can also:
  - Suggest some idess 

Markdown is a lightweight markup language based on the formatting conventions that people naturally use in email.  As [Bala Govindarjan] writes on the [Markdown site][df1]

> The goal of this page is
> to report common production and live issues 
> with as much details as possible. 

This text you see here is *actually* written in Markdown! To get a feel for Markdown's syntax, type some text into the left window and watch the results in  the right.

### Tech

This demo uses number of open source projects to work properly:

* [HA Proxy] - HA Proxy server!
* [K8S] - Kubernetes
* [NGINX](https://www.nginx.com/) - Lightweight server
* [jQuery] - duh


### Installation

Install AWS Shell by following the link and make sure you can run basic AWS commands afterwards
https://github.com/awslabs/aws-shell.

```sh
$ aws-shell
aws> configure
Enter AWS access , secret key and default region
aws>ec2 describe-regions
aws>ec2 describe-instances
```

### Plugins

The below plugins will be used as need arises 

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md][PlDb] |
| Github | [plugins/github/README.md][PlGh] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Medium | [plugins/medium/README.md][PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |


### Development

Want to contribute? Great!
Clone the repo and make changes and raise a pull request

 
Open your favorite Terminal and run these commands.

First Tab:
```sh
$ git clone repo
``` 
Create a branch and make the changes :
```sh
$ git checkout -b Changes_To_Improve

Make the changes
```
Push the changes :
```sh
$  git push origin
And then raise a pull request to merge with the master 
```
### Docker build 
Pushing the changes in docker image and applying them 
```sh
cd 
docker build -t bgovinda/aws_tickets:${packag e.json.version} .
```
This will create the bgovinda image and pull in the necessary dependencies

Once done, run the Docker image and map the port to whatever you wish on your host. In this example, we simply map port 8000 of the host to port 8080 of the Docker (or whatever port was exposed in the Dockerfile):

```sh
docker run -d -p 8000:8080 --restart="always" <youruser>/bgovinda:${package.json.version}
```

Verify the deployment by navigating to your server address in your preferred browser.

```sh
127.0.0.1:8000
```

#### Kubernetes + Google Cloud 

See [KUBERNETES.md](https://github.com/joemccann/dillinger/blob/master/KUBERNETES.md)


### Todos
 - Write MORE Tests
 - Add Night Mode


