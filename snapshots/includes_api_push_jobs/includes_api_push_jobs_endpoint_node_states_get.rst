.. The contents of this file may be included in multiple topics (using the includes directive).
.. The contents of this file should be modified in a way that preserves its ability to appear in multiple topics.

The ``GET`` method is used to get a list of nodes and their status (``up`` or ``down``).

This method has no parameters.

**Request**

.. code-block:: xml

   GET /organizations/ORG_NAME/pushy/node_states

**Response**

The response is similar to:

.. code-block:: javascript

   {
     {
       "node_name": "FARQUAD", 
       "status": "up", 
       "updated_at": "Tue, 04 Sep 2012 23:17:56 GMT"
     }
     {
       "node_name": "DONKEY", 
       "status": "up", 
       "updated_at": "Tue, 04 Sep 2012 23:17:56 GMT"
     }
     {
       "node_name": "FIONA", 
       "status": "down", 
       "updated_at": "Tue, 04 Sep 2012 23:17:56 GMT"
     }
   }

The following values are possible: ``up`` or ``down``.

.. list-table::
   :widths: 200 300
   :header-rows: 1

   * - Response Code
     - Description
   * - ``200``
     - OK. The request was successful.
   * - ``400``
     - Bad request. The contents of the request are not formatted correctly.
   * - ``401``
     - Unauthorized. The user or client who made the request could not be authenticated. Verify the user/client name, and that the correct key was used to sign the request.
   * - ``403``
     - Forbidden. The user who made the request is not authorized to perform the action.
   * - ``404``
     - Not found. The requested object does not exist.
