# Style-Transfer Print/Scan
This repository describes the complementary material for the paper: "Generating Automatically Print/Scan Textures for Morphing Attack Detection Applications". This process focuses on simulating the handcrafted print/scan texture used to create print/scan version images automatically from bona fide examples. This scenario allows us to train in single and differential morphing Attacks. 

This repository describes the Transfer-style method-based GANs using a PyTorch-CycleGAN-and-pix2pix implementation
- Paper under revision process.

# Pre-requisite
- Linux
- Python 3
- CPU or NVIDIA GPU + CUDA CuDNN

# Getting Started
- Clone this repo:
```
git clone https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix
cd pytorch-CycleGAN-and-pix2pix
```
- Install PyTorch and 0.4+ and other dependencies (e.g., torchvision, visdom)
- For pip users, please type the command pip install -r requirements.txt.
- For Conda users, you can create a new Conda environment using conda env create -f environment.yml.

# Pre-trained models
  - Downloading (Soon)
  - Paper under revision process.

# Generate your own PS600 images:
- Pix2pix
- CycleGAN
```
python test.py --dataroot datasets/face/testA --name CycleGANps600-noflip-pixel --model test --no_dropout  
```
The option --model test is used for generating results of CycleGAN only for one side. This option will automatically set --dataset_mode single, which only loads the images from one set. On the contrary, using --model cycle_gan requires loading and generating results in both directions, which is sometimes unnecessary. The results will be saved at ./results/. Use --results_dir {directory_path_to_save_result} to specify the results directory.

For pix2pix and your own models, you need to explicitly specify --netG, --norm, --no_dropout to match the generator architecture of the trained model. 
# Example images
<p align="center">
<img width="823" alt="Example-ps600-caption" src="https://github.com/jedota/Style-Transfer-PS600/assets/45126159/577164af-6b85-46ca-bc4c-cf5dac331042">
</p>

# Complentary model
- A secondary semi-automatic  texture transfer method was also developed.
- Implementation is available in: 

# Cite
Pending

# Disclaimer
This work and the methods proposed are only for research purposes, and the images are generated by chance. Any implementation or commercial use modification must be analysed separately for each case to the email: juan.tapia-farias@h-da.de 
