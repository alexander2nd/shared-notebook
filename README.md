# shared-notebook
#%% Connect to Server
#     from opcua import Client
# >>> client = Client("opc.tcp://127.0.0.1:12345")
# >>> client.connect()
# >>> client.get_namespace_array()
# >>> client.get_namespace_array()
# ['http://opcfoundation.org/UA/', 'urn:freeopcua:python:server', 'Room1']
# >>> objects=client.get_objects_node()
# >>> print(objects)
# i=85
# >>> objects.get_children()
# [Node(NumericNodeId(i=2253)), Node(StringNodeId(ns=2;s="TS1")), Node(NumericNodeId(ns=2;i=1))]
# >>> bulb = objects.get_children()[2]
# >>> tempsensor=objects.get_children()[1]
# >>> bulb.get_children()
# [Node(NumericNodeId(ns=2;i=2))]
# >>> bulb.get_children()[0].get_browse_name()
# QualifiedName(2:Lightbulb State)
# >>> state = bulb.get_children()[0]
# >>> state.get_value()
# False
# >>> state.set_value(True)
# >>> tempsensor.get_children()
# [Node(StringNodeId(ns=2;s="TS1_VendorName")), Node(StringNodeId(ns=2;s="TS1_SerialNumber")), Node(StringNodeId(ns=2;s="TS1_Temperature"))]
# >>> for i in tempsensor.get_children():
# ...  i.get_value()
# ...
# 'A Temperature Sensor'
# '481632'
# 15.324596924251166
# >>> state.set_value(False)
