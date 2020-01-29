# YouTube Trending Video Analysis

Data analysis of YouTube trending videos. Using a public dataset powered by the YouTube API, this project uncovers some key observations and insights into trending videos in the US and around the world for one of the largest search engines and one of the largest social media platforms.

* [Background](#background)
* [Team](#team)
* [About the Data](#data)
* [Tasks and Timeline](#timeline)
* [Getting Started / Project Setup](#setup)
* [Merge / Pull Request Checklist](#pr_checklist)
* [Jupyter Notebook](#nb)
* [Images](#images)
* [Technologies Used](#technologies)

## <a name="background></a> Background

YouTube is one of the largest search engines and one of the largest social media platforms. It is used by people all over the US and around the world. People use YouTube for a variety of reasons, such as watching music videos, learning how to do something new, watching sports highlights, or just watching random videos for entertainment. Because of the popularity of YouTube, we decided to dig a little deeper into some of the characteristics that videos (in particular, trending videos) share. After gathering the information, we used that data to uncover some observations into what makes up a trending video and some insights for how a YouTube creator can improve their viewer engagement (likes, comments, dislikes, etc).

## <a name="team"></a> Team

* The following people worked together over the course of about a couple of weeks to make this project happen:
  * Phil Stubbs
  * Katrina Koenders
  * Ben Smethurst
  * Jenna Nytes

## <a name="data"></a> About the Data

For this project, we used a public kaggle dataset, which is located [here](./https://www.kaggle.com/datasnaek/youtube-new/data). This dataset is powered by the YouTube API. It includes various information about trending videos in the US from 2017 - 2018 and includes video information for several other countries as well. For this project, we primarily looked at the US but did compare the US vs OUS for a couple of the visualizations/research questions. The dataset was in the form of csv files (one for each country). Due to the large size of these csv files, we chose not to store the data files in GitHub. We stored the csv files that we used for this project in a shared Google Drive folder where everyone on the team could access them, pull them down, and unzip them. The data includes a lot of useful information about each video, such as publish time, number of views, number of likes, and the tags associated with each video. To complete this analysis, we merged all the csv files into one pandas dataframe to do the analysis. The data also includes a category_id field. To retrieve the category name, we had to create and hit an endpoint to the YouTube API to get the additional category data. For more information about specific columns and what they mean, refer to the [YouTube API documentation](https://developers.google.com/youtube/v3/docs/videos/list).

## <a name="timeline"></a> Tasks and Timeline

 We started this project on January 15, 2020, completed our analysis on January 28, 2020, and then presented our findings on January 29. To keep track of the tasks and who needed to do what to meet this tight deadline, we created a [Trello Board](https://trello.com/b/qjMY63WI/whos-doing-what) so everyone on the team knows who is working on what and to help keep track of key project resources and files.

## <a name="setup"></a> Getting Started / Project Setup

To set up this repository locally on your computer, perform the following steps:

1. Clone this repository to a local directory (for example, **Desktop**) on your computer.

2. Make sure you are in your **PythonData** Anaconda environment.

  ```bash
  conda activate PythonData
  ```

3. Change directory to the project root directory (**team_hopper**).

```bash
cd ./team_hopper
```

4. Inside this directory, create a folder called **Resources** and add the **youtube_trending.zip** and **trending_videos_2020.zip** files to this folder.

You can get the data zip files from the shared Google Drive folder (see Project Resources in Trello board for the link or ask phil to share them with you).

5. We are using one package that is not part of the standard python library. So, you will need to run the followig command in your anaconda environment to install it:

```bash
pip install isodate
```

6. From the project root directory (**team_hopper**), open jupyter notebook.

```bash
jupyter notebook
```

7. Before running the cells in the notebook file, you will need to get a Google API key to use/access the YouTube Data API v3 (if you don't have one already).

To get a Google API key:

* Go to <https://cloud.google.com>.
* Click **Go to console**.
* If you don't already have a project, you will need to create a new project. Otherwise, select any project you want to use.
* In the **Getting Started** section on your **DASHBOARD**, click **Explore and enable APIs**.
* Click **Credentials** to generate an API key (if you don't already have one).
* Then, click **Library** and search for **YouTube Data API v3**. Enable this one.

8. Create a file called **config.py** in the project root directory (**team_hopper**) and add the following line with your API key:

  ```bash
  youtube_api_key = "YOUR_API_KEY_HERE"
  ```

9. Go into the [youtube_trends.ipynb](youtube_trends.ipynb) notebook file and run the cells inside of the section called, **Getting Started and Setup**.

## <a name="pr_checklist"></a> Merge/Pull Request Checklist

To contribute to this project, you will need to submit a pull request and have at least one person review your code and merge it in for you.
But, before you create a pull request, go through the following checklist.

* For the csv files in the **Resources** folder, dont commit the zip files or the extracted csv files.  This is already accounted for in the .gitignore but you never know.
* Make sure to restart and clear output in jupyter notebook. This keeps the file diff small when having someone else code review your work, and it will also help cut down on merge conflicts.
* Code is documented and includes comments where needed for further explanation.
* Make sure you are working in your **PythonData** anaconda environment when making changes.
* Always pull in master into your branch **before** you start working on a new feature and **before** you submit a pull request for code review. This will help cut down on merge conflicts.

## <a name="nb"></a> Jupyter Notebook

For this project, we used jupyter notebook to render and display the results of this analysis. You can view the notebook [here](./youtube_trends.ipynb):

In this notebook, you will find more information about the project, including an overview, the code used to do the analysis, the actual written analysis, and of course, the visualizations (the best part).

## <a name="technologies"></a> Technologies Used

We used the following technologies to complete this project:

* YouTube API
* Jupyter Notebook
* Python
* Pandas
* Matplotlib
* Packages for formatting and manipulated time and dates (isodate, time, datetime)
* Packages for reading, writing to, and zipping files/folders (glob, Path, os, zipfile, shutil)
* And other small packages/tools...