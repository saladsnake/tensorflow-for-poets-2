# Overview

This is the Codelab guide to retraining this tensorflow image classifier:

goo.gl/8seMCU

I have retrained it to identify the toyota supra and toyota corolla, test this by placing your own image into the /tf_files directory and run the following command:
```
python -m scripts.label_image \
  --graph=tf_files/retrained_graph.pb  \
  --image=tf_files/{your own image}
```
