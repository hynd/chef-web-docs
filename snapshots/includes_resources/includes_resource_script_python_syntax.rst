.. The contents of this file may be included in multiple topics (using the includes directive).
.. The contents of this file should be modified in a way that preserves its ability to appear in multiple topics.

A **python** resource block executes scripts using Python:

.. code-block:: ruby

   python 'hello world' do
     code <<-EOH
       print "Hello world! From Chef and Python."
       EOH
   end

where 

* ``code`` specifies the command to run

The full syntax for all of the properties that are available to the **python** resource is:

.. code-block:: ruby

   python 'name' do
     code                       String
     creates                    String
     cwd                        String
     environment                Hash
     flags                      String
     group                      String, Integer
     notifies                   # see description
     path                       Array
     provider                   Chef::Provider::Script::Python
     returns                    Integer, Array
     subscribes                 # see description
     timeout                    Integer, Float
     user                       String, Integer
     umask                      String, Integer
     action                     Symbol # defaults to :run if not specified
   end

where 

* ``python`` is the resource
* ``name`` is the name of the resource block
* ``:action`` identifies the steps the chef-client will take to bring the node into the desired state
* ``code``, ``creates``, ``cwd``, ``environment``, ``flags``, ``group``, ``path``, ``provider``, ``returns``, ``timeout``, ``user``, and ``umask`` are properties of this resource, with the Ruby type shown. See "Properties" section below for more information about all of the properties that may be used with this resource.
