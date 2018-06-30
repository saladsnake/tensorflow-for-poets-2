# Overview

This is the Codelab guide to retraining this tensorflow image classifier:
goo.gl/8seMCU

I have retrained it to identify the toyota supra and toyota corolla.

To retrain, pass these settings inside Linux shell variables first
- export IMAGE_SIZE=224
- export ARCHITECTURE="mobilenet_0.50_${IMAGE_SIZE}"

Launch tensorboard before training
- tensorboard --logdir tf_files/training_summaries &

Run the training script with this command 
- python -m scripts.retrain \
-   --bottleneck_dir=tf_files/bottlenecks \
-   --model_dir=tf_files/models/"${ARCHITECTURE}" \
-   --summaries_dir=tf_files/training_summaries/"${ARCHITECTURE}" \
-   --output_graph=tf_files/retrained_graph.pb \
-   --output_labels=tf_files/retrained_labels.txt \
-   --architecture="${ARCHITECTURE}" \
-   --image_dir=tf_files/(folder all the images are in)
