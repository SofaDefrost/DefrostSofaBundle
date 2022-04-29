# RoboSoft2022

This is a bundle of SOFA binaries specially prepared for RoboSoft 2022 workshop.  
The bundle contains:
- sofa-framework/sofa@robosoft2022 (snapshot from master, at commit 479fd27b, 30 March 2022)
- sofa-framework/SofaPython3@robosoft2022 (synced with master)
- SofaDefrost/STLIB@robosoft2022 (synced with master)
- SofaDefrost/SoftRobots@robosoft2022 (synced with master)
- sofabot/SoftRobots.Inverse@robosoft2022 (private repository)

----------------------------------------

## Windows

To open a Terminal: Start > type "cmd" > press Enter

### Install the dependencies

1. Install **[Microsoft Visual C++ 2017 Redistributable](https://aka.ms/vs/15/release/vc_redist.x64.exe)**.

2. Install **python + pip**  
   Open a Terminal and run `python -V`  
   If the command shows a version that is in [3.7 ; 3.9], skip to step 3.  
   Else, install one of these compatible versions:  
   - [python 3.7 (amd64)](https://www.python.org/ftp/python/3.7.9/python-3.7.9-amd64.exe)  
   - [python 3.8 (amd64)](https://www.python.org/ftp/python/3.8.10/python-3.8.10-amd64.exe)  
   - [python 3.9 (amd64)](https://www.python.org/ftp/python/3.9.12/python-3.9.12-amd64.exe)  
   
   Make sure to enable **pip installation** and **addition to PATH**.  
   Open a Terminal and run `python -V` again. You should see the version of python you just installed.

3. Install **numpy + Scipy**  
   Open a Terminal and run `python -m pip install numpy scipy`

4. You may need to edit the system environment variables:
   - Create a system variable SOFA_ROOT and set it to <SOFA-install-directory>
   - Create a system variable PYTHON_ROOT and set it to <Python3-install-directory>
   - Create a system variable PYTHONPATH and set it to %SOFA_ROOT%\plugins\SofaPython3\lib\python3\site-packages
   - Edit the system variable Path and add at the end ;%PYTHON_ROOT%;%PYTHON_ROOT%\DLLs;%PYTHON_ROOT%\Lib;%SOFA_ROOT%\bin;

### Install the SOFA RoboSoft bundle

Go to https://github.com/SofaDefrost/RoboSoft2022/releases/tag/release-main  
Download the ZIP corresponding to your system and the version of python you just installed.  
Extract the ZIP on your Desktop.

### Execute runSofa

Open a Terminal and run  
```cmd
cd %HOMEPATH%\Desktop\SOFA_robosoft2022_*
set PYTHONPATH=plugins\SofaPython3\lib\python3\site-packages
bin\runSofa.exe
```

----------------------------------------

## Ubuntu

### Install the dependencies

1. Install **libopengl0**  
   `sudo apt install libopengl0`
   
2. Install **python + pip**  
   Open a Terminal and run `python3 -V`  
   If the command shows a version that is in [3.7 ; 3.10], skip to step 3.  
   Else, search which compatible version is proposed by your package manager:  
   ```bash
   sudo apt update
   sudo apt info python3 | grep -i 'version: '
   ```
   If the proposed version is in [3.7 ; 3.10] then install it  
   ```bash
   sudo apt install python3-dev python3-distutils
   curl -L https://bootstrap.pypa.io/pip/get-pip.py --output /tmp/get-pip3.py
   python3 /tmp/get-pip3.py
   ```
   Open a Terminal and run `python3 -V` again. You should see the version of python you just installed.

3. Install **numpy + scipy**  
   Open a Terminal and run  
   ```bash
   python3 -m pip install --upgrade pip
   python3 -m pip install numpy scipy
   ```

### Install the SOFA RoboSoft bundle

Go to https://github.com/SofaDefrost/RoboSoft2022/releases/tag/release-main  
Download the ZIP corresponding to your system and the version of python you just installed.  
Extract the ZIP on your Desktop.

### Execute runSofa

Open a Terminal and run  
```bash
cd ~/Desktop/SOFA_robosoft2022_*
export PYTHONPATH=plugins/SofaPython3/lib/python3/site-packages 
./bin/runSofa.exe
```

----------------------------------------

## MacOS

### Install the dependencies

1. Install **python + pip**  
   Open a Terminal and run `python3 -V`  
   If the command shows a version that is in [3.7 ; 3.10], skip to step 2.  
   Else, search which compatible version is proposed by your package manager:   
   ```bash
   brew update
   brew info python
   ```
   If the proposed version is in [3.7 ; 3.10] then install it  
   ```bash
   brew install python
   ```
   Open a Terminal and run `python3 -V` again. You should see the version of python you just installed.  

2. Install **numpy + scipy**   
   Open a Terminal and run  
   ```bash
   python3 -m pip install --upgrade pip
   python3 -m pip install numpy scipy
   ```

### Install the SOFA RoboSoft bundle

Go to https://github.com/SofaDefrost/RoboSoft2022/releases/tag/release-main  
Download the ZIP corresponding to your system and the version of python you just installed.  
Extract the ZIP in your User folder.  

### Execute runSofa

Open a Terminal and run  
```bash
cd ~/SOFA_robosoft2022_*
export PYTHONPATH=plugins/SofaPython3/lib/python3/site-packages 
./bin/runSofa.exe
```
