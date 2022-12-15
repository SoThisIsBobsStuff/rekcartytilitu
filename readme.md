# utility tracker
a simple set of scripts and utilities to enable a variety of web based items to be tracked and the data consolidated

# deployment
the eventual aim is to add to PyPi for fast deployment, but currently download the repo and enter:

# flow
 [main] -> [load config]
   [connect to storage]
   [load modules]
   [init queues]
   
   -> [load actions]
   [process actions -> create actions]
   -> [... rinse and repeat]

# running
python main.py --config [path to config.json]

# languages and technologies
- python 3.8+
- neo4j

# requirements
- python -m pip install -r requirements.txt

# config file:
- paths
  - settings
      - type - [file | envvar | database | api | uri]
      - uri - the location of the resource
      - reader - the class used to read the node
      - security - settings for security
      - params - extra parameters needed to help the reader
  - storage
      - see above
  - [labeled data]
      - heirarchy key values ussed for a varieyt of information
