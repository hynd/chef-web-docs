.. The contents of this file may be included in multiple topics (using the includes directive).
.. The contents of this file should be modified in a way that preserves its ability to appear in multiple topics.


This argument has the following options:

``-c``, ``--create-key``
   Generate a new public/private key pair and replace an existing public key with the newly-generated public key. To replace the public key with an existing public key, use ``--public-key`` instead.

``-e DATE``, ``--expiration-date DATE``
   The expiration date for the public key, specified as an ISO 8601 formatted string: ``YYYY-MM-DDTHH:MM:SSZ``. If this option is not specified, the public key will not have an expiration date. For example: ``2013-12-24T21:00:00Z``.

``-f FILE``, ``--file FILE``
   Save a private key to the specified file name. If the ``--public-key`` option is not specified the Chef server will generate a private key.

``-k NAME``, ``--key-name NAME``
   The name of the public key. 

``-p FILE_NAME``, ``--public-key FILE_NAME``
   The path to a file that contains the public key. If this option is not specified, and only if ``--key-name`` is specified, the Chef server will generate a public/private key pair.
