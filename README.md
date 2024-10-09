# CS7180-FinalProject

This is the submission for 

The Final Project
for the course "CS7180 Advanced Perception"

Collaborators: Aditya Varshney, Anirudh Muthuswamy, Gugan Kathiresan

# Low-Rank Adaptation for Image Super-Resolution
This project aims to apply the Low-Rank Adaptation (LoRA) technique to efficiently fine-tune and optimize complex deep learning models for the task of single image super-resolution (SISR). As state-of-the-art SISR models continue to grow in size and complexity, traditional fine-tuning methods become computationally expensive and time-consuming. LoRA offers a promising solution by drastically reducing the number of trainable parameters while preserving model performance.
Approach
The key steps involved in this project are:

Baseline Model: We start with the Enhanced Super-Resolution Generative Adversarial Network (ESRGAN), a powerful SISR model that incorporates perceptual and adversarial losses for high-quality image reconstruction.
Low-Rank Adaptation: We integrate LoRA layers into the ESRGAN architecture, allowing us to fine-tune the model on new datasets while freezing the pre-trained weights. This significantly reduces the number of trainable parameters and computational requirements.
Experiments and Evaluation: We conduct extensive experiments to evaluate the efficacy of LoRA for SISR. This includes training on a combination of datasets (DIV2K, Flickr2K, OutdoorSceneTraining) and testing on diverse datasets like FloodNet (aerial images), Set4, and Set15.

Results
Our experiments demonstrate the significant benefits of using LoRA for efficient SISR:

81% reduction in trainable parameters: By leveraging LoRA, we achieve a massive reduction in the number of trainable parameters compared to traditional fine-tuning.
Improved performance metrics: Despite the reduced parameter count, the LoRA-optimized ESRGAN model achieves higher PSNR and SSIM scores on the test datasets.
Faster inference: We observe up to a 35% decrease in inference time compared to the baseline ESRGAN model, enabling faster and more efficient super-resolution.

Future Work
Potential future directions for this project include:

Extending the LoRA approach to other state-of-the-art architectures, such as transformer-based and diffusion models for SISR.
Investigating the impact of different rank values for the LoRA layers and their effect on performance and efficiency trade-offs.
Combining LoRA with other efficient training techniques like mixed-precision, gradient checkpointing, and quantization for further optimization.
Analyzing the generalization capabilities of LoRA-optimized models across diverse domains and datasets.

---------------------------------------------
Details

## Repository Highlights
- Demo Notebook- "training_exp.ipynb"
- Source Code - in the files and folders inside ./src/
  
## Operating System
- Google Colab Pro Ubuntu / T4 GPU
- Discovery Cluster Jupyter Notebook / V100 GPU
- macOS for file management

## Required Packages
In your command line
> cd /path/to/your/project
> pip install -r requirements.txt

## Compilation Instructions for the script files
- Download the datasets
    - FloodNet dataset - https://drive.google.com/drive/folders/1sZZMJkbqJNbHgebKvHzcXYZHJd6ss4tH?usp=sharing
    - Set5 dataset - https://uofi.box.com/shared/static/kfahv87nfe8ax910l85dksyl2q212voc.zip
    - Set14 dataset - https://uofi.box.com/shared/static/igsnfieh4lz68l926l8xbklwsnnk8we9.zip

- Unzip the files and place it in the working directory
- Install all requirements from the "requirements.txt" file
- Open src/main.py and edit the parameters according to your experiment's requirments. These include parameters like dataset_path, crop_size, batch_size, warmup_batches, n_batches, batch, sample_interval, save_path_suffix,and lora_save_path
- Then simply run tthe main.py file sing 
> !python ./src/main.py



