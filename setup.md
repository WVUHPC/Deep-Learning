---
title: Setup
---

## Open On-Demand + JupyterLab + Deep Learning frameworks

All the examples and exercises proposed in this Workshop will be executed on Dolly Sods, the WVU HPC Cluster specialized for GPU processing.
To facilitate the interaction with the cluster we will use Jupyter Notebooks running on compute nodes on Dolly Sods and we will do that from a web interface thanks to Open On-Demand.

Open On-Demand is a web-based client portal, that hides all the complexity with web data pipelines and job submission and allow you to start using powerful computers for your research from a web interface, with minimal effort and fast learning curve.
On this episode you will not have to use Linux commands, you just need to execute one for the purpose of downloading all the materials for the tutorials but beyond that, your interaction will take place on a friendly web interface.
The job submission and web pipelines happen transparently to you.
You just need to declare the resources that you need and a new tab open with *JupyterLab* running remotely on one of the compute nodes.

Several technologies are involved here and it is important to understand how those different pieces are interconnected.

Open OnDemand is a web-based client, based on the Ohio Supercomputer Center’s proven “OSC On Demand” platform, that enables HPC centers to install and deploy advanced web and graphical interfaces for their users.
HPC resources are accessible from a web browser without the user having to install any special software or plugin.

The path for this tutorial is as follows. First we will demonstrate how to access the open on demand portal. Next we will create *JupyterLab*  sessions and opening a terminal and a file manager.

### Accessing the Dashboard

First, go to [Dolly Sods On Demand Dashboard](https://ondemand-ds.hpc.wvu.edu)

The first page you will see is asking for your credentials

<a href="{{ page.root }}/fig/OOD-CAS.png">
  <img src="{{ page.root }}/fig/OOD-CAS.png" alt="OOD-CAS" />
</a>

After entering your credentials and using your DUO authentication you will land on the Open On Demand Dashboard:

<a href="{{ page.root }}/fig/OOD-Dashboard.png">
  <img src="{{ page.root }}/fig/OOD-Dashboard.png" alt="OOD-Dashboard" />
</a>

From this dashboard you can launch interactive jobs, open terminals and access a file manager, we will see each of those operations in the next sections.

### Interactive applications

From the dashboard go to `Interactive Apps`. There are several options there, we will show *Jupyter-Lab Sessions* as this is the environment that will be used for the lessons.

#### Jupyter

For Jupyter click on `Interactive Apps > Jupyter Notebook`. A form is shown with all the options available to create the Jupyter session.

A good starting point is to select `CPython 3.7.4` as the Python version, select `standby` as the queue and `4 hours` as the wall time. There are options for alternative Python versions, queues and walltimes. A short description of each options is shown on the form.

<a href="{{ page.root }}/fig/OOD-jupyter1.png">
  <img src="{{ page.root }}/fig/OOD-jupyter1.png" alt="OOD-jupyter1" />
</a>

The next fields on the form ask for the number of cores, GPU cards, extra modules and the singularity image in case you have selected that as your Python version.

Notice that taking advantage of multiple cores depends on your code being able to use those cores. In the case of Python that usually means that your code is using `multiprocessing` module or you are using `numpy` with multi-threading capabilities. The usage of multiple cores is not something that happens automatically so if you are not sure asking for one core is enough. A similar situation happens with GPUs noticing that only the queue `comm_gpu_inter` give you access to GPUs for community nodes.

<a href="{{ page.root }}/fig/OOD-jupyter2.png">
  <img src="{{ page.root }}/fig/OOD-jupyter2.png" alt="OOD-jupyter2" />
</a>

Once you have customize the parameters for your Jupyter session, click on `Launch`. Open On demand will launch a new interactive session and when the interactive session is launched you will get a button to connect to the Jupyter notebook.

<a href="{{ page.root }}/fig/OOD-jupyter3.png">
  <img src="{{ page.root }}/fig/OOD-jupyter3.png" alt="OOD-jupyter3" />
</a>

The Jupyter session is launched on a compute node. The Jupyter interface shows as file manager where you can select a notebook to launch, upload one from your local computer or create a new Notebook, go to `New > Python 3` to create a new Jupyter notebook with Python 3 as kernel.

<a href="{{ page.root }}/fig/OOD-jupyter4.png">
  <img src="{{ page.root }}/fig/OOD-jupyter4.png" alt="OOD-jupyter4" />
</a>

The new notebook give you entries for typing Python instructions that are executed when you type `SHIFT-ENTER`

<a href="{{ page.root }}/fig/OOD-jupyter5.png">
  <img src="{{ page.root }}/fig/OOD-jupyter5.png" alt="OOD-jupyter5" />
</a>

{% include links.md %}
