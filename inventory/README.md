# Inventory

## Branches

| Name      | Details                                                           |
| --------- | ----------------------------------------------------------------- |
| a-prelive | This branch resembles the `develop` branch in other projects.     |
| z-stable  | This branch resembles the stable `main` branch in other projects. |

_Make sure to regularily update the `a-prelive` branch from `z-stable`_

## Folders

| Name       | Details           |
| ---------- | ----------------- |
| group_vars | Group vars folder |
| host_vars  | Host vars folder  |
| inventory  | Inventory folder  |

## Groups

| Name                         | Details                                                             |
| ---------------------------- | ------------------------------------------------------------------- |
| middleware_worknodes         | Worknodes for Ansible development                                   |
| middleware_gitlab_runner_all | Middleware Gitlab Runner: Collection, Playbook, Inventory Pipelines |
| role_apache                  | all Apache hosts                                                    |
| role_tomcat                  | all Tomcat hosts                                                    |

## Tools

### Dump variables of host

```shell
ansible-playbook --ask-vault-pass -i . .utils/dump.yml --limit 'somename'
```
