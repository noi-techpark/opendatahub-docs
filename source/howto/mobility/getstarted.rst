.. _get-started-mobility:

How to Access Mobility Data With API v2
=======================================

The new :strong:`API v2` (see :ref:`the description <ninja api>`) for
the Mobility domain has simplified the access to data; among its
features, we recall that there is now one single endpoint from which
to retrieve data from all datasets.

The starting point for all actions to be carried out on the datasets
made available by the Open Data Hub team is the swagger mobility API
home page:

https://swagger.opendatahub.com/?url=https://mobility.api.opendatahub.com/v2/apispec
          
.. figure:: /images/mobility-swagger.png
   :scale: 33%
   :align: right

   The swagger interface of the Mobility API v2.

From this site, links provide access to documentation about data
licencing and use of the API; it is also possible to contact the Open
Data Hub team by sending an email to the issue tracker, to ask
questions, provide feedback, or to report issues.

When executing queries against the datasets, besides the output data,
you will always receive the `curl` command and the corresponding
direct URL, to be used for examples, in scripts. See
:ref:`mobility-api_examples`

Getting Started
---------------
  
In the API v2, the central concept is :strong:`Station`: all data come
from a given :literal:`StationType`, whose complete list can be
retrieved by simply opening the second method of the :strong:`Mobility
V2` controller, :strong:`/v2/{representation}`, then click on
:button:`Try it out` and then on `Execute`.

Station types in the resulting list can be used in the other methods to
retrieve additional data about each of them. To check which station
belongs to which datasets, you can check the list of
mobility-datasets.

.. _mobility-api_examples:

Example Queries
---------------

We use some of the techniques presented in section
:ref:`mobility-advanced` and the :dataset:`Parking dataset
<traffic/parking/>` to show a few simple queries and see the output
they provide.

We recall that the two :literal:`StationType`\s of that datasets are
`ParkingStation` and `ParkingSensor`; we start by retrieving all
`ParkingStation`\s, leaving all other options to their default values,
and then building two more refined queries, one using the select
clause and one using the where clause:

.. table::
   :align: center

   +-------------------------------------+-------------------------------------+
   | .. _fig-mobility-1:                 | .. _fig-mobility-2:                 |
   |                                     |                                     |
   | .. figure:: /images/mobility1.png   | .. figure:: /images/mobility2.png   |
   |    :scale: 33%                      |    :scale: 33%                      |
   |                                     |                                     |
   |    Querying all `ParkingStation`\s. |    The Output of query.             |
   +-------------------------------------+-------------------------------------+

.. hint:: You can copy to the clipboard or download the result of the
   query by clicking on the bottom-right corner icons.

If we would like to know the capacity of each of the parking lots, we
add `smetadata.municipality, smetadata.mainaddress,
smetadata.capacity` to the :strong:`select` clause:

.. table::
   :align: center

   +---------------------------------------+-------------------------------------+
   | .. _fig-mobility-3:                   | .. _fig-mobility-4:                 |
   |                                       |                                     |
   | .. figure:: /images/mobility3.png     | .. figure:: /images/mobility4.png   |
   |    :scale: 33%                        |    :scale: 33%                      |
   |                                       |                                     |
   |    Querying the capacity of parkings. |    The Output of query.             |
   +---------------------------------------+-------------------------------------+

Finally, we are interested only in the `ParkingStation`\s whose origin
is :strong:`not` FAMAS. We need therefore to add the following to the
:strong:`where` clause (we also remove the entry added for the
previous query in the :strong:`select` clause):

.. table::
   :align: center

   +-------------------------------------+-------------------------------------+
   | .. _fig-mobility-5:                 | .. _fig-mobility-6:                 |
   |                                     |                                     |
   | .. figure:: /images/mobility5.png   | .. figure:: /images/mobility6.png   |
   |    :scale: 33%                      |    :scale: 33%                      |
   |                                     |                                     |
   |    Non-FAMAS `ParkingStation`\s.    |    The Output of query.             |
   +-------------------------------------+-------------------------------------+

You can build more complex queries by simply adding more entries to
the Select and where clauses.
