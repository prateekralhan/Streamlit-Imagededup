# 🗣 Imagededup - Streamlit based Web App 🚀 [![Project Status: Active](https://www.repostatus.org/badges/latest/active.svg)](https://www.repostatus.org/#active) [![](https://img.shields.io/badge/Prateek-Ralhan-brightgreen.svg?colorB=ff0000)](https://prateekralhan.github.io/)

A simple streamlit based web application in order to find duplicates in a corpus of images using perceptual hashing, uploaded by the user.

![demo](https://user-images.githubusercontent.com/29462447/203412429-ebdcc031-dd6e-4f32-87df-69f1931d75e1.gif)


## Installation:
* Simply run the command ***pip install -r requirements.txt*** in order to install the necessary dependencies.

## Usage:
1. Clone this repository in your favourite directory.
2. Simply run the command: 
```
streamlit run app.py
```
3. Navigate to http://localhost:8501 in your web-browser. This will launch the web app :

![1](https://user-images.githubusercontent.com/29462447/203628192-337df35e-012a-49c6-99c0-e9de43c70d5f.png)


4. By default, streamlit allows us to upload files of **max. 200MB**. If you want to have more size for uploading images, execute the command :
```
streamlit run app.py --server.maxUploadSize=1028
```

### Running the Dockerized App
1. Ensure you have Docker Installed and Setup in your OS (Windows/Mac/Linux). For detailed Instructions, please refer [this.](https://docs.docker.com/engine/install/)
2. Navigate to the folder where you have cloned this repository ( where the ***Dockerfile*** is present ).
3. Build the Docker Image (don't forget the dot!! :smile: ): 
```
docker build -f Dockerfile -t app:latest .
```
4. Run the docker:
```
docker run -p 8501:8501 app:latest
```

This will launch the dockerized app. Navigate to ***http://localhost:8501/*** in your browser to have a look at your application. You can check the status of your all available running dockers by:
```
docker ps
```


### Heroku Deployment (Optional)
1. Navigate to the [Heroku Platform](https://www.heroku.com/) and login using your E-mail. In case you don't have an account, you can sign-up using your E-mail.
2. After account creation and successful login, click on **Create New App**. The platform shall now ask you to choose a suitable name for the webapp and the corresponding region (Europe/United States)
3. Add a payment method and click on **Create App**.
4. Open a new tab and login into your [Github Account](https://github.com/) and create a git repository comprising of this entire directory's files and sub-directories. Ensure that your webapp's directory structure looks like this:
![ls](https://user-images.githubusercontent.com/29462447/204844686-aa004efe-39b4-49f2-a5a7-a5098831c1df.png)

5. Switch back to the heroku app configuration and under the **Deploy** menu, select **Github** under the **Deployment Method** category.
6. You need to successfully authenticate and authorize access to your Github account by Heroku. After successful authorization, search for your git repository name and select **Connect**.
7. Go to **Manual Deploys** section and select the suitable branch name from the git repository which you wish to deploy.
8. Click **Deploy Branch**. This will launch the webapp deployment and you can view the build logs. This may take several minutes and upon completion, you should see a message stating:
```
Launching...
Released v1
https://<heroku app name>.herokuapp.com/ deployed to Heroku
```
9. You can now navigate to the URL **https://<heroku app name>.herokuapp.com/** in order to view your deployed webapp. For any troubleshooting, you can refer [their documentation.](https://devcenter.heroku.com/categories/python-support)
