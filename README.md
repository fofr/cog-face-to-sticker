# face-to-sticker

Turn any face into a sticker.

Run this model on Replicate:

https://replicate.com/fofr/face-to-sticker

Or run it in ComfyUI:

https://github.com/fofr/cog-face-to-sticker/blob/main/face-to-sticker-ui.json

![Arnold](https://replicate.delivery/pbxt/RZzqVdLsqSZgHtEefD00iMK8VuDif6iVmXlSbNeiAShPuHtJB/ComfyUI_00002_.png)

## Developing locally

Clone this repository:

```sh
git clone --recurse-submodules https://github.com/fofr/cog-face-to-sticker.git
```

Run the [following script](https://github.com/fofr/cog-comfyui/blob/main/scripts/clone_plugins.sh) to install all the custom nodes:

```sh
./scripts/clone_plugins.sh
```

### Running the Web UI from your Cog container

1. **GPU Machine**: Start the Cog container and expose port 8188:
```sh
sudo cog run -p 8188 bash
```
Running this command starts up the Cog container and let's you access it

2. **Inside Cog Container**: Now that we have access to the Cog container, we start the server, binding to all network interfaces:
```sh
cd ComfyUI/
python main.py --listen 0.0.0.0
```

3. **Local Machine**: Access the server using the GPU machine's IP and the exposed port (8188):
`http://<gpu-machines-ip>:8188`

When you goto `http://<gpu-machines-ip>:8188` you'll see the classic ComfyUI web form!
