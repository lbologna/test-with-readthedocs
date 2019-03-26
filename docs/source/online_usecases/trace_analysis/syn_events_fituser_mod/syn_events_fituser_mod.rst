.. _syn_events_fit_user_mod:

######################################
Synaptic events fitting (user’s model)
######################################

This Use Case allows a user to fit synaptic events using user’s data and model.

Selecting this use case, two Jupyter Notebooks are cloned in a private existing/new Collab.
The cloned Notebooks are:

**************************************************
Synaptic events fitting with a user model - Config
**************************************************

It allows the user to:

1. Select a local experimental file

.. container:: bsp-container-center

    .. image:: images/select_exp.png
        :width: 450px
        :align: center

|

At this time, the only accepted format for the experimental file is a text file with time in the first column and individual traces in successive columns. All columns must be of the same length

|

2. Select a local mod file

.. container:: bsp-container-center

    .. image:: images/select_mod.png
        :width: 450px
        :align: center

|

We assume that the user knows what we are talking about here, and that the 
uploaded mod file has been already tested by the user in preliminary 
simulations. The program does not perform checks on this. An invalid file will 
result in errors at NEURON compilation time

All other parameters that are not fitted have their default value as 
defined in the mod file.

|

3. Fill in the form with the values needed to write a configuration file: the 
   number of traces in the experimental file, the protocol (voltage clamp 
   amplitude and reversal potential of the synapse), the name of the parameters 
   to be fitted, their initial values and the allowed variation range, 
   exclusion rules, and an optional set of dependencies for other parameters. 
   Typical values are shown in the figure below


.. container:: bsp-container-center

    .. image:: images/fill_form.png
        :width: 450px
        :align: center

|

.. container:: bsp-container-center

 .. image:: images/initial_values.png
     :width: 450px
     :align: center

|

.. container:: bsp-container-center

 .. image:: images/dependencies.png
     :width: 450px
     :align: center

|

4. Configure the parameters of the optimization job: number of nodes, number of cores and runtime. Run the fitting procedure using UNICORE authentication on JURECA or MARCONI, or on the NSG, and check the status of the job

On JURECA the number of nodes, number of CPUs per node and runtime are set by default to 2, 24 and 10m respectively

|

On MARCONI the number of nodes, number of CPUs per node and runtime are set by default to 2, 36 and 10m respectively

|

The user needs to be aware of the limitations imposed by each HPC system on resources

|

On the NSG the number of nodes, number of cores and runtime are set by default to 2, 24 and 0.5 (hours) respectively. The maximum number of nodes available per job is 72. If you require more than 72 nodes please contact nsghelp@sdsc.edu. The maximum number of cores required per node is 24.

|

.. container:: bsp-container-center

 .. image:: images/select_hpc.png
     :width: 300px
     :align: center

|

.. container:: bsp-container-center

 .. image:: images/run_all_traces.png
     :width: 200px
     :align: center

|


.. container:: bsp-container-center

 .. image:: images/set_CPU_nodes.png
     :width: 400px
     :align: center

|

.. container:: bsp-container-center

 .. image:: images/login.png
     :width: 400px
     :align: center

|

.. container:: bsp-container-center

 .. image:: images/job_submitted.png
     :width: 400px
     :align: center

|

Note that when the job is submitted through UNICORE, the user can specify a title for the job and the account to use for submitting the job on the HPC.

|

.. container:: bsp-container-center

 .. image:: images/unicore.png
     :width: 300px
     :align: center

|

Note that when the job is submitted through NSG, the user can see the 
submission date converted to CET time next to the status of the job. This will 
be useful in the analysis notebook in order to fetch the job.

|

.. container:: bsp-container-center

 .. image:: images/NSGstatus.png
     :width: 300px
     :align: center

|

The user can choose to fit all experimental traces 100 times, a single trace 20 
times or use a demo version where a trace is fitted 5 times. For the single 
trace and the demo version the user can choose the trace to be fitted.

Once the job is completed, the output files will be in the Collab storage under 
different directories, according to the system used.

JURECA: results are saved under the results/output_submissionTime folder;

|

MARCONI: results are saved under the resultsMarconi/output_submissionTime folder;

|

NSG results are saved under the resultsNSG/output_submissionTime folder.

|

5. If you are interested in the code, click on the “Click here to toggle on/off the source code” button

.. container:: bsp-container-center

    .. image:: images/toggle_button.png
        :width: 300px
        :align: center

|

6. If you want to start a new fitting from the beginning, click on the “Click here to start a new fit” button.

.. container:: bsp-container-center

    .. image:: images/Restart.png
        :width: 300px
        :align: center

|

**************************************************
Synaptic events fitting with user model - Analysis
**************************************************

.. include:: ../syn_events_fit_analysis/syn_events_fit_analysis.rst
