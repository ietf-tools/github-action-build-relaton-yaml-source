This action uses ``relaton-cli`` to fetch bibliographic data using specified adapter
and commit it to this repository in YAML.

This action places files under `data` directory under repository root.

A repository using this action is supposed to be used
for Relaton bibliographic data storage only.

.. note::

   Always keep ``relaton-cli`` pinned to minor version,
   and only increment minor version after manual review and testing.

   This action is intended to be used
   by *all* ``ietf-tools/relaton-data-*`` repositories,
   which are used by IETF BibXML service as bibliographic data sources.

   Thus, generated YAML **must** be readable
   by the version of ``relaton-py`` that production IETF BibXML service uses.

   Since Relaton bibdata sourcing gems (including the ``relaton-cli`` umbrella)
   follow a pattern of incrementing a minor version on breaking schema changes
   (patch version updates are safe), it’s important to keep
   ``relaton-cli`` pinned to minor version.
