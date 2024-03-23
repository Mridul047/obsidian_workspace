
## Kafka Producer : Java API with callbacks
*  If the Producer send the events rapidly to the topic ( with default batch size 16KB) then Kafka   will try to store all the events in same partition. This behavior is done for performance improvement & is called sticky partitioner.
  
	![[Pasted image 20231121230250.png]]

## Kafka Producer : Java API with keys


## Kafka Consumer : Java API - CG Rebalance
* Default behavior: before v3
	![[Pasted image 20231127155728.png]]
	![[Pasted image 20231127155950.png]]
	![[Pasted image 20231127160243.png]]
	![[Pasted image 20231127160431.png]]

## Kafka Consumer : Java API - Offset

![[Pasted image 20231127161645.png]]

![[Pasted image 20231127161802.png]]



## Kafka Producer : Availability

![[Pasted image 20231127232549.png]]

## Kafka Producer :  Retries & Timeouts

![[Pasted image 20231127232741.png]]

![[Pasted image 20231127233056.png]]

![[Pasted image 20231127233742.png]]



## Kafka Producer : Idempotency

![[Pasted image 20231127234044.png]]

![[Pasted image 20231127234151.png]]

![[Pasted image 20231127234300.png]]

![[Pasted image 20231127234355.png]]


## Kafka Message Compression
* Message Compression :
	![[Pasted image 20231127235012.png]]
	![[Pasted image 20231127235926.png]]
	![[Pasted image 20231128000034.png]]
	![[Pasted image 20231128000208.png]]
	![[Pasted image 20231128000436.png]]
	![[Pasted image 20231128000504.png]]
	![[Pasted image 20231128000601.png]]
	![[Pasted image 20231128000626.png]]
	![[Pasted image 20231201152221.png]]

## Kafka Producer : Default Partitioner & Sticky Partitioner  
![[Pasted image 20231201152808.png]]
![[Pasted image 20231201152851.png]]
![[Pasted image 20231201152951.png]]
![[Pasted image 20231201153044.png]]
![[Pasted image 20231201153106.png]]


## Kafka Consumer : Delivery Semantics
* Delivery Semantics
	![[Pasted image 20231202131017.png]]
	![[Pasted image 20231202131153.png]]
	![[Pasted image 20231202131242.png]]

### Kafka Consumer : Commit Strategy
* Commit strategies:
	Option 1:
	![[Pasted image 20231202132307.png]]
	![[Pasted image 20231202132350.png]]
	![[Pasted image 20231202132442.png]]
	Option 2:
	![[Pasted image 20231202132625.png]]
	Option 3:
	![[Pasted image 20231202132828.png]]

## Kafka Consumer : Offset Reset Behavior
* ![[Pasted image 20231202155424.png]]
* ![[Pasted image 20231202155525.png]]
* ![[Pasted image 20231202155603.png]]


## Kafka Consumer : Internal Threads
* ![[Pasted image 20231202160142.png]]
* ![[Pasted image 20231202160243.png]]
* ![[Pasted image 20231202160407.png]]
* ![[Pasted image 20231202160448.png]]
* ![[Pasted image 20231202160540.png]]

## Kafka Consumer : Replica fetching
 *  ![[Pasted image 20231202203203.png]]
 * ![[Pasted image 20231202203325.png]]
 * ![[Pasted image 20231202203415.png]]
 * 