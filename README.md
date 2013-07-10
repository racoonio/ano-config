# bower-config [![Build Status](https://secure.travis-ci.org/bower/config.png?branch=master)](http://travis-ci.org/bower/config)

The Bower config reader and writer.


## Usage

#### .load()

Loads the bower configuration from the configuration files.


#### .get(key)

Returns a configuration value by `key`.   
Keys with dots are supported to access deep values.


#### .set(key, value)

Sets a configuration value for `key`.   
Keys with dots are supported to set deep values.


#### .del(key)

Removes configuration named `key`.   
Keys with dots are supported to delete deep keys.


#### .save(where, callback)

Saves changes to `where`.   
The `where` argument can be a path to a configuration file or:

- `local` to save it in the configured current working directory (defaulting to `process.cwd`)
- `user` to save it in the configuration file located in the home directory


#### .toObject()

Returns a deep copy of the underlying configuration object.


#### #create(cwd)

Obtains a instance where `cwd` is the current working directory (defaults to `process.cwd`);

```js
var config = require('bower-config').create();
// You can also specify a working directory
var config2 = require('bower-config').create('./some/path');
```


#### #read(cwd)

Alias for:

```js
var configObject = (new Config(cwd)).load().toJson();
```


## License

Released under the [MIT License](http://www.opensource.org/licenses/mit-license.php).