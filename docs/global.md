
### global

These settings define behaviour of the deployment or the default behavior of all cronjobs.

```yaml
# default settings

annotations:
priority: ('low', 'mid', 'high', 'core', 'database', 'critical')
restart: Always ('Always', 'OnFailure', 'Never')
nodes:
  prohibit:
  force:
add:
  logs:
  metrics:
  mesh:
```

```yaml
# explanations

annotations: additional deployment/cronjob annotations
priority: the pod priority class
restart: the restart policy for the pod
nodes:
  prohibit: map of key/value node labels that pods should never run on
  force: map of key/value node labels that pods have to run on
add:
  logs: adds logs annotations if defined in default section
  metrics: adds metrics annotations if defined in default section
  mesh: adds service mesh annotations if defined in default section
```
