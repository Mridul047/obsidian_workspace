
## Topic , Partition & Offsets

## Producers & Message Key
* Producers can send message with a message key. This message key is used to identify partition to which the message will be sent. 
* Kafka Message structure:

	![[Pasted image 20231115134149.png]]

* Kafka stores messages once serialization is done on the key & value.

	![[Pasted image 20231115134839.png]]
	![[Pasted image 20231115135223.png]]

## Consumers & Deserialization
* Consumers :
	
	![[Pasted image 20231115162058.png]]

* Consumers Deserialization :
 
	![[Pasted image 20231115162313.png]]

## Consumer Groups & Consumer Offsets
*  Consumer Groups :
	
	![[Pasted image 20231115180404.png]]![[Pasted image 20231115180404.png]]![[Pasted image 20231115180448.png]]![[Pasted image 20231116144256.png]]

*  Consumer offsets :
	
	![[Pasted image 20231116144917.png]]
	![[Pasted image 20231116145056.png]]

## Kafka Broker & Topic
* Broker :
	![[Pasted image 20231118123900.png]]
	![[Pasted image 20231118124020.png]]
	![[Pasted image 20231118124156.png]]
* Topic Replication :
	![[Pasted image 20231118124355.png]] ![[Pasted image 20231118124555.png]]
	![[Pasted image 20231118124805.png]]
	![[Pasted image 20231118124943.png]]

## Producer Acks & Topic Durability
* Acks :
	![[Pasted image 20231118125911.png]]
	![[Pasted image 20231127231759.png]]
	![[Pasted image 20231127231854.png]]
	![[Pasted image 20231127232038.png]]
	![[Pasted image 20231127232212.png]]
* Durability :
	![[Pasted image 20231118130016.png]]


## Zookeeper
* Basics of zookeeper :
	![[Pasted image 20231118130402.png]]
	![[Pasted image 20231118130641.png]]
	![[Pasted image 20231118130807.png]]
	![[Pasted image 20231118131841.png]]
	![[Pasted image 20231118131905.png]]


