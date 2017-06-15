## [Go back home](https://github.com/vishal-biyani/saltstack-cluster)

# Grains

Grains are pieces of information about the Nodes in your cluster that Salt discovers when it installs Minion on the node. The grain attribute comprise of information about the OS, Kernel and other system information attributes.

In addition to the built in Grains, you can also add custom grains to a node which can be used for classification. For example some teams add a "roles" grain to the system and then assign roles such as "webserver", "dbserver" and so on.

A grain can be a value or a list of values based on nature of the grain attribute.

## 

