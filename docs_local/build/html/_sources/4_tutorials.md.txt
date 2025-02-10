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
  ├── docs
    └──.nojekyll
    └──index.html
  ├── docs_local
    └── processed
  ├── results
  └── .gitignore
  └── requirements.txt
  └── README.md
  ```

</details>

Inside docs/index.html we add:

  ```html
  <meta http-equiv="refresh" content="0; url=./html/index.html" />
  ```
The folder *docs/html* will be copied from *docs_local/build/html* once we build the docs, as explained below. Meanwhile, the folder *docs_local* is added to *.gitignore*.

<br>
<br>

<details>
  <summary><span style="color:#3382FF"> Set up pyenv environment (first install pyenv)</span></summary>  

  We can then create a python environment locally and install Sphinx:

  ```shell
  pyenv install 3.8.19
  pyenv virtualenv 3.8.19 Sphinx
  pyenv activate Sphinx
  pip install -r requirements.txt
  ```

</details>

The environment contains Sphinx 5.2.0 and the associated dependencies needed to make Disqus and Bibtex work. Then we can link our github page to our Disqus account and include a

<br>
<br>
  
<details>
  <summary><span style="color:#3382FF"> Initialize or fork Github project</span></summary>  


  ```
  echo "# ResearchLog" >> README.md
  git init
  git add README.md
  git commit -m "1st commit"
  git branch -M main
  git remote add origin https://github.com/.../ResearchLog.git
  git push -u origin main
  ```

</details>

<br>
<br>
  
<details>
  <summary><span style="color:#3382FF"> Create a Python package</span></summary>  

  Create a pyproject.toml file in the root of your project: 
  
  ```shell
  cd ResearchLog
  touch pyproject.toml.py
  ```
  
  and add the following to setup.py:

  ```toml
  [build-system]
  requires = ["setuptools", "wheel"]
  build-backend = "setuptools.build_meta"

  [project]
  name = "myCodeIsYourCode"
  version = "0.0.0"  # You can specify the version here
  description = "A short description of your project"
  readme = "README.md"
  requires-python = ">=3.8"


  [tool.setuptools.packages.find]
  where = ["."]

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
  Then in python:

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

  The folder *docs_local* will be used to generate the [sphinx](https://www.sphinx-doc.org/en/master/index.html) documentation. Then, we will copy the *build/html* to *docs*.

  ```shell
  cd /home/.../ResearchLog/docs_local/
  make clean; make html
  rsync -a --delete /home/.../ResearchLog/docs_local/build/html /home/.../ResearchLog/docs/
  ```

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

  After adding new code and document everything, write docstrings, etc, do not forget to commit the changes to Github and update both the documentation and the package. For example, if you write new python functions, do:

  ```shell
  pip install -e .
  sphinx-apidoc -f -o docs_local/source myCodeIsYourCode
  git add .
  git commit -m "replace setup.py for pyproject.toml, updates in docstrings"
  git push -u origin main'
  ```

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