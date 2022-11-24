---
title: python_def
tags: TeXt
article_header:
  type: cover
---


```python
#encoding: utf-8
from tkinter import *
import numpy as np
import cv2
import tkinter as tk
from tkinter import filedialog
from tkinter.filedialog import askdirectory
import os
imagepath= askdirectory()
# print(imagepath)
f_path = os.listdir(imagepath)
# print(f_path)
for image in f_path:
    # print(image)
    poirtion = os.path.splitext(image)
    # print(poirtion)
    if poirtion[1] == '.raw':
        realpath = imagepath + "/" + image
        # print(realpath)
        f = np.fromfile(realpath , np.uint16)
        f.shape = (964, 1280)
        filename = poirtion[0] + '.png'
        png_filename = os.path.join(imagepath , filename)
        cv2.imwrite(png_filename , f)
        # print("完成")
    else:
        # print("not raw")




```
