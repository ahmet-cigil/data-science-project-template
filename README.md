# Data Science Project Template

Youtube instructions:

ENG: https://youtu.be/pTk82vkhsMc  
RUS: https://youtu.be/xf58pNYhRss

My Summary:
How to use Data Science Template from Github:
mkdir /project
cd /project
open /project in VS Code
git init
git pull https://github.com/glebmikha/data-science-project-template.git
Add your favorite Python modules to ./docker/jupyter/requirements.txt. For example:
	xgboost
	tensorflow==1.6.0
docker-compose up
A jupyter notebook link will be created fully embedded conda etc.
Stop containers
	docker-compose down
Update images
	docker-compose build --pull
Clean Docker's mess
	docker rmi -f $(docker images -qf dangling=true)
Sometimes it is useful to remove all docker's data.
	docker system prune

From the Github Owner:

This repo is inspired by the <a href="https://www.amazon.com/Docker-Data-Science-Extensible-Infrastructure/dp/1484230116" target="_blank">Docker for Datascience book</a>. It's a Docker image with a data science environment based on the <a href="https://hub.docker.com/r/jupyter/datascience-notebook/" target="_blank">jupyter/datascience-notebook </a>with pandas, matplotlib, scipy, seaborn and scikit-learn pre-installed.

## To start new Data Science project:

1. Copy this repo

Create a new directory, cd into it, and then run

```
git init
git pull https://github.com/glebmikha/data-science-project-template.git
```

Or you can just download it as a zip and use it without git.

2. Add your favorite Python modules to ./docker/jupyter/requirements.txt. For example:

```
xgboost
tensorflow==1.6.0
```

Or use pip install right in jupyter (don't forget ! in front of the command)

```
!pip install your_package
```

3. Start containers

```
docker-compose up
```

4. Copy a jupyter url from terminal and open it in your browser.

5. Find an examples.ipynb notebook in ipynb folder. Create your notebooks.
6. Copy your data into ./data and read it in Jupyter. You can also upload data into PostgreSQL, which is running in it's own container along with Jupyter (see examples notebook for details)
7. Stop containers

```
docker-compose down
```

8. Update images
```
docker-compose build --pull
```

9. Clean Docker's mess

```
docker rmi -f $(docker images -qf dangling=true)
```

Sometimes it is useful to remove all docker's data.

```
docker system prune
```
