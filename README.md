# SUMMA_Singularity_In_Rivanna

## Instruction 
1. Install Singularity in Ubuntu os.
- Installation description: https://sylabs.io/guides/3.5/admin-guide/installation.html#installation-on-linux

2. Create a Definition file to create a Singularity image
- Use a SUMMA and pySUMMA definition file in this GitHub
- https://github.com/DavidChoi76/SUMMA_Singularity_In_Rivanna/blob/master/summa_20200628.def

3. Create the Singularity image
```python
sudo singularity build summa_20200628.sif summa_20200628.def
```
- Sinuglarity image in HydroShare: https://www.hydroshare.org/resource/6e8b3991a6dc46ba97c00688f7cb67de/

4. Upload Singularity image
```python
scp summa_20200628.sif UVA_ID@rivanna.hpc.virginia.edu:/home/UVA_ID
```

5. Log in Rivanna (UVA HPC)
- Move to https://rivanna-portal.hpc.virginia.edu/pun/sys/dashboard
- Select Menu (Interactive APPs - JupyterLab)
- Select Option (Work Directory - HOME)

6. You can find `summa_20200628.sif` singularity image in ‘/home/UVA_ID` folder of Rivanna

7. Upload kernel.json file in this GitHub to ‘/home/uvaID` folder of Rivanna
- https://github.com/DavidChoi76/SUMMA_Singularity_In_Rivanna/blob/master/kernel.json

8. Create SUMMA Jupyter Kernel 
```python
mkdir -p ~/.local/share/jupyter/kernels/summa
mv kernel.json ~/.local/share/jupyter/kernels/summa
```

9. Start JupyterLab and select summa Kernel

## If you don't want to create a Singularity image, you can use `kernel_copy.json` in this GitHub
- https://github.com/DavidChoi76/SUMMA_Singularity_In_Rivanna/blob/master/kernel_copy.json

1. Download `kernel_copy.json` in your local computer.

2. Change the name of `kernel_copy.json` to `kernel.json`  

3. Upload `kernel.json` to ‘/home/uvaID` folder of Rivanna

4. After that, follow step 8 above
- This method use the summa Singularity image in yc5ef's Singularity image

