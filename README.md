This is the script which will perform reindexing on Elasticsearch Index...

## How to run 
  - give permission to the script chmod +x reindex.sh
  - bash reindex.sh {{es_ip}} {{old_index}} {{new_index}} {{alias_name}} {{index_req_filePath}} {{mappings_req_filePath}}



## CLI ARGS DESCRIPTION
 - es_ip: Ip of ElasticSearch and port is asumed to be 9200
 - old_index: Source Index from which reindexing to be done
 - new_index: Destination Index, to which reindexing to be done
 - alias_name: Name of Alias to which new_index to be mapped and old index need to be removed.
 - index_req_filepath: .json file path which will have a request body for creating new_index.
 - mapping_req_filepath: .json file path which will have a request body for creating mappings of new_index.  
 
 
 **NOTE**: old_index will be deleted by the script.
 
 
 ## Following Steps will be done by Script:

  1: Validating Input params
      - File paths
      - ElasticSearch health  
  2: mapping alias_name with `old_index`
  4: creating indices and mapping of `new_index`.
  5: Reindexing from `old_index` index to `new_index` index.
  6: deleting alias with  `old_index` and mapping alias with `new_index`.
  7: deleting  `old_index`


 
SOURCE : https://engineering.carsguide.com.au/elasticsearch-zero-downtime-reindexing-e3a53000f0ac
