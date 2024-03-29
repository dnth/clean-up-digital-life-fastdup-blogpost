# Clean Up Your Digital Life: How I Found 1929 Fully Identical Images, Dark, Bright and Blurry Shots in Minutes, For Free.

![img](https://dicksonneoh.com/images//blog/clean_up_your_digital_life/post_image.gif)

A companion repo for the blog post [Clean Up Your Digital Life: Simplify Your Photo Organization and Say Goodbye to Photo Clutter](https://dicksonneoh.com/blog/clean_up_your_digital_life/).

## 📂 Folder Structure

* `fastdup_report/` -- Folder to store fastdup files.

* `images/` -- Images folder. Use your own or download from [Kaggle](https://www.kaggle.com/datasets/duttadebadri/image-classification).

* `fastdup_analyze.ipynb` -- A Jupyter notebook to run fastdup.


## 🧮 Install and Run
First, let’s install fastdup with -

```
pip install fastdup==0.903
```

Run fastdup -

```python
import fastdup

work_dir = "./fastdup_report"
images_dir = "./images"

fd = fastdup.create(work_dir, images_dir)
fd.run()
```

## 🚫 Invalid Images

Get a list of broken images found by fastdup:

```python
fd.invalid_instances()
```

![img](https://dicksonneoh.com/blog/clean_up_your_digital_life/invalid.png)


## 👯‍♂️ Duplicate Images
View duplicate images - 

```python
fd.vis.duplicates_gallery()
```

![img](https://dicksonneoh.com/blog/clean_up_your_digital_life/duplicates.png)


## 🤳 Dark, Bright, and Blurry Shots

View dark shots.

```python
fd.vis.stats_gallery(metric='dark')
```

![img](https://dicksonneoh.com/blog/clean_up_your_digital_life/dark.png)

View bright shots.

```python
fd.vis.stats_gallery(metric='bright')
```

![img](https://dicksonneoh.com/blog/clean_up_your_digital_life/bright.png)

View blurry shots.

```python
fd.vis.stats_gallery(metric='blur')
```

![img](https://dicksonneoh.com/blog/clean_up_your_digital_life/blur.png)


## 🗂 Clustering Similar Shots
View clusters - 

```python
fd.vis.component_gallery()
```

![img](https://dicksonneoh.com/blog/clean_up_your_digital_life/components.png)

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
