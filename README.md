# l2_learning_rest
Module for POX Controller that offers table mac-interface of switches connected to a POX controller.

It is recommended run this script in Mininet VM.

In Mininet VM, configure the interface in bridge mode and open two ssh connections.
Copy this code to folder ~/pox/pox/forwarding
Run a topology: sudo mn --topo tree,2 --controller remote
In other connection, run the module:

cd pox
./pox.py forwarding.l2_learning_rest

In first connection make a ping between h1 and h2:

h1 ping h2

Acess by the browser the REST interface:

http://IP_VM:8000/switches

and you will the dpids of each one them.

If acess http://IP_VM:8000/switches/2 after ping,

You will see the table mac-interface of switch 2.
