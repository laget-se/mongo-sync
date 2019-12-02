[mongo-sync]
=================================================================================

> _Sync Remote and Local MongoDB Databases in Bash.!_


## Usage

- Download / Clone the script

    ```bash
    git clone https://github.com/laget-se/mongo-sync.git
    cd mongo-sync
    ```

- Edit `config.yml` and insert your configuration details

- Use the script like this:
	```bash
	./mongo-sync push [options]    # Push DB to Destination
	./mongo-sync pull [options]    # Pull DB from Source
	./mongo-sync sync [options]    # Pull & Push
	```
- Options
	```
	-y (--yes)                     # Skip confirmation
	-c (--config) file.yml         # Use alternative config file
	```

## Notes

 - `mongo-sync` requires `mongodump` and `mongorestore` binaries to be installed in your system. If you have [`mongodb`](http://docs.mongodb.org/manual/tutorial/#getting-started) installed, then you probably already have them
 - Pushing/Pulling ***overwrites*** the destination DB
 - It's a good idea to keep your alternative/custom `config.yml` in `.gitignore` if you're using it inside some other project


## TODO

 - Add a `backup` command and an `--auto-backup` feature


## Contributing

1. [Fork it](https://github.com/laget-se/mongo-sync/fork)
2. Create your feature/fix branch (`git checkout -b feature/my-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin feature/my-feature`)
5. Create a new Pull Request