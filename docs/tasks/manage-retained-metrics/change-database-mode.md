<!--
title: "Change database mode"
sidebar_label: "Change database mode"
custom_edit_url: "https://github.com/netdata/netdata/blob/master/docs/tasks/manage-retained-metrics/change-database-mode.md"
learn_status: "Published"
learn_topic_type: "Tasks"
learn_rel_path: "manage-retained-metrics"
learn_docs_purpose: "Instructions on how to change database mode"
-->

Netdata is fully capable of long-term metric storage, at per-second granularity, via its default database engine
`dbengine`.  
To remain as flexible as possible, Netdata supports several storage options.  
Read more, by checking the [Database Reference](https://github.com/netdata/netdata/blob/master/database/README.md)
documentation.

## Prerequisites

- The Agent installed on a Node
- Terminal access to that node

## Steps

You can select the database mode
by [editing Netdata's configuration](https://github.com/netdata/netdata/blob/master/docs/tasks/general-configuration/configure-the-agent.md)
and setting:

```conf
[db]
    mode = <YOUR OPTION>
```

The available database modes, are:

- `dbengine` (default)
- `ram`
- `save` (the default if `dbengine` not available)
- `map` (swap like)
- `none`
- `alloc`

## Related topics

1. [Metrics Storage Concept](https://github.com/netdata/netdata/blob/master/docs/concepts/netdata-agent/metrics-storage.md)
2. [Database Reference](https://github.com/netdata/netdata/blob/master/database/README.md)