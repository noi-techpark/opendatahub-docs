Unlike browser access, that provides an interactive access to data,
with the option to incrementally refine a query, command line access
proves useful for non-interactive, one-directional, and quick data
retrieval in a number of scenarios, including:

* Scripting, data manipulation and interpolation, to be used in
  statistical analysis.
* Applications that gather data and present them to the end users.
* Automatic updates to third-parties websites or kiosk-systems like
  e.g., in the hall of hotels.

Command line access to the data is usually carried out with the
:program:`curl` Linux utility, which is used to retrieve information
in a non-interactive way from a remote site and can be used with a
variety of options and can save the contents it downloads, which can
them be send to other applications and manipulated.

Your best opportunity to learn about the correct syntax and parameters
to use is to go to the :strong:`swagger interface` of the `tourism
<https://tourism.opendatahub.com/swagger/ui/index>`_ or `mobility
<https://mobility.api.opendatahub.com/>`_ domains and execute a
query: with the output, also the corresponding :program:`curl` command
used to retrieve the data will be shown.