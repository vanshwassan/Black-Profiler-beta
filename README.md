# Black-Profiler-beta
Black Profiler - Find all relevant information of a person through his/her image using OSINT and ML techniques

![alt text](https://raw.githubusercontent.com/vanshwassan/Black-Profiler-beta/master/blackprofiler.png)

# Idea
My main idea behind this project was to mix the concepts of OSINT(Open Source Intelligence), Web Scraping and Machine Learning to make an effective profiler to find anyone's information just by his/her image file.

### For the sake of making this project simple, I've divided the whole problem into 3 steps
- First, we need to prepare a training set of people with their images. For that, the best source was Instagram. There is an epic script which I've used in this project to scrape Instagram accounts. It also holds the ability to download posts of multiple accounts and even a whole city! (We have downloaded 7-8 profiles for the sake of keeping it simple for now)

- Secondly, I used OpenCV, dlib and face_recognition libraries to make a script that works on KNN (K Nearest-Neighbour) Algorithm for face recognition. It trains the train_dir (which contains the scrapped instagram accounts) and then tests it with a testing image stored in test directory.<br>
It then predicts the output which is then stored in a text file <b>username.txt</b>.

- Finally, I used BeautifulSoup and made <b>profiler.py</b> that simply takes the username from the txt file and then finds the information about that Instagram account.

# Installation

<b>YOU NEED SCIKIT AND DLIB FOR THIS PROJECT!</b>

```
pip install face_recognition
pip install PIL
```

# Usage
Use an Instagram scrapper to download posts from accounts. I used the scrapper from arc298 - https://github.com/arc298/instagram-scraper <br>
Train the dataset and provide an unknown image in test directory <br>
```
python facerecog.py
```
Predict the result and then start profiler.py to scan that account. <br>
```
python profiler.py
  
Special Thanks <br>
face_recognition library - https://github.com/ageitgey/face_recognition <br>
Instagram-Scrapper - https://github.com/arc298/instagram-scraper 

  
 

