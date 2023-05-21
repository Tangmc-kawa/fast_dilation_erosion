# fast_dilation_erosion

This program perform fast dilation_erosion(closing) on multi-label 3d image, which can fill gaps or smooth the edge of 3d objects in the 3d image. You can perform other operations if you like just by editing corresponding functions.

## Quickstart

### Create environment using conda or pip

```powershell
conda create --name <env_name> --file requirements.txt # <env_name> = image_process for example
pip install -r requirements.txt
```

## Strategy

This code accelerate closing performed on specific tiff labels file by cut the label to small cubes and close the cubes parallel on CPU.

The strategy can accelerate the process by 6 times or so based on data, CPU cores, memory size and current CPU occupation.
