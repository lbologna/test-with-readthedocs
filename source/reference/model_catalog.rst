.. _model-catalog-app:

#################
Model Catalog app
#################

The HBP Model Catalog contains information about models developed and/or used within the ecosystem of tools
provided by the HBP Platforms.

The Model Catalog app can be installed in any Collab workspace, and can be used:

- to search for models of a given brain region, cell type, modelling scale, etc.
- to provide information/metadata about a model
- to register a model and obtain a unique identifier for use with other tools and workflows, such as model validation


Adding the app to your Collab
-----------------------------

As shown in the screenshot below, click on the "ADD" button in the left-hand navigation bar,
then search for "model catalog", and click on "Add to Navigation" to install the app.

.. image:: images/model_catalog_add_to_navigation.png
   :width: 569
   :align: center

Choose which models to view
---------------------------

When you first click on "Model Catalog" in the navigation bar, you will see a configuration screen with a group of drop-down lists.
This allows you to filter the catalog, and show only the model(s) that is/are relevant to your Collab.

.. image:: images/model_catalog_configure.png
   :width: 429
   :align: center

When you have finished, click "Save", and then click the "X" icon to close the configuration view.
This then shows a list of the models corresponding to the criteria you have selected.
These models can be further filtered dynamically using the drop-down lists at the top of the model list.

.. image:: images/model_catalog_hippocampus_models.png
   :width: 680
   :align: center

Viewing an individual model
---------------------------

Clicking on a single model in the list brings up a detailed view of that model,
including a potentially detailed description, metadata about the brain region, cell type, etc., being modelled,
and references to different versions of the model (which may be versions in a Git repository, ModelDB entries,
zip archives, etc.)

.. image:: images/model_catalog_model_detail_kali_freund.png
   :width: 538
   :align: center

Editing a model
---------------

For access-control purposes, each model is associated with a "home" Collab.
If you are a member of that Collab you can edit the details of the models.

Note that the model description field accepts Markdown_ syntax for adding sub-headings, lists, italics, bold text,
hyperlinks, images, etc.

Models may also be marked as public or private.
Private models may only be viewed by people who are members of the model's home Collab.

.. image:: images/model_catalog_model_edit_kali_freund.png
   :width: 519
   :align: center

Adding a model to the Catalog
-----------------------------

At the upper-left of the model list is a "New model" button,
which opens a form allowing any user to register a model in the Catalog.

The Collab in which the model is first created is the "home" Collab of that model,
and only members of that Collab can subsequently edit the model.

When you create a model, it receives a unique ID, a long hexadecimal string
which is used to identify the model in some other tools and workflows in the HBP Platforms.
To avoid having to type this long, difficult-to-remember, ID each time,
you can also create a short alias for the model.

.. image:: images/model_catalog_model_create.png
   :width: 531
   :align: center

Access privileges to models in the model catalog
------------------------------------------------

* Collabs on the HBP Collaboratory can be either public or private. Public
  Collabs can be accessed by all registered users, whereas private Collabs
  require the user to be granted permission for access.

* Models are created inside specific Collab instances of the *Model Catalog* app.
  The particular app inside which a model was created is termed its *host app*.
  Similarly, the Collab containing the *host app* is termed the *host Collab*.

* Models can be set as public or private. If public, the model and its associated
  results are available to all users. If private, it can only be seen by users who
  have access to the *host Collab*. See table below for a summary of access privileges.

* No information can be deleted from the *Model Catalog*
  app. In the future, an option to *hide* data will be implemented. This will offer
  users a functionality similar to deleting, while retaining the data in the
  database back-end.

* Models and model instances can be edited as long as
  there are no results associated with them. Results can never be edited!

 .. raw:: html

   <div>
   <style type="text/css">
   .tg  {border-collapse:collapse;border-spacing:0;}
   .tg td{font-family:Arial, sans-serif;font-size:14px;padding:11px 8px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
   .tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:11px 8px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
   .tg .tg-6v17{font-weight:bold;font-size:14px;background-color:#d6eebe;border-color:inherit;text-align:center;vertical-align:top}
   .tg .tg-ynlj{font-size:14px;background-color:#ffffff;border-color:inherit;text-align:center;vertical-align:top}
   .tg .tg-5jl3{font-style:italic;font-size:14px;background-color:#c3b696;border-color:inherit;text-align:center;vertical-align:top}
   .tg .tg-c3ow{border-color:inherit;text-align:center;vertical-align:top}
   .tg .tg-iu76{font-weight:bold;font-size:18px;background-color:#ffce93;border-color:inherit;text-align:center;vertical-align:top}
   .tg .tg-7xg9{font-weight:bold;font-style:italic;font-size:16px;background-color:#ffffc7;border-color:inherit;text-align:center;vertical-align:top}
   .tg .tg-ecuv{font-weight:bold;font-size:18px;background-color:#ffce93;border-color:inherit;text-align:center}
   </style>
   <table class="tg">
     <tr>
       <th class="tg-c3ow" colspan="2" rowspan="3"></th>
       <th class="tg-iu76" colspan="6">Collab (Private/Public)</th>
     </tr>
     <tr>
       <td class="tg-7xg9" colspan="3">Collab Member</td>
       <td class="tg-7xg9" colspan="3">Not Collab Member</td>
     </tr>
     <tr>
       <td class="tg-5jl3">View (GET)</td>
       <td class="tg-5jl3">Create (POST)</td>
       <td class="tg-5jl3">Edit (PUT)</td>
       <td class="tg-5jl3">View (GET)</td>
       <td class="tg-5jl3">Create (POST)</td>
       <td class="tg-5jl3">Edit (PUT)</td>
     </tr>
     <tr>
       <td class="tg-ecuv" rowspan="2">Model</td>
       <td class="tg-7xg9">Private</td>
       <td class="tg-6v17">Yes</td>
       <td class="tg-6v17">Yes</td>
       <td class="tg-6v17">Yes</td>
       <td class="tg-ynlj">No</td>
       <td class="tg-ynlj">No</td>
       <td class="tg-ynlj">No</td>
     </tr>
     <tr>
       <td class="tg-7xg9">Public</td>
       <td class="tg-6v17">Yes</td>
       <td class="tg-6v17">Yes</td>
       <td class="tg-6v17">Yes</td>
       <td class="tg-6v17">Yes</td>
       <td class="tg-ynlj">No</td>
       <td class="tg-ynlj">No</td>
     </tr>
   </table>
   </div>


.. _Markdown: https://daringfireball.net/projects/markdown/syntax
