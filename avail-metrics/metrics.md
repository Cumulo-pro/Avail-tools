# Avail metrics

## Table of contents

### Overview

1. [Block Height](#block-height)

### Node metrics

2. [Average Block Proposal Time](#average-block-proposal-time)
3. [Average Block Construction Time](#average-block-construction-time)
4. [Peers Connected](#peers-connected)
5. [Peers Discovered](#peers-discovered)
6. [Major Syncing](#major-syncing)
7. [Num Transactions](#num-transactions)
8. [Number of Transactions in the Queue](#number-of-transactions-in-the-queue)
9. [Num Blocks Import Queue](#num-blocks-import-queue)
10. [Queued Blocks](#queued-blocks)
11. [Number of Known Forks](#number-of-known-forks)
12. [State Cache](#state-cache)
13. [Total Bandwidth Usage](#total-bandwidth-usage)
14. [Evaluation Grid Build Time](#evaluation-grid-build-time)
15. [Average Execution Time](#average-execution-time)
16. [Average Time to Build Commitment](#average-time-to-build-commitment)
17. [Task Polling Duration](#task-polling-duration)
18. [Polling Rate Imbalance](#polling-rate-imbalance)
19. [GRANDPA's Gossip](#grandpas-gossip)
20. [Grandpa Precommits Total](#grandpa-precommits-total)
21. [Grandpa Prevotes Total](#grandpa-prevotes-total)
22. [Grandpa Finality Round](#grandpa-finality-round)
23. [Total Gossip Expired](#total-gossip-expired)


![linea transpa](https://github.com/user-attachments/assets/eda24507-f888-406b-ad16-511bd2e23d4c)


## Overview

### Block Height
__substrate_block_height__  

- best: This is the most recent block that the node considers to be the best known block.
- finalised: This is the last block that has been finalised and confirmed as a permanent part of the chain.
- sync_target (sync target): This is the block height target that the node is trying to reach during synchronisation.
  
![image](https://github.com/Cumulo-pro/Avail-tools/assets/2853158/65b3e3b6-7f55-4d5a-8001-38485faeb1ae)

### Build Info   
__substrate_build_info__   

This metric provides static information about the build and network configuration of a Substrate-based node. This metric is useful for identifying the node's software version and network configuration, assisting in debugging and monitoring.  

•	Moniker: Indicates the name of the node or project running.  
•	Node Version: Represents the specific version of the node software in use.  
•	Chain Id: Specifies the blockchain network the node is connected t.o  

![image](https://github.com/user-attachments/assets/7fb1bff4-c773-4259-8b37-f5bf96222c1e)


## Node metrics

### Average Block Proposal Time
__substrate_proposer_block_proposal_time_sum/substrate_proposer_block_proposal_time_count__  

This metric measures the time it takes to build a block and prepare it for the proposal.  

![image](https://github.com/Cumulo-pro/Avail-tools/assets/2853158/4f125ae2-de9c-474a-b3aa-1ad88b1bdd5b)

### Average Block Construction Time
__substrate_proposer_block_constructed_sum/substrate_proposer_block_constructed_count__  

Time it takes to build blocks in the network. This metric is useful for monitoring the efficiency of the block building process.  

![image](https://github.com/Cumulo-pro/Avail-tools/assets/2853158/180fd64e-7c95-43b5-9cd6-a1a5e967323a)

### Major Syncing  
__substrate_sub_libp2p_is_major_syncing__

This metric indicates whether the node is performing a major synchronisation or not.   
In a blockchain environment, a major synchronisation can refer to an intensive process where the node catches up with the entire blockchain, downloading and verifying all blocks from the genesis or from a significant fork.  

![image](https://github.com/Cumulo-pro/Avail-tools/assets/2853158/66426365-843d-46ac-ae58-40fec4d9bff9)

### Num transactions
__substrate_proposer_number_of_transactions__

This metric indicates the number of transactions included in the most recent block in the network.    

![image](https://github.com/Cumulo-pro/Avail-tools/assets/2853158/c64e4980-5dea-4124-9a91-dde91169ee62)


### Number of Transactions in the Queue
__substrate_ready_transactions_number__

This metric indicates the number of transactions that are in the queue of transactions ready to be included in a block.  

![image](https://github.com/Cumulo-pro/Avail-tools/assets/2853158/7c76a4eb-744c-458c-8c5c-f14fc6245c13)

### Num blocks import queue
__substrate_sync_queued_blocks__

Number of blocks that are in the import queue on the chain.  
By observing this metric, node operators can determine if there is a delay in block import and take corrective action if the number of blocks in the queue increases unexpectedly. This metric provides a quick and efficient overview of the block flow within the node, ensuring that the synchronisation process remains smooth and uninterrupted.  

![image](https://github.com/Cumulo-pro/Avail-tools/assets/2853158/47881e72-6d28-42ab-bf90-8b679c1c1144)

### Queued Blocks
__substrate_sync_queued_blocks__

The current number of blocks that are in the import queue to be processed by the network. In the context of a blockchain, block import refers to the process of receiving, validating and adding new blocks to the main chain.
This metric provides crucial information about the congestion or block import workflow on the Avail Turing Network blockchain network, allowing operators and developers to monitor the efficiency and operational status of the network.  

![image](https://github.com/Cumulo-pro/Avail-tools/assets/2853158/578d3ec1-7f7a-46ee-9446-9a313b0f0e6f)

### Number of Known Forks
__substrate_number_leaves__

Measures the number of forks in the chain. An increase in the number of forks may indicate consensus problems or possible attacks on the network. Maintaining a low and stable number of forks is generally a sign of a healthy network.  

![image](https://github.com/Cumulo-pro/Avail-tools/assets/2853158/dc0e1678-c6d7-4dd8-9fe6-518b37dbed97)

## State System

### State Cache
__substrate_state_cache_bytes__ 

Indicates the size of the state cache in bytes.  
This metric is useful for monitoring memory resource usage on network nodes. An excessively large cache size may indicate the need to adjust the cache configuration.  

![image](https://github.com/Cumulo-pro/Avail-tools/assets/2853158/a4ea6776-d17b-4c60-b7b4-43d6dfa7fcb6)





![linea transpa](https://github.com/user-attachments/assets/eda24507-f888-406b-ad16-511bd2e23d4c)

## Node Connectivity

### peers Connected
__substrate_sub_libp2p_peers_count__ 

This metric indicates the number of peers connected to the network.

![image](https://github.com/Cumulo-pro/Avail-tools/assets/2853158/7a9c1469-237b-48b0-bbd5-098b08966eec)

### peers Discovered
__substrate_sub_libp2p_peerset_num_discovered__  

Indicates the current number of nodes (or peers) that have been discovered and are stored in the peerset manager.  

![image](https://github.com/Cumulo-pro/Avail-tools/assets/2853158/c012ddc5-580d-4381-8386-530ed1f8b08c)


### Total Bandwidth Usage 
__substrate_sub_libp2p_network_bytes_total__  

This metric indicates the total bandwidth usage of the libp2p network in bytes. This information is crucial for monitoring, optimising and ensuring network performance.  

![image](https://github.com/Cumulo-pro/Avail-tools/assets/2853158/7a2fb4ef-251a-4541-9e4f-74f56c2d5a16)

### Evaluation Grid Build Time
__avail_header_extension_builder_evaluation_grid_build_time_sum/avail_header_extension_builder_evaluation_grid_build_time_count__  

This metric measures the average time required to build the header extension evaluation grid on an avail_turing_network node.  Building the evaluation grid" refers to the creation of a data structure that organises and evaluates the information in the data block or transactions. This structure can be used for various purposes, including network validation, verification and optimisation.  

![image](https://github.com/Cumulo-pro/Avail-tools/assets/2853158/6ba95d3c-2951-4575-9d75-98872174fe39)

### Average execution time
__avail_header_extension_builder_total_execution_time_sum/avail_header_extension_builder_total_execution_time_count__  

This metric measures the total execution time for the construction of the header extension, the time is reported in microseconds. This metric provides a clear view of the performance of the node in terms of total execution time for the header extension construction.  

![image](https://github.com/Cumulo-pro/Avail-tools/assets/2853158/dbfaa3af-0436-4128-ab0f-34dc3bca65e5)

### Average time to build commitment
__avail_header_extension_builder_commitment_build_time_sum/avail_header_extension_builder_commitment_build_time_count__  

Average time to build the header extension commitment on a node in the avail_turing_network network.
This metric provides a clear view of node performance in terms of building header extension commitment, helping to maintain efficiency and proactively detect potential problems.  

![image](https://github.com/Cumulo-pro/Avail-tools/assets/2853158/3c04efb3-6652-4c2d-8da5-3eda74a9a920)

## Avail Node Stats

### Task Polling Duration 
__substrate_tasks_polling_duration__  

Counts the total number of times the invocation of Future::poll has been started for each specific task. This helps to understand how often tasks are executed compared to the duration of their invocations.  

![image](https://github.com/Cumulo-pro/Avail-tools/assets/2853158/854d9688-6089-4f9b-be28-ea51302256cc)

### Polling Rate Imbalance
__rate(substrate_tasks_polling_started_total[1m]) - rate(substrate_tasks_polling_duration_count[1m])__  

This composite metric is useful for monitoring system performance and efficiency, helping to identify processing problems and optimise the execution of tasks on the network.
Calculates the difference between the start rate and the completion rate of Future::poll invocations.
-A positive value indicates that more poll invocations are being started than are being completed in the last minute.
-A negative value indicates that more poll invocations are being completed than are being started in the last minute.
-A value close to zero suggests that the number of initiated and completed invocations is balanced.  

![image](https://github.com/Cumulo-pro/Avail-tools/assets/2853158/5314f0ad-ba78-4f3b-9a7f-944cc4487236)

### GRANDPA's gossip
__substrate_finality_grandpa_communication_gossip_validator_messages__  

Information on the number of messages validated by the gossip validator of the GRANDPA (GHOST-based Recursive ANcestor Deriving Prefix Agreement) completion mechanism.  
ES Información sobre el número de mensajes validados por el validador de gossip del mecanismo de finalización GRANDPA (GHOST-based Recursive ANcestor Deriving Prefix Agreement)  

![image](https://github.com/Cumulo-pro/Avail-tools/assets/2853158/0ce80a9d-e021-457d-8e69-68c5b50554cb)

### Grandpa Precommits Total
__substrate_finality_grandpa_precommits_total__  

The metric provides information on the total number of precommits made locally by the GRANDPA (GHOST-based Recursive ANcestor Deriving Prefix Agreement) completion mechanism in the chain.  

![image](https://github.com/Cumulo-pro/Avail-tools/assets/2853158/0f1e478d-e9c7-4879-ae42-61d10d542dae)

### Grandpa Prevotes Total
__substrate_finality_grandpa_prevotes_total__

Information on the total number of prevotes made locally by the GRANDPA (GHOST-based Recursive ANcestor Deriving Prefix Agreement) completion mechanism in the chain.
This metric is useful to monitor the activity and performance of the GRANDPA consensus process in the avail_turing_network chain, providing an indication of the total number of prevotes that have been issued by the validators.  

![image](https://github.com/Cumulo-pro/Avail-tools/assets/2853158/a76df61a-2936-4785-9905-2710fde29af7)

### Grandpa Finality Round
__substrate_finality_grandpa_round__  

Indicates the highest number of completed rounds using the GRANDPA (GHOST-based Recursive ANcestor Deriving Prefix Agreement) completion protocol.
This value can be used to monitor the progress of the network in terms of block completion. An increasing value indicates that the network is progressing and completing more rounds.  

![image](https://github.com/Cumulo-pro/Avail-tools/assets/2853158/7478efaf-5cc0-44dc-a774-d36625abc62b)

### Total Gossip Expired
__substrate_network_gossip_expired_messages_total__  

Total number of messages that have expired and have not been processed by the gossip service.
A high number of expired messages may indicate network overload or problems in message processing, where messages are not handled before they expire.  

![image](https://github.com/Cumulo-pro/Avail-tools/assets/2853158/2a6c7f06-56f3-4c11-bc21-fd57a18b3c7c)

## Authority Discovery

### Failures Handling 'Value Found' Events in DHT  

__substrate_authority_discovery_handle_value_found_event_failure__  

This metric shows the number of times the authority discovery system failed to handle a value_found event in the Distributed Hash Table (DHT). A failure in handling these events means that, although a requested value was found in the DHT, an error occurred during its processing.
Value: 0 – Indicates that no failures have been recorded when handling value_found events so far.

![image](https://github.com/user-attachments/assets/92f76838-56cc-4da2-b755-a9b9204f3a66)

### Known Authorities Count

__substrate_authority_discovery_known_authorities_count__

This metric shows the current number of authority nodes known to the authority discovery system in the network. Known authorities are nodes that have been identified and stored by the system, allowing for reliable connections and communication across the network.  

![image](https://github.com/user-attachments/assets/1e2f6bc1-5276-47fc-b3a1-a4ece127f457)

### Total Times External Addresses Published  

__substrate_authority_discovery_times_published_total__  

This metric shows the total number of times the authority discovery system has published external addresses for the nodes in the network. Each publication event makes the node's external addresses available to other network participants, enhancing connectivity.
If this count is unusually low or stagnant, it might indicate issues with address publication, potentially affecting other nodes' ability to connect.  

![image](https://github.com/user-attachments/assets/0d72abfd-54db-41ea-ba36-53fdbd21ecf9)

### Pending Authority Address Requests  

__substrate_authority_discovery_authority_address_requests_pending__  

This metric shows the number of pending requests for authority addresses in the network. Pending requests represent attempts by nodes to obtain addresses of other authorized nodes (or “authorities”) in the network that have not yet been resolved.
0 – This indicates that there are currently no pending requests for authority addresses in the network.  

![image](https://github.com/user-attachments/assets/f751a087-7be0-4ee3-89e3-5334768d9385)

### DHT Events Received by Authority Discovery  

__substrate_authority_discovery_dht_event_received__  

This metric tracks the number of Distributed Hash Table (DHT) events received by the authority discovery system. Each event type represents different outcomes in DHT operations, such as successfully finding or storing values, which are essential for maintaining network connectivity.  

Values
•	value_found: The number of times a requested value was found in the DHT.  
•	value_not_found: The number of times a requested value was not found in the DHT.  
•	value_put: The number of times a value was successfully stored in the DHT.  
•	value_put_failed: The number of times an attempt to store a value in the DHT failed.  

![image](https://github.com/user-attachments/assets/28a6b88a-88ce-43e0-999d-b62be0e2f69a)

### External Addresses Last Published  

__substrate_authority_discovery_amount_external_addresses_last_published__  

This metric provides the count of external addresses that were published the last time authority discovery updated addresses in the network. It shows the current number of addresses made available by the authority discovery mechanism, which helps other network participants connect and maintain communication with the node.  

![image](https://github.com/user-attachments/assets/50416642-f579-44b4-ac1c-e04ff88decb0)

### Total Authority Addresses Requested  

__substrate_authority_discovery_authority_addresses_requested_total__

This metric shows the total number of times the authority discovery system has requested external addresses of a single authority node within the network. Each request represents an instance where the network attempted to retrieve the address information of a specific authority, which is essential for maintaining node connectivity.
An unexpectedly high or rapidly increasing count could indicate frequent address loss or issues with address retention, prompting more requests than usual. Monitoring this can help identify if connectivity problems are emerging.  

![image](https://github.com/user-attachments/assets/fe65a020-569b-45a9-a6f6-01558b161834)





