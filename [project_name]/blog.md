# EduHub

EduHub is a platform for all your educational needs built using Python ,Flask ,Courier's API and Cohere's NLP  API.

<img src="https://raw.githubusercontent.com/cyrixninja/CourierHacks/main/screenshots/1.png">

# Inspiration💡
Whenever we sign up on educational platforms we always need to sign up to use anything.No feature is usable without signing up. That's a huge concern for us these days. We really care about privacy and protecting our credentials. So we decided to make a  platform for all your educational needs that doesn't require a sign up or anything. We have added a lot of features to EduHub. Also we sometimes felt a need for a news notification service that's completely open-source and provides you with daily news notifications about your desired topic. We always thought that it would make our lives easier as students as we can get news notifications about anything we are learning or want to learn about. Like when I was trying to learn about astrophysics I felt a need for an email service that would give me the latest news about astrophysics or anything I want to learn about.   

# API,Frameworks and Plaforms needed for development

- [Courier API](https://www.courier.com/docs/)
- [Python](https://www.python.org/downloads/)
- [Python Flask](https://pypi.org/project/Flask/)
- [Firebase Realtime Database](https://firebase.google.com/docs/database)
- [Cohere's NLP API](https://docs.cohere.ai/)
- [Replit](https://replit.com/)
- [Visual Studio Code](https://code.visualstudio.com/)
- [GitHub](https://github.com/)

# Features 

### 1.Daily News Notification: It provides you daily news notification about your desired topic. Just type your email and you'll get daily news notification about your topic. It will help you to keep yourself with current academic news or the thing you're learning about currently.

### 2.Connect with People: It's a page where you can meet with fellow students and people around you. Just type in your information and we'll let you know if anyone wants to connect with you in your inbox.

### 3.AI Advice: Ever stuck or unable to make a decision? I have been in that situation a lot of times. Well then need a quick reply? We got you. Our AI Advice service is powered by Courier's API and Cohere's NLP API. Enter your query and email address and our service will give you a quick response in your inbox.

### 4:Anonymous Advice: Aren't satisfied with our AI's Advice? Then you can try taking advice from fellow students and get your problem or query resolved. It will be anonymous and you don't need to sign up for an account to use it. Whenever someone replies, you'll get an email from us about their reply.

### 5.Donate Books: We all have some books that we don't use after quite a while. Well then you can always donate them to people who really need it. Just type your email and add some information about the book you wanna donate. Whenever anyone wants your books we'll contact you with their information in your inbox

# Instructions

## Part 1: Setting Up the Backend

```
git clone https://github.com/cyrixninja/CourierHacks.git
cd CourierHacks
cd backend
```

### A) Setting up Daily News Notification Backend

#### 1. Navigate into the news directory in Backend Folder 
 ```
 cd news 
 cd webapp
 code .
 ```

#### 2. Add your API Keys and Credentials to following lines in app.py

##### Add your Firebase Credentials on line 8 and 10 respectively
   To generate firebase credentials follow this link [here](https://firebase.google.com/docs/database/admin/start)
   ```
  cred_obj = firebase_admin.credentials.Certificate('<JSON>')
default_app = firebase_admin.initialize_app(cred_obj, {
	'databaseURL':"<DATABASE URL>"
	})
   ```
##### Add your Courier API Key on Line 116
 To generate Courier API Key follow this link [here](https://help.courier.com/en/articles/4677510-using-environments-api-keys-and-migrating-assets)
```
        headers = {
  "Accept": "application/json",
  "Content-Type": "application/json",
  "Authorization": "Bearer pk_test_<Courier APIKEY>"
}

```
##### 3. Now the code is ready to run. You can host it on any of the services like replit or heroku.We used replit for hosting it.Please Copy the link of hosted app url.You'll need it when we start assemblying the project.


### B) Setting up Connect Backend

#### 1. Navigate into the Connect directory in Backend Folder 
 ```
 cd connect
 code .
 ```

#### 2. Add your API Keys and Credentials to following lines in app.py

##### Add your Firebase Credentials on line 11 and 13 respectively
   To generate firebase credentials follow this link [here](https://firebase.google.com/docs/database/admin/start)
   ```
  cred_obj = firebase_admin.credentials.Certificate('<JSON>')
default_app = firebase_admin.initialize_app(cred_obj, {
	'databaseURL':"<DATABASE URL>"
	})
   ```
##### Add your Courier API Key on Line 95
 To generate Courier API Key follow this link [here](https://help.courier.com/en/articles/4677510-using-environments-api-keys-and-migrating-assets)
```
        headers = {
  "Accept": "application/json",
  "Content-Type": "application/json",
  "Authorization": "Bearer pk_test_<Courier APIKEY>"
}

```
##### 3. Now the code is ready to run. You can host it on any of the services like replit or heroku.We used replit for hosting it.Please Copy the link of hosted app url.You'll need it when we start assemblying the project.


### C) Setting up Donate Backend

#### 1. Navigate into the Donate directory in Backend Folder 
 ```
 cd donate
 code .
 ```

#### 2. Add your API Keys and Credentials to following lines in app.py

##### Add your Firebase Credentials on line 10 and 12 respectively
   To generate firebase credentials follow this link [here](https://firebase.google.com/docs/database/admin/start)
   ```
  cred_obj = firebase_admin.credentials.Certificate('<JSON>')
default_app = firebase_admin.initialize_app(cred_obj, {
	'databaseURL':"<DATABASE URL>"
	})
   ```
##### Add your Courier API Key on Line 93
 To generate Courier API Key follow this link [here](https://help.courier.com/en/articles/4677510-using-environments-api-keys-and-migrating-assets)
```
        headers = {
  "Accept": "application/json",
  "Content-Type": "application/json",
  "Authorization": "Bearer pk_test_<Courier APIKEY>"
}

```
#### 3. Now the code is ready to run. You can host it on any of the services like replit or heroku.We used replit for hosting it.Please Copy the link of hosted app url.You'll need it when we start assemblying the project.


### D) Setting up AI Advice Backend

#### 1. Navigate into the Advice directory in Backend Folder 
 ```
 cd advice 
 cd ai-advice
 code .
 ```

#### 2. Add your API Keys and Credentials to following lines in app.py

##### Add your Cohere NLP Credentials on line 9 
   To generate Cohere credentials follow this link [here](https://docs.cohere.ai/)
   ```
co = cohere.Client('APIKEY')
   ```
##### Add your Courier API Key on Line 62
 To generate Courier API Key follow this link [here](https://help.courier.com/en/articles/4677510-using-environments-api-keys-and-migrating-assets)
```
        headers = {
  "Accept": "application/json",
  "Content-Type": "application/json",
  "Authorization": "Bearer pk_test_<Courier APIKEY>"
}

```
#### 3. Now the code is ready to run. You can host it on any of the services like replit or heroku.We used replit for hosting it.Please Copy the link of hosted app url.You'll need it when we start assemblying the project.

### E) Setting up Anonymous Advice Backend

#### 1. Navigate into the Anonymous directory in Backend Folder 
 ```
 cd advice
 cd anonymous-advice
 code .
 ```

#### 2. Add your API Keys and Credentials to following lines in app.py

##### Add your Firebase Credentials on line 10 and 12 respectively
   To generate firebase credentials follow this link [here](https://firebase.google.com/docs/database/admin/start)
   ```
  cred_obj = firebase_admin.credentials.Certificate('<JSON>')
default_app = firebase_admin.initialize_app(cred_obj, {
	'databaseURL':"<DATABASE URL>"
	})
   ```
##### Add your Courier API Key on Line 88
 To generate Courier API Key follow this link [here](https://help.courier.com/en/articles/4677510-using-environments-api-keys-and-migrating-assets)
```
        headers = {
  "Accept": "application/json",
  "Content-Type": "application/json",
  "Authorization": "Bearer pk_test_<Courier APIKEY>"
}

```
#### 3. Now the code is ready to run. You can host it on any of the services like replit or heroku.We used replit for hosting it.Please Copy the link of hosted app url.You'll need it when we start assemblying the project.

## Part 2: Connecting it all together

### Head Over to the following HTML Files and Add the hyperlinks of the Hosted Website that you did on last step in Following Lines
#### Add your Daily News Notification Website link on the line 96 in news.html
```
 <section class="py-6">
        <div class="container-lg">
          <div class="row flex-center mb-5">
            <div class="col-auto text-center my-4">
            </div>
            <center>
              <iframe src="<WEBSITE URL>"  scrolling="no" style=" width: 1000px; height: 500px;  overflow: hidden;" ></iframe>
          </center>
          </div>
      </section>
```

#### Add your Connect Website link on the line 97 and 108 in connect.html
```
      <section class="py-6">
        <div class="container-lg">
          <div class="row flex-center mb-5">
            <div class="col-auto text-center my-4">
              <h1 class="mb-4 fw-bold"></h1>
            </div>
            <center>
              <iframe src="<WEBSITE URL>"  scrolling="no" style=" width: 1000px; height: 600px;  overflow: hidden;" ></iframe>
          </center>
          </div>
      </section>
      
      <section class="py-6">
        <div class="container-lg">
          <div class="row flex-center mb-5">
            <div class="col-auto text-center my-4">
              <h1 class="mb-4 fw-bold">People Available to Connect</h1>
            </div>
            <center>
              <iframe src="<WEBSITE URL>/connect"  scrolling="no" style=" width: 1000px; height: 600px;  overflow: hidden;" ></iframe>
          </center>
          </div>
      </section>
```

#### Add your Donate Website link on the line 97 and 108  in donate.html
```
      <section class="py-6">
        <div class="container-lg">
          <div class="row flex-center mb-5">
            <div class="col-auto text-center my-4">
              <h1 class="mb-4 fw-bold">Donate your books</h1>
            </div>
            <center>
              <iframe src="<WEBSITE URL>"  scrolling="no" style=" width: 1000px; height: 600px;  overflow: hidden;" ></iframe>
          </center>
          </div>
      </section>
      <section class="py-6">
        <div class="container-lg">
          <div class="row flex-center mb-5">
            <div class="col-auto text-center my-4">
              <h1 class="mb-4 fw-bold">Available Books</h1>
            </div>
            <center>
              <iframe src="<WEBSITE URL>/books"  scrolling="no" style=" width: 1000px; height: 600px;  overflow: hidden;" ></iframe>
          </center>
          </div>
      </section>
```

#### Add your ad-advice link on the line 97  in autoadvice.html
```
    <section class="py-6">
        <div class="container-lg">
          <div class="row flex-center mb-5">
            <div class="col-auto text-center my-4">
              <h1 class="mb-4 fw-bold">Ask your questions below</h1>
            </div>
            <center>
              <iframe src="<WEBSITE URL>"  scrolling="no" style=" width: 1000px; height: 600px;  overflow: hidden;" ></iframe>
          </center>
          </div>
      </section>
```
#### Add your Donate Website link on the line 97 and 108  in advice.html

      <section class="py-6">
        <div class="container-lg">
          <div class="row flex-center mb-5">
            <div class="col-auto text-center my-4">
              <h1 class="mb-4 fw-bold">Get an advice</h1>
            </div>
            <center>
              <iframe src="<WEBSITE URL>"  scrolling="no" style=" width: 1000px; height: 600px;  overflow: hidden;" ></iframe>
          </center>
          </div>
      </section>
      <section class="py-6">
        <div class="container-lg">
          <div class="row flex-center mb-5">
            <div class="col-auto text-center my-4">
              <h1 class="mb-4 fw-bold">Give Advice</h1>
            </div>
            <center>
              <iframe src="<WEBSITE URL>/advice"  scrolling="no" style=" width: 1000px; height: 600px;  overflow: hidden;" ></iframe>
          </center>
          </div>
      </section>

## Part 3: Hosting Webiste 
### You can host your webiste on Github Pages or Replit once you're done adding the hyperlinks.Your website is ready to go now!

# Image Gallery(Email Notifications)
![image](https://raw.githubusercontent.com/cyrixninja/CourierHacks/main/screenshots/0.png)
![image](https://raw.githubusercontent.com/cyrixninja/CourierHacks/main/screenshots/9.png)
![image](https://raw.githubusercontent.com/cyrixninja/CourierHacks/main/screenshots/10.png)
![image](https://raw.githubusercontent.com/cyrixninja/CourierHacks/main/screenshots/11.png)
![image](https://raw.githubusercontent.com/cyrixninja/CourierHacks/main/screenshots/12.png)

# Image Gallery(Website)
![image](https://raw.githubusercontent.com/cyrixninja/CourierHacks/main/screenshots/1.png)
![image](https://raw.githubusercontent.com/cyrixninja/CourierHacks/main/screenshots/2.png)
![image](https://raw.githubusercontent.com/cyrixninja/CourierHacks/main/screenshots/3.png)
![image](https://raw.githubusercontent.com/cyrixninja/CourierHacks/main/screenshots/4.png)
![image](https://raw.githubusercontent.com/cyrixninja/CourierHacks/main/screenshots/5.png)
![image](https://raw.githubusercontent.com/cyrixninja/CourierHacks/main/screenshots/6.png)
![image](https://raw.githubusercontent.com/cyrixninja/CourierHacks/main/screenshots/7.png)
![image](https://raw.githubusercontent.com/cyrixninja/CourierHacks/main/screenshots/8.png)


# Message from developers

This is an open-source project. Feel Free to Fork it or Make Pull Requests to this project. We would love it if anyone wanted to contribute to this project and want to help in creating a perfect student platform. You can contact us at cyrixninja#0157 or ninnza#2681 if you got any doubts regarding implementing any new feature in this project. You should host each app individually and add their iframe in their respective HTML page. We used replit for hosting, you can use any services you like. If you face any difficulty in testing or usage, you can contact us for files with API or for our API keys. You can also use node js, go, or any programming language. Since the main page is static and features are embedded in the main page you can use always add a page with a hosted backend in any programming language and it would work flawlessly.
We can't wait to see how this platform turns out in the future. Thanks for showing your interest in our project.😁

## About the Author

Hi, I am Harsh Kumar, I am a self taught Full Stack Developer and a Machine Learning Developer.I am doing my Bachelors in Computer Science from the Gujarat Technological University in India.I have a strong interest in Cloud Computing,Linux Kernel Devlopment and Machine Learning.

Hello I am Rashi Agarwal,final year student persuing BTech in Computer Science And Engineering,a passionate engineer in the making and have my interest in developement and ai (Machine Learning,Deep Learning,Natural Language Processing and Python Developement).Quite interested in heathcare development,looking forward to create some interesting software solution for the current society problems. 

# YouTube Video Tutorial Link :- 
https://www.youtube.com/watch?v=i0xsM9EYS48
