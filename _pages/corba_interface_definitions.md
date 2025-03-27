In CORBA IDL stub means client side proxy. It looks like the real object, but it doesn't implement any logic, it just forwards method calls over the network to the real implementation.

My Code -> CORBA Stub -> ACS Container or another host -> Real Python method (servant)