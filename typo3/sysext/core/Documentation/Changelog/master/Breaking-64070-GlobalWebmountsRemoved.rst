====================================================
Breaking: #64070 - Removed global variable WEBMOUNTS
====================================================

Description
===========

The global variable WEBMOUNTS was removed, as the same data from the WEBMOUNTS can always be fetched via
``$GLOBALS['BE_USER']->returnWebmounts()``.

Impact
======

The variable ``$GLOBALS['WEBMOUNTS']`` will no longer be filled.


Affected installations
======================

Any installation using ``$GLOBALS['WEBMOUNTS']`` directly within an extension will produce a wrong result.

Migration
=========

Replace all occurrences of ``$GLOBALS['WEBMOUNTS']`` with ``$GLOBALS['BE_USER']->returnWebmounts()``.
