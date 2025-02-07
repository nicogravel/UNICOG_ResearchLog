---
layout: default
title: "Retinotopy tutorial"
comments: true
---



# <span style="color:black">Tutorials</span>


<br>
<br>


<details>
  <summary><span style="color:#3382FF"> Set up research project codebook folder using Python, Sphinx and Github</span></summary>  

  First, we want to create a project folder that will contain the research code (Matlab, Python, Jupyter notebooks, etc), the data, the results and the documentation:

  ```
  ├── data
    └── raw
    └── processed
  ├── docs
  ├── results
  ├── reports
    └── figures
    └── notes
    └── references
    └── slides
  ├── code
    └── notebooks
    └── scripts
    └── tests
  ├── src
    └── data
    └── tasks
    └── models
    └── visualization
  ├── tests
  └── .gitignore
  └── environment.yml
  └── README.md
  ```

</details>

<br>
<br>

<details>
  <summary><span style="color:#3382FF"> Set up Conda environment from another computer</span></summary>  

  We can then recreate Conda environment from another computer:

  ```
  conda env create --name recoveredenv --file environment.yml
  ```

</details>

<br>
<br>
  
<details>
  <summary><span style="color:#3382FF"> Initialize or fork Github project</span></summary>  


  ```
  echo "# UNICOG_ResearchLog" >> README.md
  git init
  git add README.md
  git commit -m "1st commit"
  git branch -M main
  git remote add origin https://github.com/nicogravel/UNICOG_ResearchLog.git
  git push -u origin main
  ```

</details>

<br>
<br>
  
<details>
  <summary><span style="color:#3382FF"> Create a Python package</span></summary>  

  Create a setup.py file in the root of your project: 
  
  ```shell
  cd UNICOG_ResearchLog
  touch setup.py
  ```
  
  and add the following to setup.py:

  ```python
  from setuptools import find_packages, setup

  setup(
      name='myCodeIsYourCode',
      packages=find_packages(),
  )
  ```
  Create myCodeIsYourCode directory an add empty __init__.py file to it, together with a python file that prints "hello world" to your package:

  ```shell
  mkdir myCodeIsYourCode
  cd myCodeIsYourCode
  touch __init__.py
  echo "print('hello world')" > helloworld.py
  ```

  Go to the root directory and install your package from the root directory:

  ```shell
  cd ..
  pip install -e .
  sphinx-apidoc -f -o docs_local/source myCodeIsYourCode
  ```

Try it:  

  ```shell
  python
  ```
  
  ```python
  >>> import myCodeIsYourCode.helloworld
  hello world
  >>> exit()
  ```

</details>

<br>
<br>

<details>
  <summary><span style="color:#3382FF"> Generate project and code documentation using Sphinx</span></summary>  

  The folder *docs* will be used to generate [sphinx](https://www.sphinx-doc.org/en/master/index.html) docs, `cd` into this directory and run:

  ```shell
  pip install sphinx
  pip install sphinxcontrib-bibtex
  pip install sphinxcontrib-napoleon
  pip install -U sphinxcontrib-matlabdomain
  pip install sphinx-autodoc-typehints

  sphinx-quickstart
  make html
  ```

  We can then install [sphinx.ext.napoleon](https://www.sphinx-doc.org/ar/master/usage/extensions/napoleon.html), a *sphinx* plugin, to automatically read the *doctsrings* we have written as 'readme's' in the top of our python scripts, and add that content to the package dictionary of functions. To do so:


Edit *myCodeIsYourCode.rst*: add *:noindex:* to the end of the file, as follows:

```rst
Module contents
---------------

.. automodule:: myCodeIsYourCode
   :members:
   :undoc-members:
   :show-inheritance:
   :noindex:
```
 
Now enjoy building up your python package!

</details>
  
<br>
<br>
  
<details>
  <summary><span style="color:#3382FF"> Work: edit, make and commit</span></summary>  


  After these steps one wants to *make* the documentation locally. To build the documentation automatically, edit then the document modules.rst –if necessary, and do *make clean* followed by *make html*.

  ``` shell
  cd docs_local
  make clean
  make html
  ```

  After adding new code and document it as described, write docstrings, etc, do not forget to commit the changes to Github and update both the documentation and the package.

</details>
  
<br>
<br>
  
<details>
  <summary><span style="color:#c0392b"> Prepare and present retinotopy stimulus</span></summary>  

</details>

<br>
<br>
  
<details>
  <summary><span style="color:#c0392b"> Acquisition guidelines (triggers, sequences and other scanning parameters) </span></summary>  

</details>
  
<br>
<br>
    
<details>
  <summary><span style="color:#c0392b"> Data collection and organization into BIDS format</span></summary>  

</details>
  
<br>
<br>
   
<details>
  <summary><span style="color:#c0392b"> Preprocessing of the anatomical data</span></summary>  

</details>
     
<br>
<br>
  
<details>
  <summary><span style="color:#c0392b"> Preprocessing of the functional data</span></summary>  

</details>
  
<br>
<br>
  
<details>
  <summary><span style="color:#c0392b"> Coregistration of functional and anatomical</span></summary>  

</details>
  
<br>
<br>
    
<details>
  <summary><span style="color:#c0392b"> Population receptive field mapping (using pyprf)</span></summary>  

</details>
  
<br>
<br>
    
<details>
  <summary><span style="color:#c0392b"> Visualizing the results</span></summary>  

</details>
  
<br>
<br>
  
<details>
  <summary><span style="color:#c0392b"> Defining regions of interests</span></summary>  

</details>
  
<br>
<br>
    
<details>
  <summary><span style="color:#c0392b"> Extracting and grouping time series</span></summary>  

</details>
  
<br>
<br>
    
<details>
  <summary><span style="color:#c0392b"> Fitting GLMs</span></summary>  

</details>
    
<br>
<br>
  
<details>
  <summary><span style="color:#c0392b"> Connectivity estimates</span></summary>  

</details>
  
<br>
<br>
  
<details>
  <summary><span style="color:#c0392b"> Parse trials from another task</span></summary>  

</details>
  
<br>
<br>
  
<details>
  <summary><span style="color:#c0392b"> Compute a general linear model (GLM)</span></summary>  

</details>
  
<br>
<br>
  
<details>
  <summary><span style="color:#c0392b"> Work with anatomical or functional atlases</span></summary>  

</details>
  
<br>
<br>
  
<details>
  <summary><span style="color:#c0392b"> Laminar fMRI</span></summary>  

</details>
  
<br>
<br>
  
<details>
  <summary><span style="color:#c0392b"> Statistical assessments</span></summary>  

</details>
  
  
## <span style="color:lightblue">Comments🔨</span>

```{disqus}
```