### Restore single collection to MongoDB

`mongorestore --db={{DB_NAME}} --collection={{COLLECTINO_NAME}} {{COLLECTION_BSON_FILE}}`

- <b>DB_NAME: </b> DB to get backup from
- <b>COLLECTION_NAME: </b>Collection which needs to be dumped in destination directory
- <b>COLLECTION_BSON_FILE: </b>Location of the collections `bson` file which was generated by [mongodump](mongo-dump-collection.md) command

#### Example:

`mongorestore --db=ak-cli --collection=cli_commands /arshad/ak-cli/db/dump/cli_commands.bson`

To drop the collection before importing, add `--drop` flag at the end of the command. Something like the below command.

`mongorestore --db=ak-cli --collection=cli_commands /arshad/ak-cli/db/dump/cli_commands.bson --drop`

- <b>--drop</b>: Drop flag, drops the collection before proceeding with import.

#### Related Commands

- [Dump collection from mongoDB](mongo-dump-collection.md)
