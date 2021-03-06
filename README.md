topbeat Cookbook
================

[![Build Status](https://travis-ci.org/vkhatri/chef-topbeat.svg?branch=master)](https://travis-ci.org/vkhatri/chef-topbeat)

This is a [Chef] cookbook to manage [Topbeat].


## Repository

https://github.com/vkhatri/chef-topbeat


## Supported OS

This cookbook was tested on Amazon and expected to work on other RHEL platforms. Cookbook is expected to work on Ubuntu, but have not tested yet.


## Recipes

- `topbeat::default` - default recipe (use it for run_list)

- `topbeat::install` - install topbeat

- `topbeat::config` - configure topbeat


## Core Attributes


* `default['topbeat']['version']` (default: `1.0.0-beta3`): topbeat version

* `default['topbeat']['package_url']` (default: `calculated`): package download url

* `default['topbeat']['packages']` (default: `[]`): package dependencies

* `default['topbeat']['conf_dir']` (default: `/etc/topbeat`): topbeat yaml configuration file directory

* `default['topbeat']['conf_file']` (default: `/etc/topbeat/topbeat.yml`): topbeat configuration file

* `default['topbeat']['notify_restart']` (default: `true`): whether to restart topbeat service on configuration file change

* `default['topbeat']['disable_service']` (default: `false`): whether to stop and disable topbeat service, useful for maintenance mode


## Configuration File topbeat.yml Attributes

* `default['topbeat']['config']['input']['period']` (default: `10`): topbeat statistics collection interval

* `default['topbeat']['config']['input']['period']` (default: `10`): topbeat procs to collect statistics

* `default['topbeat']['config']['output']['elasticsearch']['enabled']` (default: `true`):

* `default['topbeat']['config']['output']['elasticsearch']['hosts']` (default: `[]`):: `false`):

* `default['topbeat']['config']['output']['redis']['enabled']` (default: `false`):

* `default['topbeat']['config']['output']['redis']['host']` (default: `127.0.0.1`):

* `default['topbeat']['config']['output']['redis']['port']` (default: `6379`):

* `default['topbeat']['config']['output']['file']['enabled']` (default: `false`):

* `default['topbeat']['config']['output']['file']['path']` (default: `/tmp/topbeat`):

* `default['topbeat']['config']['output']['file']['filename']` (default: `topbeat`):

* `default['topbeat']['config']['output']['file']['rotate_every_kb']` (default: `1000`):

* `default['topbeat']['config']['output']['file']['number_of_files']` (default: `7`):


For more attribute info, visit below link:

https://github.com/elastic/topbeat/blob/master/etc/topbeat.yml


## Contributing

1. Fork the repository on Github
2. Create a named feature branch (like `add_component_x`)
3. Write your change
4. Write tests for your change (if applicable)
5. Run the tests (`rake & rake knife`), ensuring they all pass
6. Write new resource/attribute description to `README.md`
7. Write description about changes to PR
8. Submit a Pull Request using Github


## Copyright & License

Authors:: Virender Khatri and [Contributors]

<pre>
Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
</pre>


[Chef]: https://www.chef.io/
[Topbeat]: https://www.elastic.co/downloads/beats/topbeat
[Contributors]: https://github.com/vkhatri/chef-topbeat/graphs/contributors
