# Jeff Bezos vs Bill Gates

We're going to classify images, folks. Instead of the lame dogs and cats, which are basically imagenet categories, we're doing to 2 similar dudes that look very similar (caucasion, over 50, wealthy, etc....). Fire up your conda enviorment, install some packages and let's get on our way :)


# Highlights:
- Using Keras to train a convnet from scratch to classify images of Bill Gates or Jeff Bezos (binary classification)
- Using the Generator Utilities Keras provides to avoid reading image data into RAM and also applying transformations to images
- Comparing the bottleneck feature gen strategy using VGG16 with the scratch convnet and why the imagenet weights didn't really provide for much of an advantage
- Differences in performance between taking the first 50 images google served as validation data, vs taking a large, random subset. The dangers of small data!

# Forthcoming:
- Does scaling from 500 to 2000 images improve the convnet?
- Can we finetune another convnet to get closer to 90% accuracy?
- How can we use intermediate layers to find similar images?
- Better randomization of the image data (train and validation)

# Details about my enviorment (sorry, no requirements.txt)


```bash
Python 3.5.2 |Anaconda custom (64-bit)| (default, Jul  2 2016, 17:52:12) 
[GCC 4.2.1 Compatible Apple LLVM 4.2 (clang-425.0.28)] on darwin
```

```python

>>> import keras
Using TensorFlow backend.
>>> keras.__version__
'2.0.2'

```

You'll need firefox along with selenium webdriver to get this working. Again, use Conda as a package manager and it should be OK, at least on Mac :/

# Videos and brief descriptions

- First Video: downloading the images, getting a convnet working from scratch with around 75% validation accuracy

[![Keras Bezos Gates Part 1](https://img.youtube.com/vi/O3hffX-jC98/0.jpg)](https://www.youtube.com/watch?v=O3hffX-jC98)

- Second Video: using a pretrained feature extractor VGG16 to genreate better features, which we'll feed into a MLP (not a conv network). 

[![Keras Bezos Gates Part 2](https://img.youtube.com/vi/3yxXGWnSaJI/0.jpg)](https://www.youtube.com/watch?v=3yxXGWnSaJI)


- Third Video: here we delve into further issues around training and validation set splitting and also step through a basic python script to split our images up into training and validation sets. I also reflect a bit on these issues

[![Keras Bezos Gates Part 3](https://img.youtube.com/vi/er5Z4p9W29U/0.jpg)](https://www.youtube.com/watch?v=er5Z4p9W29U)


- Fourth Video: we switch gears and move onto a better dataset to apply our incremental learning stragies (scratch convnet --> transfer learning). I also move to a windows machine with a gtx1080ti card

[![Keras Bezos Gates Part 4](https://img.youtube.com/vi/r3vFSRCdkhU/0.jpg)](https://www.youtube.com/watch?v=r3vFSRCdkhU)


- Fifth Video: using our validation generator, but tweaking it to generate ordered predictions and hacking some code together to check out some images and view the images behind some inaccurately classified predictions. We also introduce the confusion matrix

[![Keras Bezos Gates Part 5](https://img.youtube.com/vi/DCzJQTcYgYU/0.jpg)](https://www.youtube.com/watch?v=DCzJQTcYgYU)







