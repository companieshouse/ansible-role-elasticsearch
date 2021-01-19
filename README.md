# ansible-role-elasticsearch

This role is specifically intended for creating Redhat based AMIs, providing a minimal install prior to configuration

## Role Variables

| Variable                             |           Default          | Description                                                       |
| ------------------------------------ | :------------------------: | ----------------------------------------------------------------- |
| elasticsearch_data_directory         |  `/var/lib/elasticsearch`  | The directory in which elasticsearch stores it's data             |
| elasticsearch_home_directory         | `/usr/share/elasticsearch` | The home directory of elasticsearch                               |
| elasticsearch_service_group          |       `elasticsearch`      | The group under which elasticsearch will run                      |
| elasticsearch_service_user           |       `elasticsearch`      | The user under which elasticsearch will run                       |
| elasticsearch_version                |          `7.10.1`          | The version of elasticsearch to install                           |
| plugins                              |              -             | The list of plugins to install                                    |
| resource_bucket_elasticsearch_prefix |              -             | The path under which the rpm package is located within the bucket |
| resource_bucket_name                 |              -             | The bucket from which to source the rpm package                   |

## Dependencies

| Role                                                                            | Version |
| ------------------------------------------------------------------------------- | ------- |
| [ansible-role-pip](https://github.com/geerlingguy/ansible-role-pip)             | `2.0.0` |
| [ansible-role-repo-epel](https://github.com/geerlingguy/ansible-role-repo-epel) | `3.0.0` |

### Example Requirements File

How you use the role within a given project

```yml
- src: https://github.com/companieshouse/ansible-role-elasticsearch
  name: elasticsearch
  version: 1.0.0
```

## License

MIT
