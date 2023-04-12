
# 🍌 Stable Diffusion 2.1 Automatic 1111 for Banana

Deploy an API for AUTOMATIC1111's [Stable Diffusion WebUI](https://github.com/AUTOMATIC1111/stable-diffusion-webui) to generate images with **Stable Diffusion 2.1**.

Based on [https://app.banana.dev/templates/patienceai/automatic1111-sd-2-1-banana]()

## Model Inputs

### txt2img example

```
{
  "endpoint": "txt2img",
  "params": {
    "prompt": "banana",
    "negative_prompt": "low quality",
    "steps": 25,
    "sampler_name": "Euler a",
    "cfg_scale": 7.5,
    "seed": 42,
    "batch_size": 1,
    "n_iter": 1,
    "width": 768,
    "height": 768,
    "tiling": false
    
  }
}
```

(Only `prompt` is required.)

Output:

```
{
  "images": [
    "<base64 image>"
  ]
}
```

### img2img example

```
{
  "endpoint": "img2img",
  "params": {
    "prompt": "banana",
    "negative_prompt": "low quality",
    "steps": 25,
    "sampler_name": "Euler a",
    "cfg_scale": 7.5,
    "denoising_strength": 0.7,
    "seed": 42,
    "batch_size": 1,
    "n_iter": 1,
    "width": 768,
    "height": 768,
    "tiling": false
    "init_images": [
        "<base64 image>"
    ]
  }
}
```

(Only `prompt` and `init_images` are required.)

Output:

```
{
  "images": [
    "<base64 image>"
  ]
}
```
