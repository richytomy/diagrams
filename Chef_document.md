# Chef configuration management

![Chef configuration management](https://github.com/richytomy/diagrams/blob/master/chef_configuration_management.jpg)



## Chef server
Your Chef server acts as a central repository for your cookbooks as well as for information about every node it manages. For example, the Chef server knows a node's fully qualified domain name (FQDN) and its platform.

Central server which is bootstrapped to the nodes  
Repository for Cookbooks and recipes  
running a chef server on unbuntu on AWS  
[Go to learn chef rally](https://learn.chef.io/modules/learn-the-basics/ubuntu/aws#/)

## Chef recipes
Recipes in chef are essentially ruby scripts. It is mostly a collection of resources.
[Find more about chef recipes](https://docs.chef.io/recipes.html)

## Cookbooks
Cook books as the name implies is a collection of chef recipes with a bunch of other supporting files.

To generate a template cookbook use the below command
_chef generate cookbook cookbooks/learn_chef_apache2_


## Chef node

A node is any computer that is managed by a Chef server. Every node has the Chef client installed on it. The Chef client talks to the Chef server. A node can be any physical or virtual machine in your network.

## Chef workstation
Your workstation is the computer from which you author your cookbooks and administer your network. It's typically the machine you use everyday. 

[Install chef workstation](https://downloads.chef.io/chef-workstation/)

## Knife
The knife command enables you to communicate with the Chef server from your workstation.

knife cookbook upload learn_chef_apache2

knife cookbook list


## local mode
apply a chef recipe on the local system
* sudo chef-client --local-mode webserver.rb


## Architecture

![Basic chef server node setup](https://github.com/richytomy/diagrams/blob/master/Screen%20Shot%202019-05-07%20at%208.51.48%20AM.png)
