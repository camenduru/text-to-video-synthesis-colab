🐣 Please follow me for new updates https://twitter.com/camenduru <br />
🔥 Please join our discord server https://discord.gg/k5BwmmvJJU

## 🚦 WIP 🚦

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/camenduru/text-to-video-synthesis-colab/blob/main/text_to_video_synthesis.ipynb)

## Tutorial
If you are using free colab please click `restart runtime` after each generation (pipe using lots of ram)


![Screenshot 2023-03-19 234114](https://user-images.githubusercontent.com/54370274/226207884-3052f5a8-862b-4785-85fe-9f6aa26be879.png)
![Screenshot 2023-03-19 234144](https://user-images.githubusercontent.com/54370274/226207887-d9dec199-162e-4992-882b-a4f05bf182c6.png)

if you want you can edit `configuration.json` under `/root/.cache/modelscope/hub/damo/text-to-video-synthesis/configuration.json`
```json
{   "framework": "pytorch",
    "task": "text-to-video-synthesis",
    "model": {
        "type": "latent-text-to-video-synthesis",
        "model_args": {
            "ckpt_clip": "open_clip_pytorch_model.bin",
            "ckpt_unet": "text2video_pytorch_model.pth",
            "ckpt_autoencoder": "VQGAN_autoencoder.pth",
            "max_frames": 16,
            "tiny_gpu": 1
        },
        "model_cfg": {
            "unet_in_dim": 4,
            "unet_dim": 320,
            "unet_y_dim": 768,
            "unet_context_dim": 1024,
            "unet_out_dim": 4,
            "unet_dim_mult": [1, 2, 4, 4],
            "unet_num_heads": 8,
            "unet_head_dim": 64,
            "unet_res_blocks": 2,
            "unet_attn_scales": [1, 0.5, 0.25],
            "unet_dropout": 0.1,
            "temporal_attention": "True",
            "num_timesteps": 1000,
            "mean_type": "eps",
            "var_type": "fixed_small",
            "loss_type": "mse"
        }
    },
    "pipeline": {
        "type": "latent-text-to-video-synthesis"
    }
}
```

## Main Repo
https://www.modelscope.cn/models/damo/text-to-video-synthesis/summary
https://github.com/modelscope/modelscope

## Models License
Apache License 2.0

## Examples
<table><tbody><tr><td><center>
A giraffe underneath a microwave.
<br>
<img src="https://user-images.githubusercontent.com/54370274/226195676-edd1b5da-906c-445e-b6a5-612a4dbfb1fe.gif" alt="A giraffe underneath a microwave." style="width: 300px;">
</center></td><td><center>
A goldendoodle playing in a park by a lake.
<br>
<img src="https://user-images.githubusercontent.com/54370274/226195681-f54e38c2-1936-4153-b145-f238853a4df0.gif" alt="A goldendoodle playing in a park by a lake." style="width: 300px;">
</center></td><td><center>
A panda bear driving a car.
<br>
<img src="https://user-images.githubusercontent.com/54370274/226195685-e188e342-5c6d-4e68-ab3f-32e2d7d30e34.gif" alt="A panda bear driving a car." style="width: 300px;">
</center></td></tr><tr><td><center>
A teddy bear running in New York City.
<br>
<img src="https://user-images.githubusercontent.com/54370274/226195689-318e0e5e-ee14-4443-84a0-a3c8b07b8aed.gif" alt="A teddy bear running in New York City." style="width: 300px;">
</center></td><td><center>
Drone flythrough of a fast food restaurant 
<br>on a dystopian alien planet.
<br>
<img src="https://user-images.githubusercontent.com/54370274/226195692-0853b49a-9cd5-4f9b-84e6-2288632ca2f7.gif" alt="Drone flythrough of a fast food restaurant on a dystopian alien planet." style="width: 300px;">
</center></td><td><center>
A dog wearing a Superhero outfit with red cape 
<br>flying through the sky.
<br>
<img src="https://user-images.githubusercontent.com/54370274/226195699-14b16290-15e7-4577-aaae-ea16c15f44c3.gif" alt="A dog wearing a Superhero outfit with red cape flying through the sky." style="width: 300px;">
</center></td></tr><tr><td><center>
Monkey learning to play the piano.
<br>
<img src="https://user-images.githubusercontent.com/54370274/226195867-f6b079ff-ee1a-4dea-928c-dbf28d4a656e.gif" alt="Monkey learning to play the piano." style="width: 300px;">
</center></td><td><center>
A litter of puppies running through the yard.
<br>
<img src="https://user-images.githubusercontent.com/54370274/226195930-1fd957df-f403-4ae3-9a85-f4f954c82f5a.gif" alt="A litter of puppies running through the yard." style="width: 300px;">
</center></td><td><center>
Robot dancing in times square.
<br>
<img src="https://user-images.githubusercontent.com/54370274/226209983-eae320fc-078e-4e62-9989-d97beb9477eb.gif" alt="Robot dancing in times square." style="width: 300px;">
</center></td></tr></tbody></table>
