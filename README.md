# Using Singularity in Local (Approach 4) for the reproducibility of SUMMA modeling

## Instruction 
1. Install Singularity in Ubuntu os.
- Installation description: https://sylabs.io/guides/3.5/admin-guide/installation.html#installation-on-linux

2. Create a Definition file to create a Singularity image
- Use a SUMMA and pySUMMA definition file in this GitHub
- https://github.com/DavidChoi76/SUMMA_Singularity_In_Rivanna/blob/master/summa_singularity.def

3. Create the Singularity image
```python
sudo singularity build summa3_singularity.sif summa_singularity.def
```
- Sinuglarity image in HydroShare: https://www.hydroshare.org/resource/6e8b3991a6dc46ba97c00688f7cb67de/

4. You can find `summa_singularity.sif` singularity image in the HS resource and download it in your local environment.

5. Download kernel.json file from this GitHub to your local environment
- https://github.com/DavidChoi76/SUMMA_Singularity_In_Rivanna/blob/master/kernel.json

6. Create SUMMA Jupyter Kernel 
```python
mkdir -p ~/.local/share/jupyter/kernels/summa
mv kernel.json ~/.local/share/jupyter/kernels/summa
```

7. Start JupyterLab and select summa Kernel

## If you don't want to create a Singularity image, you can use `kernel_copy.json` in this GitHub
- https://github.com/DavidChoi76/SUMMA_Singularity_In_Rivanna/blob/master/kernel_copy.json

1. Download `kernel_copy.json` in your local computer.

2. Change the name of `kernel_copy.json` to `kernel.json`  

3. Upload `kernel.json` to ‘/home/uvaID` folder of Rivanna

4. After that, follow step 8 above
- This method use the summa Singularity image in yc5ef's Singularity image

