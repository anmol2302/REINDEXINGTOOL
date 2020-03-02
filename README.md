This is the script which will perform reindexing on Elasticsearch Index...

## How to run 
  - give permission to the script chmod +x reindex.sh
  - bash reindex.sh {{es_ip}} {{old_index}} {{new_index}} {{alias_name}} {{index_req_filePath}} {{mappings_req_filePath}}



## CLI ARGS DESCRIPTION
 - es_ip: Ip of ElasticSearch port is asumed to be 9200
 - old_index: Source Index from which reindexing to be done
 - new_index: Destination Index, to which reindexing to be done
 - alias_name: Name of Alias to which index need to be mapped/removed
 - index_req_filepath: .json file path which will have a request body for creating new_index.
 - mapping_req_filepath: .json file path which will have a request body for creating mappings of new_index.  

 
SOURCE : https://engineering.carsguide.com.au/elasticsearch-zero-downtime-reindexing-e3a53000f0ac
