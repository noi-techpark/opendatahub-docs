.. image:: /images/alpinebits-logo.png
   :scale: 30%
   :align: right

The AlpineBits Alliance strives to develop and to spread a standard
format to exchange tourism data. There are two datasets they developed
and keep up to date, that are of particular interest for |odh| users:
HotelData and DestinationData.
 
.. _ab-dd:

DestinationData
```````````````

The `AlpineBits DestinationData
<https://www.alpinebits.org/destinationdata/>`_ is a standardisation
effort to allow the exchange of information related to mountains,
events, tourism. Developed by the AlpineBits Alliance, Destination
Data relies on a number of standards (Including json, REST
API, Schema.org, OntoUML) to build the :strong:`AlpineBits
DestinationData Ontology`, the core result of the effort. The goal of
`DestinationData` it to provide a means to describe events, their
location, and additional information on them. For this purpose, the
DestinationData Ontology specifies a number of :strong:`Named
Entities` used to describe `Events` and `Event Series`, `Mountain
Areas`, `Places`, `Trails`, `Agents`, and so on.

The full specification of the ontology, including architecture of the
API and description of the datatypes defines can be found in the
official :strong:`Destination
Data specs` (`pdf
<https://www.alpinebits.org/wp-content/uploads/2021/05/AlpineBits-DestinationData-2021-04.pdf>`_
).

The :strong:`reference implementation` of AlpineBits DestinationData
is provided by |odh| and publicly available at the dedicated endpoint at
https://destinationdata.alpinebits.opendatahub.com/.

.. seealso:: More information and resources about AlpineBits
   DestinationData can be found on the `official page
   <https://www.alpinebits.org/destinationdata/>`_.

.. _ab-hd:

HotelData
`````````

The `AlpineBits HotelData <https://www.alpinebits.org/hoteldata/>`_ is
meant for data strictly related to hotels and booking, like Inventory
Basic, Inventory HotelInfo, and FreeRooms. This dataset can be access
from the dedicated endpoint at
https://alpinebits.opendatahub.com/AlpineBits/

.. seealso::

   The dedicated howto :ref:`ab-howto`.

   The `official page
   <https://www.alpinebits.org/destinationdata/>`_ of AlpineBits HotelData.
