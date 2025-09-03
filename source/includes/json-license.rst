.. _license-json-records:

License of the JSON Responses
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Whenever you query the data in the tourism domain of the |odh|\, the snippet that you
retrieve always includes a block of information called
:literal:`LicenseInfo`, similar to the following one:

.. code-block:: json
   :linenos:
   :emphasize-lines: 3

   {
      "LicenseInfo": {
        "Author": "",
          "License": "CC0",
          "ClosedData": false,
          "LicenseHolder": "https://www.lts.it"
      }
   }

The highlighted line shows a licence, which in this case is
:strong:`CC0`, i.e., public domain and therefore freely reusable.

This block is always included as a child node within a JSON record
that starts with an ID and a number of additional information, which
may include also hyperlinks to resources that are external to the
|odh|\, like in the following snippet--shortened for the sake of
simplicity, which refers to a webcam and contains a link to an
external provider where to find actual resources (e.g., streams and
images) from that webcam.

.. code-block:: json
   :linenos:
   :emphasize-lines: 4-5

   {
     "Id": "D3659E1F111C4CDB2EC19F8FC95118B7",
     "Active": true,
     "Streamurl": null,
     "Webcamurl": "https://webtv.feratel.com/webtv/?&pg=5EB12424-7C2D-428A-BEFF-0C9140CD772F&design=v3&cam=6323&c1=0",
     "LicenseInfo": {
       "Author": "",
       "License": "CC0",
       "ClosedData": false,
       "LicenseHolder": "https://www.lts.it"
     }
   }

Whenever hyperlinks like the one shown in line :strong:`5` above
appear, it must not be implied that the license mentioned in the
:literal:`LicenseInfo` block (again, CC0) is applied to them:
everything contained in that link may be covered by a different
licence.

Indeed, the :strong:`Licence` mentioned in :literal:`LicenseInfo`
nodes refer only to content of the parent node--i.e., the one that
starts with :strong:`"Id"`, not to the content of any of the other
children nodes, including :literal:`Streamurl` and
:literal:`Webcamurl`.
