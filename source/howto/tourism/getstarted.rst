
.. _tourism-data-howto:
   
How to access Tourism Data?
===========================

The purpose of this howto is to quickly introduce the alternatives to
access datasets in the Tourism domain. Technical information about the
datasets can now be found in section :ref:`tourism-tech`.

Swagger Interface
-----------------

All the APIs available for the tourism domain can be accessed from the
same URL through their Swagger user interface:

https://tourism.api.opendatahub.com/swagger/index.html

.. hint:: Check section tourism-datasets for direct URLs to the
   datasets.

With the introduction on the Tourism API graphic interface of a newer
swagger version, supplying and storing the token has become easier,
making older procedures deprecated or obsolete. Moreover, in the new
GUI, for every API method is shown whether it can provide Open Data as
a result and if not, it will be necessary to authenticate.

.. _data-access-tourismAPI:

Authentication with Swagger
~~~~~~~~~~~~~~~~~~~~~~~~~~~

Authentication is easy and, unlike it happened in the past, it does
require only to supply your credentials. From the swagger UI, click on
the :strong:`Authorize` button on the right-hand side of the page
(shown in the bottom-right corner in :numref:`tourism-ui`).

.. _tourism-ui:

.. figure:: /images/tourism-01.png
   :scale: 33%
   :align: center

   The new Swagger UI for Tourism domain.

A dialog window will pop up; here, supply your username and password,
and click on :strong:`Authorize`. It is not necessary to change any
other parameter.

.. _tourism-auth:

.. figure:: /images/tourism-02.png
   :scale: 33%
   :align: center

   Providing credentials for authentication.

After a few seconds a new dialog replaces the one used for
authentication, whose most important bit is the :strong:`Authorized`
word, that means you are now authenticated. No additional step is now
necessary: the browser will remember the token. Click on
:strong:`Close` to close the dialog window start browsing the Tourism
data.

.. _tourism-auth-ok:

.. figure:: /images/tourism-03.png
   :scale: 33%
   :align: center

   Successful authentication.

To log out, click again on :strong:`Authorize` in the Swagger UI (see
:numref:`tourism-ui`), then on :strong:`Logout`.

Browsing API Datasets
---------------------

The data in the API can be browsed at the following URL:

https://tourism.api.opendatahub.com/v1/

.. note:: You may need to install a `JSON browser plugin` for your
   browser to browse the datasets in this way.

.. _tourism-api-browse:

.. figure:: /images/API-browser.png
   :scale: 33%
   :align: center

   Browsing Tourism API

Here, every link can be clicked to navigate through the various
datasets and the data they contain. A lot of metadata and information
is provided for every object in the dataset, depending on the type of
object. For example, The starting point to browse the API, shown in
:numref:`tourism-api-browse` includes for each datas licensing
information, a description, an ID, the API and swagger URLs, while a
dataset shows the total number of items and of pages it contains, the
current page, pointers to previous and next page, and the items
themselves.


Using Command Line Tools
------------------------

If you plan to access the API methods with command line tools like
:command:`curl` or :command:`wget`, or only from scripts, you need to
add an authentication header to each call. For example, using curl:

.. code-block:: bash

   ~# curl -X GET --header 'Accept: application/json' \
   --header 'Authorization: Bearer vLwemAqrLKVKXsvgvEQgtkeanbMq7Xcs' \
   'https://tourism.api.opendatahub.com/v1/Gastronomy'

.. note:: The string of the token is shortened for the sake of
   clarity. 

   

It is important to mention that the authorisation header reaquires the
following syntax: :strong:`Authorization: Bearer`, followed by the
whole `string` of the token.

One you have retrieved the data, which come in JSON format, you can
process and manipulate them with a tool like `jq
<https://github.com/stedolan/jq>`_.

