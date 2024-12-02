# FLUX LoRa

A LoRA adapter tailored to the [FLUX.1-dev](https://huggingface.co/black-forest-labs/FLUX.1-dev) AI image model, with a focus on generating personalized images.

**NOTE:** To protect the privacy of the data, the LoRA weights as well as the data used to train the LoRA is not included in this repository.

## Background

### LoRAs

LoRAs are small, efficient adapters that can be added to a model to improve its performance on a specific task. They are typically used in conjunction with a base model, such as a large language model or an image model.

For more information, please read the [LoRA paper](https://arxiv.org/abs/2106.09685).

### FLUX.1-dev

FLUX.1-dev is a state-of-the-art AI image model that can generate high-quality images from text descriptions.

For more information, please read the [official blog post](https://blackforestlabs.ai/announcing-black-forest-labs/) from Black Forest Labs.

## Sample Images
generated_images/1.jpg             | generated_images/2.jpg
:-------------------------:|:-------------------------:
![](./generated_images/1.jpg)  |  ![](./generated_images/2.jpg)

generated_images/3.jpg             | generated_images/4.jpg
:-------------------------:|:-------------------------:
![](./generated_images/3.jpg)  |  ![](./generated_images/4.jpg)

## Training Your Own LoRA

### Install Dependencies

First, you need to install the project dependencies using `pip`:

```bash
pip install -r requirements.txt
```

### Gather Data

Then, in the `/images` directory, place the training images in `.png` format. You should have at least 12 high-quality images to train the LoRA. (Example: `/images/1.png`, `/images/2.png`, etc.)

### Add captions

Also in the `/images` directory, you must place the captions for the images in `.txt` format. Each caption should be in a separate file and the file name should match the image file name. (Example: `/images/1.txt`, `/images/2.txt`, etc.)

### Train LoRA

Finally, you can train the LoRA by running the following command:

```bash
python train.py --config train_configs/lora.yaml
```
