<h1 align="center">Core ML VAEs</h1>

<p align="center">Original Stable Diffusion VAEs already converted to MLMODELC</p>

<p align="center"><a href="#usage">Usage</a> • <a href="#choosing-a-vae">Choosing a VAE</a> • <a href="#comparison">Comparison</a></p>

## Usage

Donwload the .mlmodelc folders and swap them with the ones found in your model folder.\
You can visit my [Hugging Face](https://huggingface.co/Zabriskije/CoreML-VAEs) repo if you prefer to download them as .zip files. I couldn't upload them already packed as .zip here since the GitHub limit for files are 100MB, and I don't want to pay for Git LFS storage.\
Based on the version in use (`split-einsum`, `original`, `original_512x768`, or `original_768x512`), you must choose the corresponding VAE.\
Always make a backup of your original files in case you don't like the new look 😉

### Other Resources

If you want to convert a model yourself, you can use my [SD to Core ML](https://github.com/Zabriskije/SD-to-CoreML) script.\
Alternatively, already compiled models can be [found here](https://huggingface.co/coreml).

## Choosing a VAE

- `anything-vae`: for use with anime models; found in [Anything v3](https://huggingface.co/Linaqruf/anything-v3.0). Use is intended for ANE only since `SPLIT_EINSUM` models, combined with `CPU_AND_NE`, sometimes produce washed-out images. `orangemix-vae` yelds far superior results if used with `CPU_AND_GPU`.
- `kl-f8-anime`: for use with anime models; found in [Waifu Diffusion v1.4](https://huggingface.co/hakurei/waifu-diffusion-v1-4). Output is smoother and more contrasty than `orangemix-vae`. A lot similar to `sd-vae-ft-mse`.
- `orangemix-vae`: for use with anime models; found in [OrangeMixs](https://huggingface.co/WarriorMama777/OrangeMixs). The absolute best if used with `CPU_AND_GPU`. Produces washed-out images if used with `CPU_AND_NE`.
- `sd-vae-ft-mse`: for use with realistic models; found in [Stable Diffusion](https://huggingface.co/stabilityai/sd-vae-ft-mse). Basically every new realistic model has it already embedded.

## Comparison

![comparison](https://raw.githubusercontent.com/Zabriskije/CoreML-VAEs/main/comparison.png)
