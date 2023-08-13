# enlevo's posters 🌄

This is the collection of our event poster project files. It's just for archival/historical reasons but it can be interesting to anyone that finds it cool!


### Do I need to install anything? 🧱

We generally use [Blender](https://www.blender.org/).
Occasionally we also use [Stable Diffusion](https://github.com/CompVis/stable-diffusion) to generate images for ourselves. We use [AUTOMATIC1111's Web UI](https://github.com/AUTOMATIC1111/stable-diffusion-webui) with additional extensions:
- we're using the [`AyoniMix model`](https://civitai.com/models/4550/ayonimix) as a checkpoint.
- we're also using [`VAEs`](https://stable-diffusion-art.com/how-to-use-vae/).
- on top of these, we have [`ControlNet`](https://github.com/lllyasviel/ControlNet) to better control the output of our images.

If you *aren't* familiar with Stable Diffusion, we **highly recommend** giving the following link a read - https://stable-diffusion-art.com/automatic1111/.
You will need to know what Stable Diffusion *is* and how to use the Web UI to be able to use our parameters.

> [!NOTE]  
> You may find it easier to follow a video on setting all the Stable Diffusion models/checkpoints instead of reading.
> If so, simply watch https://www.youtube.com/watch?v=nBpD-RbglPw&ab_channel=AlbertBozesan.
> This is ***highly recommended***.


#### Okay... so how do I install all of those extensions? 🤔

Installing Blender is a breeze. You just need to go to https://www.blender.org/, download the executable depending on your OS and install it.

For Stable Diffusion, you first need to install AUTOMATIC1111'S Web GUI. Please check https://github.com/AUTOMATIC1111/stable-diffusion-webui#installation-and-running.


##### Installing `AyoniMix model` (and other models)

We are using [`AyoniMix`](https://civitai.com/models/4550/ayonimix) as our primary checkpoint/model. We are using this one primarily because it yields fair results. The process of installing models is the same for others. So if any example is using a different model, you can follow these same instructions.
Download `AyoniMix` and simply place it inside `models/Stable-diffusion` directory on your `AUTOMATIC1111 Web UI` instance. For more information, you can visit the documentation at https://github.com/civitai/civitai/wiki/How-to-use-models.


##### Adding `VAEs`

`VAE` is a small update that makes rendering small latent spaces better, mostly used in eyes. Stable Diffusion models have a default `VAE`. When people say they are downloading and using a `VAE`, they refer to using an *improved version* of it.
[Stability AI](https://stability.ai/) released two fine-tuned VAE decoders: `EMA` and `MSE`.

To install both of these and enable them on the Web UI, check https://stable-diffusion-art.com/how-to-use-vae/.


##### Installing `ControlNet`

`ControlNet` is a neural network that allows us to add more conditioning when generating images from text prompting. We can add various forms of conditioning in `ControlNet`. However, the most ued are *edge detection* and *human pose detection*, which are the ones we are going to install.
To install `ControlNet` on our Web UI, check https://stable-diffusion-art.com/controlnet/#Install_ControlNet_on_Windows_PC_or_Mac.

After installing and enabling `ControlNet` on the GUI, you will install the edge and pose detection extensions. For this, visit https://huggingface.co/webui/ControlNet-modules-safetensors/tree/main and download `control_canny-fp16.safetensors` and `control_openpose-fp16.safetensors`. Next, place these two files inside the `extensions/sd-webui-controlnet/models` directory. After reloading the Web UI, these models will be able in the `ControlNet` dropdown menus.

We *highly* suggest you to see the beginning of https://www.youtube.com/watch?v=dLM2Gz7GR44&t=587s&ab_channel=AlbertBozesan. It will give you a primer on how to enable these and get you started with `ControlNet`.


##### And you're done!

After this, you should be done with the default settings we are using. If there are any additional models/extensions being used in each folder, they will be specified. 
