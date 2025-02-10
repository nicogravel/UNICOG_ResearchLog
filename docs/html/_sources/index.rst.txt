----------------
**Tutorial I:**    
----------------

Documenting research with *Sphinx*
###################################
  
*************************************************************
**Goal:** keep track of progress during the research process.   
*************************************************************

The tutorial is an adaptation of `The Good Research Code Handbook <https://goodresearch.dev>`_, by Patrick Mineault. It is delivered as a Github repo based on `Sphinx <https://www.sphinx-doc.org/en/master/>`_, `Markdown <https://daringfireball.net/projects/markdown/>`_ and `reStructuredText <https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site>`_ (rendered using `Github pages <https://jekyllrb.com/docs/github-pages/>`_). Its purpose is to provide us with a scaffold for a personalised *research log* that can be easily adapted to one's individual needs.     
  
  
Before we begin, I wanted to share a couple of stories, both as a primer and as an example of how to use the resource, its functionalities, etc. 
    
Recently, I encountered an article discussing the ongoing replication crisis in biology :footcite:p:`Oza_2023`. Why so often, the article stressed, results obtained by different teams using the same data (and following the same inquiries) are difficult to replicate :footcite:p:`Nezer_2020`. According to the article, scientists tend to integrate their beliefs into their hypothesis-making machinery (*i.e.* in the form of a *toolbox*) to every problem they stumble upon in the field. While the need for collective consensus is clear, potentially diverging decisions taken during a statistical assessment may bring forth confusion rather than clarity. With all its good intentions, excess trust in a method should not lead us into the realm of extreme scientific belief or `scientificism/scientism <https://www.merriam-webster.com/dictionary/scientism>`_ (i.e. *the urge to trust on the temporary answers our good ol' metric provide rather than the underlying problem that inspired them in first place*). Coincidentally, while trying to reach consensus in my own work, I stumbled upon another noteworthy piece in the now defunct Twitter. The `post <https://twitter.com/lakens/status/1718654122516156777>`_ provided the much needed, *so zu sagen*, plumber's perspective: 

  *Statisticians should be less like priests and more plumbers. I don't care what you personally believe is the right way to do things - if I have a specific problem, I want to know all possible solutions that might fix it, what their limitations are, and how much each would cost.*                     `Daniël Lackens <https://twitter.com/lakens>`_


If reflecting on this wasn't already challenging, the so-called *Sufficiency and Necessity Principle* then came to mind. I remember having heard about it some years ago during a talk about the integration of causality in enactive approaches by `Shaun Gallagher <https://en.wikipedia.org/wiki/Shaun_Gallagher>`_. One of these concepts often discussed in the context of practical inference of causality. The principle is based on the idea that if a certain variable is necessary for a certain outcome, then the absence of that variable will lead to the absence of the outcome. On the other hand, if a variable is sufficient for an outcome, then the presence of that variable will lead to the presence of the outcome, as shown in the following diagram: 

|
    
.. image:: /figures/Eaton_1985.png
      :width: 750
      :align: center 
        
  
Both anecdotes matter to us, as the process of experimental design and statistical inference that we engage in often involves the equivalent of  "deactivating" or "activating" a *region of interest* using various tools (*e.g.* perceptual/cognitive/behavioral tasks, pharmacological interventions, animal models, *etc...*) and recording modalities (*e.g.* electrophysiology, fMRI, *etc...*), measuring changes in behavior before and after manipulation, and then drawing causal links between variables. If deactivation leads to suppression of the desired outcome while activation induces that outcome, a causal link can be inferred. However, it's essential to consider potentially *hidden* variables that may influence this relationship  :footcite:p:`Eaton_1985`.  
  
For a more detailed explanation of its limitations, I recommend this recent article by Grace Lindsay on The Transmitter: `Claims of necessity and sufficiency are not well suited for the study of complex systems <https://doi.org/10.53053/IHMY3378>`_.
  
  


**********
Comments
**********
.. disqus::
  
    
**********
Content
**********
.. toctree::
      :maxdepth: 2
      :numbered:          

      1_intro
      2_okr
      3_results
      4_tutorials
      5_refs
      

   
**************
Python package
**************

.. toctree::
    :maxdepth: 1
    :caption: Codebook:

    modules

Indices
=======

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

 
      
**********
References
**********

.. footbibliography::
