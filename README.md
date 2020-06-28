# SUMMA_Singularity_In_Rivanna

## Instruction 
Install Singularity in Ubuntu os.
Installation description: https://sylabs.io/guides/3.5/admin-guide/installation.html#installation-on-linux

1. Create a Definition file to create a Singularity image
- Use a SUMMA and pySUMMA definition file in this GitHub

2. Create the Singularity image
```python
sudo singularity build summa_20200628.sif summa_20200628.def
```

3. Upload Singularity image
```python
scp summa_20200628.sif uvaID@rivanna.hpc.Virginia.edu:/home/uvaID
```

4. Log in Rivanna (UVA HPC)
- Move to https://rivanna-portal.hpc.virginia.edu/pun/sys/dashboard
- Select Menu (Interactive APPs - JupyterLab)
- Select Option (Work Directory - HOME)

5. You can find `summa_20200628.sif` singularity image in ‘/home/uvaID` folder

6. Upload kernel.json file in  ‘/home/uvaID` folder

7. Create SUMMA Jupyter Kernel 
```python
mkdir -p ~/.local/share/jupyter/kernels/summa
Mv kernel.json ~/.local/share/jupyter/kernels/summa
```

8. Start JupyterLab and select summa Kernel
