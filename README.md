# Clean Up Your Digital Life: Simplify Your Photo Organization and Say Goodbye to Photo Clutter

![img](https://dicksonneoh.com/images//blog/clean_up_your_digital_life/post_image.gif)

A companion repo for the blog post [Clean Up Your Digital Life: Simplify Your Photo Organization and Say Goodbye to Photo Clutter](https://dicksonneoh.com/blog/clean_up_your_digital_life/).

## 📂 Folder Structure

* `fastdup_report/` -- Folder to store Fastdup files.

* `images/` -- Images folder. Use your own or download from [Kaggle](https://www.kaggle.com/datasets/duttadebadri/image-classification).

* `fastdup_analyze.ipynb` -- A Jupyter notebook to run Fastdup.


## 🧮 Install and Run
First, let’s install Fastdup with -

```
pip install fastdup
```

Run Fastdup -

```python
import fastdup
fastdup.run(input_dir="./images", 
            work_dir="./fastdup_report",
            turi_param='ccthreshold=0.88')
```

## ❌ Duplicate Photos
View duplicate images - 

```python
import fastdup
from IPython.display import HTML
fastdup.create_duplicates_gallery(similarity_file='./fastdup_report/similarity.csv',
                                  save_path='./fastdup_report/', 
                                  num_images=20)

HTML('./fastdup_report/similarity.html')
```

![img](https://dicksonneoh.com/blog/clean_up_your_digital_life/duplicates.png)


## 🤳 Dark, Bright, and Blurry Shots

View dark shots.

```python
fastdup.create_stats_gallery('./fastdup_report/atrain_stats.csv', 
                             save_path='./fastdup_report', descending=False,
                             max_width=400, metric='mean')
HTML('./fastdup_report/mean.html')
```

![img](https://dicksonneoh.com/blog/clean_up_your_digital_life/dark.png)

View bright shots.

```python
fastdup.create_stats_gallery('./fastdup_report/atrain_stats.csv', 
                             save_path='./fastdup_report', 
                             descending=True,
                             max_width=400, metric='mean')
HTML('./fastdup_report/mean.html')
```

![img](https://dicksonneoh.com/blog/clean_up_your_digital_life/bright.png)

View blurry shots.

```python
fastdup.create_stats_gallery('./fastdup_report/atrain_stats.csv', 
                             save_path='./fastdup_report', 
                             descending=False,
                             max_width=400, metric='blur')
HTML('./fastdup_report/blur.html')
```

![img](https://dicksonneoh.com/blog/clean_up_your_digital_life/blur.png)


## 🗂 Clustering Similar Shots
View clusters - 

```python
fastdup.create_components_gallery(work_dir='./fastdup_report/',
                                  save_path='./fastdup_report/',
                                  get_label_func= lambda x:x)
HTML('./fastdup_report/components.html')
```

![img](https://dicksonneoh.com/blog/clean_up_your_digital_life/cluster_160.png)
![img](https://dicksonneoh.com/blog/clean_up_your_digital_life/cluster_6667.png)
![img](https://dicksonneoh.com/blog/clean_up_your_digital_life/cluster_16356.png)

## 📞 Questions? Connect with me
If you have any questions or feedback, please don't hesitate to reach out to me.
I'm active on the following platforms.
<p align="left">
      <a href="https://www.linkedin.com/in/dickson-neoh/" target="blank"><img align="center"
            src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
      <a href="https://twitter.com/dicksonneoh7" target="blank"><img align="center"
            src="https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white" /></a>
      <a href="https://github.com/dnth" target="blank"><img align="center"
            src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white" /></a>
      <a href="https://www.youtube.com/channel/UCJckpaGYra_p9ixmEDvYARA" target="blank"><img align="center"
            src="https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white" /></a>
      <a href="mailto:dickson.neoh@gmail.com" target="blank"><img align="center"
            src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white"/></a>
      <a href="https://medium.com/@dickson.neoh" target="blank"><img align="center"
            src="https://img.shields.io/badge/medium-%2312100E.svg?&style=for-the-badge&logo=medium&logoColor=white"/></a>
      <a href="https://dicksonneoh.com/" target="blank"><img align="center"
            src="https://raw.githubusercontent.com/dnth/dnth.github.io/main/static/images/site-navigation/logo_dn.png"
            alt="dnth" height="45" /></a>
</p>

## ❤️ Support Me
I am thrilled to share my work with you and I hope you find it useful. 

If you do, please consider supporting my efforts by making a donation and/or sharing this repository on your social media. 

Your support will help me to continue developing and maintaining this project, as well as create new ones.

<a href="https://www.buymeacoffee.com/dicksonneoh" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-blue.png" alt="Buy Me A Coffee" style="height: 60px !important;width: 217px !important;" ></a>
