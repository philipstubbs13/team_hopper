# YouTube Trending Video Analysis

## Getting Started / Project Setup

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


5. From the project root directory (**team_hopper**), open jupyter notebook.

```bash
jupyter notebook
```

6. Before running the cells in the notebook file, you will need to get a Google API key to use/access the YouTube Data API v3 (if you don't have one already).

To get a Google API key:

* Go to <https://cloud.google.com>.
* Click **Go to console**.
* If you don't already have a project, you will need to create a new project. Otherwise, select any project you want to use.
* In the **Getting Started** section on your **DASHBOARD**, click **Explore and enable APIs**.
* Click **Credentials** to generate an API key (if you don't already have one).
* Then, click **Library** and search for **YouTube Data API v3**. Enable this one.

7. Create a file called **config.py** in the project root directory (**team_hopper**) and add the following line with your API key:

  ```bash
  youtube_api_key = "YOUR_API_KEY_HERE"
  ```

8. Go into the [youtube_trends.ipynb](youtube_trends.ipynb) notebook file and run the cells inside of the section called, **Getting Started and Setup**.

