# Movie-Recommender-with-Sentiment

A Content Based Recommender System that recommends Hollywood movies similar to the movie user likes and analyses the sentiments on the reviews given by other users for that movie.

## Datasets-
1. https://www.kaggle.com/carolzhangdc/imdb-5000-movie-dataset
2. https://www.kaggle.com/rounakbanik/the-movies-dataset
3. https://en.wikipedia.org/wiki/List_of_American_films_of_2018
4. https://en.wikipedia.org/wiki/List_of_American_films_of_2019
5. https://en.wikipedia.org/wiki/List_of_American_films_of_2020

I am also providing my Google Drive link which have all the datasets that are used in this project.
Google Drive- https://drive.google.com/drive/folders/1lLYRljaQww_19vsAloxH9b4zA_jxKRt9?usp=sharing

## Installation
The Code is written in Python 3.7.3 If you don't have Python installed you can find it [here](https://www.python.org/downloads/). If you are using a lower version of Python you can upgrade using the pip package, ensuring you have the latest version of pip. To install the required packages and libraries, run this command in the project directory after [cloning](https://www.howtogeek.com/451360/how-to-clone-a-github-repository/) the repository:

##### 1. First create a virtual environment by using this command:
```bash
conda create -n myenv python=3.7
```
##### 2. Activate the environment using the below command:
```bash
conda activate myenv
```
##### 3. Then install all the packages by using the following command
```bash
pip install -r requirements.txt
```
##### 4. Then, in cmd or Anaconda prompt write the following code:
```bash
python app.py
```
##### Make sure to change the directory to the root folder.  

## How to get the API?
First, install the tmdbv3api library using the command ```pip install tmdbv3api```. Create an account in https://www.themoviedb.org/, click on the API link from the left hand sidebar in your account settings and fill all the details to apply for API key. If you are asked for the website URL, just give "NA" if you don't have one. You will see the API key in your API sidebar once your request is approved.

## Deployement on AWS Ec2 instance
Login or signup in order to create virtual app. We can access the free tier. For application deployment we have to install Putty,Puttygen and WinSCP. I have used "Ubuntu" server for deployment and selected the "t2 micro" as it is free. We have to create a "pemp file" and download it and keep it inside the same working directory as of the project files. We have to use this pemp file and get the "ppk file". We can use Putty and Puttygen for this. Once this is done we can push our file from our local machine to the ubuntu server using WinSCP. After that we have to manually install all the libraries in the ubuntu server as it is a free tier, libraries are not pre installed. We also need to update the pip inside our ubuntu command prompt. For this I have used te code ```sudo apt-get update && sudo apt-get install python3-pip```. For installing all the dependencies use the code ```pip3 install -r requirements.txt```. Once all this is set run ```python3 app.py```. Inside AWS Management Console>EC2>Running Instances>Ations there is the publice accesss url, copy that and add :8080 (which is the port for running the application) and hit enter. We have to also note that inside our .py file, the starting point of our application should be ```app.run(debug = True, host = "0.0.0.0", port = 8080)```.
Note: In AWS EC2 we have to update the security group and set "all traffic" and "anywhere" so that anayone with the link can access our application.

## Frontend Using AJAX, HTML and CSS and Backend using Flask


http://ec2-3-23-64-155.us-east-2.compute.amazonaws.com:8080/

![Screenshot (132)](https://user-images.githubusercontent.com/75041273/132076016-641b788b-96a5-441e-8334-d76e75b474a5.png)
![Screenshot (128)](https://user-images.githubusercontent.com/75041273/132076038-491123a1-3ac1-4515-bdf1-756cf353a9e3.png)
![Screenshot (129)](https://user-images.githubusercontent.com/75041273/132076058-447a37df-84ac-4eb5-8b90-8e82a0edc5ef.png)
![Screenshot (130)](https://user-images.githubusercontent.com/75041273/132076071-5e4f3bb6-bda0-44e4-aaf3-493f114312bf.png)
![Screenshot (131)](https://user-images.githubusercontent.com/75041273/132076092-29f8b02a-7dc3-46d7-8aed-0e393c18877c.png)
