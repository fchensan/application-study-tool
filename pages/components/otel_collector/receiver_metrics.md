---
layout: page
title: BigIP Receiver Metrics
parent: OTEL Collector
grand_parent: Components
nav_order: 2
---
# BigIP Receiver (AST) - Metrics


## Default Metrics

The following metrics are emitted by default. Each of them can be disabled by applying the following configuration:

```yaml
metrics:
  <metric_name>:
    enabled: false
```

1. TOC
{:toc}

### endpoint.scrape.duration

The time spent performing a HTTP request for a particular endpoint

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| s | Gauge | Double |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| path | The path of the endpoint | Any Str |

### endpoint.scrape.requests

The total number of HTTP requests sent to a particular endpoint

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {requests} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| path | The path of the endpoint | Any Str |

### endpoint.scrape.response.size

The size of the received HTTP payload in bytes

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| By | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| path | The path of the endpoint | Any Str |

### endpoint.scrape.responses

The total number of HTTP responses received by the scraper by status

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {responses} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| path | The path of the endpoint | Any Str |
| status_code | The HTTP status code of the response | Any Int |

### f5.apm.access.sessions.current

The current number of APM access sessions by state

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {session} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.apm.session.state | The APM session state for the metric | Str: ``established``, ``active`` |

### f5.apm.access.sessions.limit

The maximum number of APM access sessions

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {session} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |

### f5.apm.sessions.current

The current number of APM sessions by session type

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {session} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.apm.session.type | The APM session type for the metric | Str: ``connectivity``, ``swg``, ``swg_limited`` |

### f5.apm.sessions.limit

The maximum number of APM sessions by session type

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {session} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.apm.session.type | The APM session type for the metric | Str: ``connectivity``, ``swg``, ``swg_limited`` |

### f5.cgnat.lsn_pool.generation

Config Generation of the lsn pool.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {generation} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |

### f5.cgnat.lsn_pool.hairpin_connections.current

Current active hairpin connections for the lsn pool.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {connection} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |

### f5.cgnat.lsn_pool.hairpin_connections.failures

The total failed hairpin connections for the lsn pool.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {connection} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |

### f5.cgnat.lsn_pool.hairpin_connections.requests

The total requested hairpin connections for the lsn pool.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {connection} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |

### f5.cgnat.lsn_pool.pba.clients.limit_reached

The total clients which reached their block allocation limit.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {client} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |

### f5.cgnat.lsn_pool.pba.info

Info about the lsn pool PBA config.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |
| f5.cgnat.lsn_pool.pba.block_idle_timeout | The PBA Block Idle Timeout | Any Int |
| f5.cgnat.lsn_pool.pba.block_lifetime | The PBA Block Idle lifetime | Any Int |
| f5.cgnat.lsn_pool.pba.block_size | The PBA Block Size | Any Int |
| f5.cgnat.lsn_pool.pba.block_client_limit | The PBA Block Client Limit | Any Int |
| f5.cgnat.lsn_pool.pba.block_zombie_timeout | The PBA Block Zombie Timeout | Any Int |

### f5.cgnat.lsn_pool.pba.port_blocks.active

Current active port blocks lsn pool.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {block} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |

### f5.cgnat.lsn_pool.pba.port_blocks.allocation_failures

The total failed port block allocations for the lsn pool.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {allocation} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |

### f5.cgnat.lsn_pool.pba.port_blocks.allocations

The total port block allocations for the lsn pool.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {allocation} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |

### f5.cgnat.lsn_pool.pba.zombie_port_blocks.active

Current active zombie port blocks for the lsn pool.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {block} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |

### f5.cgnat.lsn_pool.pba.zombie_port_blocks.created

The total zombie port block creations for the lsn pool.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {block} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |

### f5.cgnat.lsn_pool.pba.zombie_port_blocks.deleted

The total zombie port block deletions for the lsn pool.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {block} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |

### f5.cgnat.lsn_pool.translations.current

Current active translations for the lsn pool.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {translation} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |

### f5.cgnat.lsn_pool.translations.failures

The total failed translations for the lsn pool.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {translation} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |

### f5.cgnat.lsn_pool.translations.requests

The total requested translations for the lsn pool.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {translation} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |

### f5.dos.attacks

The DoS Attacks for a Vector

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {attack} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.dos.vector_name | The name of the DDoS Vector | Any Str |

### f5.dos.attacks.detected

The DoS Attacks Detected for a Vector

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {attack} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.dos.vector_name | The name of the DDoS Vector | Any Str |

### f5.dos.ba.detected

The Bad Actor detected for a Vector

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {detection} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.dos.vector_name | The name of the DDoS Vector | Any Str |

### f5.dos.ba.drops

The Bad Actor drops for a Vector

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {drop} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.dos.vector_name | The name of the DDoS Vector | Any Str |

### f5.dos.ba.stats

The Bad Actor stats for a Vector

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {stat} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.dos.vector_name | The name of the DDoS Vector | Any Str |

### f5.dos.bd.detected

The BD detected for a Vector

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {detection} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.dos.vector_name | The name of the DDoS Vector | Any Str |

### f5.dos.bd.drops

The BD drops for a Vector

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {drop} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.dos.vector_name | The name of the DDoS Vector | Any Str |

### f5.dos.bd.stats

The BD stats for a Vector

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {stat} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.dos.vector_name | The name of the DDoS Vector | Any Str |

### f5.dos.bytes

The DoS Bytes for a Vector

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| By | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.dos.vector_name | The name of the DDoS Vector | Any Str |

### f5.dos.bytes.drops

The DoS Bytes Dropped for a Vector

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {drop} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.dos.vector_name | The name of the DDoS Vector | Any Str |

### f5.dos.drops

The DoS Drops for a Vector

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {drop} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.dos.vector_name | The name of the DDoS Vector | Any Str |

### f5.dos.stats

The DoS Stats for a Vector

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {stat} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.dos.vector_name | The name of the DDoS Vector | Any Str |

### f5.firewall.rule.hits

The total count of firewall rule hits by rule

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {hit} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.firewall.rule.name | The AFM Firewall rule name | Any Str |
| f5.firewall.rule.stat_type | The AFM Firewall rule stat type | Any Str |
| f5.firewall.rule.action | The AFM Firewall rule action | Any Str |
| f5.firewall.rule.context_name | The context for the AFM Firewall rule stat | Any Str |

### f5.gtm.distributed_app.count

The number of enabled gtm distributed apps

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {items} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |

### f5.gtm.ldnses

The number of ldnses

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {ldnses} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |

### f5.gtm.listener.count

The number of enabled gtm listeners

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {items} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |

### f5.gtm.paths

The number of paths

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {paths} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |

### f5.gtm.requests

The number of requests

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {requests} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.gtm.wideip.name | The name of a wideip | Any Str |

### f5.gtm.rule.count

The number of enabled gtm rules

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {items} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |

### f5.gtm.server.count

The number of enabled gtm servers

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {items} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |

### f5.gtm.wideip.enabled.count

The number of enabled wideips

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {items} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.gtm.wideip.name | The name of a wideip | Any Str |

### f5.license.expires_at

The expiration time of the license.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {epoch_second} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| registration_key | The registration key of the current license | Any Str |

### f5.module.license.info

License status for a bigip module

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.module.name | The name of a module. | Any Str |
| f5.module.license.state | The license status of a module. | Str: ``licensed``, ``unlicensed`` |

### f5.module.provision.generation

Config Generation of the BIG-IP for this provision.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {generation} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.module.name | The name of a module. | Any Str |
| level | The provisioning level of a module | Any Str |

### f5.nethsm.async_queue.done

The total count of async_queue done

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {task} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.nethsm.queue | The id of the nethsm queue | Any Int |

### f5.nethsm.async_queue.done.last_second

The current count of async_queue done tasks in the last 1 second

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {task} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.nethsm.queue | The id of the nethsm queue | Any Int |

### f5.nethsm.async_queue.ops_per_second.avg

The current average of async_queue ops/sec

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {operation} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.nethsm.queue | The id of the nethsm queue | Any Int |

### f5.nethsm.async_queue.queue_time.avg

The average queue time

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| us | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.nethsm.queue | The id of the nethsm queue | Any Int |

### f5.nethsm.async_queue.queue_time.max

The max queue time

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| us | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.nethsm.queue | The id of the nethsm queue | Any Int |

### f5.nethsm.async_queue.queued

The current tasks queued

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {task} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.nethsm.queue | The id of the nethsm queue | Any Int |

### f5.nethsm.async_queue.queued.max

The maximum tasks queued

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {task} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.nethsm.queue | The id of the nethsm queue | Any Int |

### f5.nethsm.pkcs11d.operation.errors

The pkcs11d error statistic

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {error} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.nethsm.thread | The id of the nethsm thread | Any Int |
| f5.nethsm.vendor | The nethsm vendor string | Any Str |
| operation | The pks11d operation types | Str: ``sign``, ``decrypt``, ``find_key``, ``find_key_id``, ``gen_key_rsa``, ``delete_key`` |

### f5.nethsm.pkcs11d.operations

The pkcs11d statistic

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {operation} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.nethsm.thread | The id of the nethsm thread | Any Int |
| f5.nethsm.vendor | The nethsm vendor string | Any Str |
| operation | The pks11d operation types | Str: ``sign``, ``decrypt``, ``find_key``, ``find_key_id``, ``gen_key_rsa``, ``delete_key`` |

### f5.network.address.info

The information for a configured self-ip

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.network.address | The network address | Any Str |
| f5.network.address.name | The name of a network address | Any Str |
| f5.network.address.source | The configuration source of an network address | Any Str |
| f5.network.vlan.name | The name of a VLAN | Any Str |
| f5.network.address.floating | The enabled or disabled state of floating for the network address | Str: ``enabled``, ``disabled`` |

### f5.network.interface.bits_in

The number of bits in

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| bits | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.network.interface.name | The name of a physical network interface | Any Str |

### f5.network.interface.bits_out

The number of bits out

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| bits | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.network.interface.name | The name of a physical network interface | Any Str |

### f5.network.interface.dropped

The number of drops (all) on the interface

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {packet} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.network.interface.name | The name of a physical network interface | Any Str |

### f5.network.interface.enabled

The interface enabled status

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| 1 | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.network.interface.name | The name of a physical network interface | Any Str |

### f5.network.interface.errors

The number of errors (all) on the interface

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {error} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.network.interface.name | The name of a physical network interface | Any Str |

### f5.network.interface.info

Information about the network interface

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.network.interface.name | The name of a physical network interface | Any Str |
| f5.network.interface.index | The index (ifIndex) of a network interface | Any Int |
| f5.network.interface.media_active | The active interface media | Any Str |
| mtu | The MTU for the network interface or VLAN | Any Int |
| mac_address | The mac address of an interface | Any Str |

### f5.network.interface.packets_in

The number of packets in

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {packets} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.network.interface.name | The name of a physical network interface | Any Str |

### f5.network.interface.packets_out

The number of packets out

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {packets} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.network.interface.name | The name of a physical network interface | Any Str |

### f5.network.interface.status

The interface active status

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| 1 | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.network.interface.name | The name of a physical network interface | Any Str |

### f5.network.vlan.broadcast.packets_in

The broadcast packets into the interface

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {packets} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.network.vlan.name | The name of a VLAN | Any Str |
| f5.network.vlan.id | The VLAN identifier / tag | Any Int |

### f5.network.vlan.broadcast.packets_out

The broadcast packets out of the interface

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {packets} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.network.vlan.name | The name of a VLAN | Any Str |
| f5.network.vlan.id | The VLAN identifier / tag | Any Int |

### f5.network.vlan.bytes_in

The number of bytes into the interface

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| By | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.network.vlan.name | The name of a VLAN | Any Str |
| f5.network.vlan.id | The VLAN identifier / tag | Any Int |

### f5.network.vlan.bytes_out

The  number of bytes out of the interface

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| By | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.network.vlan.name | The name of a VLAN | Any Str |
| f5.network.vlan.id | The VLAN identifier / tag | Any Int |

### f5.network.vlan.discards_in

The number of input discards on the vlan

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {discard} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.network.vlan.name | The name of a VLAN | Any Str |
| f5.network.vlan.id | The VLAN identifier / tag | Any Int |

### f5.network.vlan.discards_out

The number of output discards on the vlan

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {discard} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.network.vlan.name | The name of a VLAN | Any Str |
| f5.network.vlan.id | The VLAN identifier / tag | Any Int |

### f5.network.vlan.errors_in

The number of errors into the vlan

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {error} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.network.vlan.name | The name of a VLAN | Any Str |
| f5.network.vlan.id | The VLAN identifier / tag | Any Int |

### f5.network.vlan.errors_out

The number of errors out of the vlan

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {error} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.network.vlan.name | The name of a VLAN | Any Str |
| f5.network.vlan.id | The VLAN identifier / tag | Any Int |

### f5.network.vlan.info

Info about the VLAN

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.network.vlan.name | The name of a VLAN | Any Str |
| f5.network.vlan.id | The VLAN identifier / tag | Any Int |
| mtu | The MTU for the network interface or VLAN | Any Int |
| mac_address | The mac address of an interface | Any Str |

### f5.network.vlan.member.info

Info about the VLAN member interface

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.network.vlan.name | The name of a VLAN | Any Str |
| f5.network.vlan.id | The VLAN identifier / tag | Any Int |
| f5.network.vlan.tag_mode | The tag mode for a VLAN | Any Str |
| f5.network.interface.name | The name of a physical network interface | Any Str |

### f5.network.vlan.multicast.packets_in

The multicast packets into the interface

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {packets} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.network.vlan.name | The name of a VLAN | Any Str |
| f5.network.vlan.id | The VLAN identifier / tag | Any Int |

### f5.network.vlan.multicast.packets_out

The multicast packets out of the interface

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {packets} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.network.vlan.name | The name of a VLAN | Any Str |
| f5.network.vlan.id | The VLAN identifier / tag | Any Int |

### f5.network.vlan.pva.bytes_in

The number of PVA bytes into the interface

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| By | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.network.vlan.name | The name of a VLAN | Any Str |
| f5.network.vlan.id | The VLAN identifier / tag | Any Int |

### f5.network.vlan.pva.bytes_out

The  number of PVA bytes out of the interface

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| By | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.network.vlan.name | The name of a VLAN | Any Str |
| f5.network.vlan.id | The VLAN identifier / tag | Any Int |

### f5.network.vlan.pva.packets_in

The PVA packets into the interface

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {packets} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.network.vlan.name | The name of a VLAN | Any Str |
| f5.network.vlan.id | The VLAN identifier / tag | Any Int |

### f5.network.vlan.pva.packets_out

The PVA packets out of the interface

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {packets} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.network.vlan.name | The name of a VLAN | Any Str |
| f5.network.vlan.id | The VLAN identifier / tag | Any Int |

### f5.network.vlan.unicast.packets_in

The unicast packets into the interface

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {packets} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.network.vlan.name | The name of a VLAN | Any Str |
| f5.network.vlan.id | The VLAN identifier / tag | Any Int |

### f5.network.vlan.unicast.packets_out

The unicast packets out of the interface

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {packets} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.network.vlan.name | The name of a VLAN | Any Str |
| f5.network.vlan.id | The VLAN identifier / tag | Any Int |

### f5.node.availability

Availability of the node.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| 1 | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.node.name | The name of a Node. | Any Str |
| f5.node.ip_address | The IP Address of a Node. | Any Str |
| availability.state | The availability state. | Str: ``offline``, ``unknown``, ``available`` |

### f5.node.bytes_in

Cumulative number of bytes transmitted to the node.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| By | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.node.name | The name of a Node. | Any Str |
| f5.node.ip_address | The IP Address of a Node. | Any Str |

### f5.node.bytes_out

Cumulative number of bytes transmitted from the node.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| By | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.node.name | The name of a Node. | Any Str |
| f5.node.ip_address | The IP Address of a Node. | Any Str |

### f5.node.connection.count

Current number of connections to the node.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {connections} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.node.name | The name of a Node. | Any Str |
| f5.node.ip_address | The IP Address of a Node. | Any Str |

### f5.node.enabled

Enabled state of of the node.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| 1 | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.node.name | The name of a Node. | Any Str |
| f5.node.ip_address | The IP Address of a Node. | Any Str |

### f5.node.packets_in

Cumulative number of packets transmitted to the node.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {packets} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.node.name | The name of a Node. | Any Str |
| f5.node.ip_address | The IP Address of a Node. | Any Str |

### f5.node.packets_out

Cumulative number of packets transmitted from the node.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {packets} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.node.name | The name of a Node. | Any Str |
| f5.node.ip_address | The IP Address of a Node. | Any Str |

### f5.node.requests

Cumulative number of requests to the node.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {requests} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.node.name | The name of a Node. | Any Str |
| f5.node.ip_address | The IP Address of a Node. | Any Str |

### f5.node.session.count

Current number of sessions for the node.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {sessions} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.node.name | The name of a Node. | Any Str |
| f5.node.ip_address | The IP Address of a Node. | Any Str |

### f5.plane.cpu.count

The number of CPU allocated to the plane.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {CPU} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| plane | The name of a plane (e.g. data, control, analysis) | Any Str |

### f5.plane.cpu.utilization

CPU Utilization for this Virtual server over the past 5 seconds.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| 5s | Gauge | Double |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| plane | The name of a plane (e.g. data, control, analysis) | Any Str |

### f5.policy.api_protection.auth_requests

The number of auth requests

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {requests} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.api_protection.name | The name of the api protection policy. | Any Str |
| f5.policy.api_protection.auth_request_type | The name of the request type | Str: ``basic``, ``bearer``, ``other`` |

### f5.policy.api_protection.generation

The version of a api protection policy

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.api_protection.name | The name of the api protection policy. | Any Str |

### f5.policy.api_protection.info

The information about a api protection policy

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.api_protection.name | The name of the api protection policy. | Any Str |
| f5.policy.api_protection.create_security_policy | The state of the create security policy action | Any Str |
| f5.policy.api_protection.security_policy_created | The state of the security policy created action | Any Str |

### f5.policy.api_protection.path.count

The number of paths for the api protection policy

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {paths} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.api_protection.name | The name of the api protection policy. | Any Str |

### f5.policy.api_protection.proxy_failed_requests

The number of failed proxy requests

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {requests} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.api_protection.name | The name of the api protection policy. | Any Str |

### f5.policy.api_protection.proxy_successful_requests

The number of successful proxy requests

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {requests} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.api_protection.name | The name of the api protection policy. | Any Str |

### f5.policy.api_protection.quota_violations

The number of quota violations

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {requests} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.api_protection.name | The name of the api protection policy. | Any Str |

### f5.policy.api_protection.rate_limiting_config.count

The number of rate limiting configs for the api protection policy

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {configs} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.api_protection.name | The name of the api protection policy. | Any Str |

### f5.policy.asm.api_checking.count

The number of API Conformance Checking policies

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {policies} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.asm.name | The name of the waap policy. | Any Str |

### f5.policy.asm.bot-events

Total number of ASM detected Bot Defense Events

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {events} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |

### f5.policy.asm.bot-incidents

Total number of ASM detected Bot Incidents

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {incidents} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |

### f5.policy.asm.brute-force-attacks

Total number of ASM detected Brute Force Attacks

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {attacks} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |

### f5.policy.asm.feature.enabled

Indicates if a WAAP feature is being used

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| 1 | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.asm.name | The name of the waap policy. | Any Str |
| feature | The name of a waap feature | Any Str |

### f5.policy.asm.incidents

Total number of ASM detected WAF incidents

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {incidents} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |

### f5.policy.asm.info

The information for an asm policy

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.asm.name | The name of the waap policy. | Any Str |
| f5.policy.asm.has_parent | Whether the policy has a parent policy. | Any Str |
| f5.policy.asm.enforcement_mode | Whether the policy has a parent policy. | Any Str |

### f5.policy.asm.last_modified_time

The lat modified time of an asm policy

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {epoch_seconds} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.asm.name | The name of the waap policy. | Any Str |

### f5.policy.asm.param_checking.count

The number of WAAP policies that are performing parameter checking

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {policies} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.asm.name | The name of the waap policy. | Any Str |

### f5.policy.asm.signature_set.count

The number of available signature sets

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {signature_set} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.asm.name | The name of the waap policy. | Any Str |

### f5.policy.asm.signature_sets.state.count

The number of signature sets by state

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {signature_set} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.asm.name | The name of the waap policy. | Any Str |
| state | The potential states of a signature set | Str: ``alerting``, ``blocking``, ``learning`` |

### f5.policy.bandwidth_control.bytes_dropped

Cumulative number of bytes dropped by the bandwidth control policy

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| By | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.bandwidth_control.name | The name of the bandwidth control policy. | Any Str |

### f5.policy.bandwidth_control.bytes_in

Cumulative number of bytes transmitted to the bandwidth control policy

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| By | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.bandwidth_control.name | The name of the bandwidth control policy. | Any Str |

### f5.policy.bandwidth_control.bytes_passed

Cumulative number of bytes passed by the bandwidth control policy

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| By | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.bandwidth_control.name | The name of the bandwidth control policy. | Any Str |

### f5.policy.bandwidth_control.generation

The version of a bandwidth control policy

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.bandwidth_control.name | The name of the bandwidth control policy. | Any Str |

### f5.policy.bandwidth_control.info

The information about a bandwidth control policy

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.bandwidth_control.name | The name of the bandwidth control policy. | Any Str |

### f5.policy.bandwidth_control.max_rate.current

The current max rate for the bandwidth control policy

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| By | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.bandwidth_control.name | The name of the bandwidth control policy. | Any Str |

### f5.policy.bandwidth_control.max_user_rate.current

The current max user rate for the bandwidth control policy

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| By | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.bandwidth_control.name | The name of the bandwidth control policy. | Any Str |

### f5.policy.bandwidth_control.max_user_rate_pps.current

The current max user rate pps for the bandwidth control policy

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {packets} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.bandwidth_control.name | The name of the bandwidth control policy. | Any Str |

### f5.policy.bandwidth_control.packets_dropped

Cumulative number of packets dropped by the bandwidth control policy

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {packets} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.bandwidth_control.name | The name of the bandwidth control policy. | Any Str |

### f5.policy.bandwidth_control.packets_in

Cumulative number of packets transmitted to the bandwidth control policy

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {packets} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.bandwidth_control.name | The name of the bandwidth control policy. | Any Str |

### f5.policy.bandwidth_control.packets_passed

Cumulative number of packets passed by the bandwidth control policy

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {packets} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.bandwidth_control.name | The name of the bandwidth control policy. | Any Str |

### f5.policy.eviction.evicted

The number of evicted objects for the eviction policy

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {flows} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.eviction.name | The name of the eviction policy. | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |

### f5.policy.eviction.generation

The version of an eviction policy

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.eviction.name | The name of the eviction policy. | Any Str |

### f5.policy.eviction.info

The information about an eviction policy

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.eviction.name | The name of the eviction policy. | Any Str |
| f5.policy.eviction.slow_flow.enabled | The state of the slow flow eviction policy | Any Str |
| f5.policy.eviction.virtual_server_priorities.enabled | The state of the virtual server priorities eviction policy | Any Str |

### f5.policy.firewall.generation

The version of a firewall policy

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.firewall.name | The name of the firewall policy. | Any Str |

### f5.policy.firewall.info

The information about a firewall policy

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.firewall.name | The name of the firewall policy. | Any Str |
| f5.description | Description string for the object | Any Str |

### f5.policy.firewall.rule.count

The number of rules for the firewall policy

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {rules} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.firewall.name | The name of the firewall policy. | Any Str |

### f5.policy.firewall.rule_hits

The number of hits for a rule in the firewall policy

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {hits} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.firewall.name | The name of the firewall policy. | Any Str |
| f5.policy.firewall.mode | The mode of the firewall policy | Any Str |

### f5.policy.ip_intelligence.feed_list.count

The number of feed lists for the ip intelligence policy

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {feedlists} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.ip_intelligence.name | The name of the ip intelligence policy. | Any Str |

### f5.policy.ip_intelligence.generation

The version of a ip intelligence policy

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.ip_intelligence.name | The name of the ip intelligence policy. | Any Str |

### f5.policy.ip_intelligence.hits

The number of hits for the ip intelligence policy

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {hits} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.ip_intelligence.name | The name of the ip intelligence policy. | Any Str |
| f5.policy.ip_intelligence.hit_type | The name of the ip intelligence policy hit type. | Any Str |

### f5.policy.ip_intelligence.info

The information about a IP Intelligence policy

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.ip_intelligence.name | The name of the ip intelligence policy. | Any Str |
| f5.policy.ip_intelligence.drop_by_default | Indicates if the policy drops by default | Any Str |

### f5.policy.nat.generation

The config generation of a NAT Policy

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.nat.name | The name of the nat policy. | Any Str |

### f5.policy.nat.info

The info object for a NAT Policy

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.nat.name | The name of the nat policy. | Any Str |

### f5.policy.nat.rules.disabled

The number of disabled NAT rules

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {rules} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.nat.name | The name of the nat policy. | Any Str |

### f5.policy.nat.rules.enabled

The number of enabled NAT rules

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {rules} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.nat.name | The name of the nat policy. | Any Str |

### f5.pool.availability

Availability of the pool.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| 1 | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |
| availability.state | The availability state. | Str: ``offline``, ``unknown``, ``available`` |

### f5.pool.availability.threshold

Minimum number of active pool members required.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {members} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |

### f5.pool.bytes_in

Cumulative total number of bytes transmitted to the pool.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| By | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |

### f5.pool.bytes_out

Cumulative total number of bytes transmitted from the pool.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| By | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |

### f5.pool.connection.count

Current number of connections to the pool.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {connections} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |

### f5.pool.connection.max

Maximum number of concurrent connections to the pool.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {connections} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |

### f5.pool.enabled

Enabled state of of the pool.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| 1 | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |

### f5.pool.generation

Generation of the pool

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {generation} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |

### f5.pool.info

Information about the pool

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |
| f5.pool.load_balancing_mode | The load balancing mode of a pool. | Any Str |
| f5.monitor.name | The full path name of a monitor | Any Str |
| f5.pool.min_up_members.action | The action to take when min members threshold is breached | Any Str |
| f5.pool.min_up_members.checking | Whether min up member threshold checking is enabled | Any Str |
| f5.pool.service_down.action | Action to take on pool service down if any | Any Str |

### f5.pool.member.availability

Availability of the pool member.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| 1 | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |
| f5.pool.member.name | The name of a Pool Member. | Any Str |
| f5.pool.member.ip_address | The IP Address of a Pool Member. | Any Str |
| availability.state | The availability state. | Str: ``offline``, ``unknown``, ``available`` |

### f5.pool.member.bytes_in

Cumulative number of bytes transmitted to the pool member.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| By | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |
| f5.pool.member.name | The name of a Pool Member. | Any Str |
| f5.pool.member.ip_address | The IP Address of a Pool Member. | Any Str |

### f5.pool.member.bytes_out

Cumulative number of bytes transmitted from the pool member.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| By | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |
| f5.pool.member.name | The name of a Pool Member. | Any Str |
| f5.pool.member.ip_address | The IP Address of a Pool Member. | Any Str |

### f5.pool.member.connection.count

Current number of connections to the pool member.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {connections} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |
| f5.pool.member.name | The name of a Pool Member. | Any Str |
| f5.pool.member.ip_address | The IP Address of a Pool Member. | Any Str |

### f5.pool.member.connections

Cumulative number of connections to the pool member.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {connections} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |
| f5.pool.member.name | The name of a Pool Member. | Any Str |
| f5.pool.member.ip_address | The IP Address of a Pool Member. | Any Str |

### f5.pool.member.count

Current number of pool members by status.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {members} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |
| active.state | The active state of the system component. | Str: ``active``, ``inactive`` |

### f5.pool.member.enabled

Enabled state of of the pool member.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| 1 | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |
| f5.pool.member.name | The name of a Pool Member. | Any Str |
| f5.pool.member.ip_address | The IP Address of a Pool Member. | Any Str |

### f5.pool.member.packets_in

Cumulative number of packets transmitted to the pool member.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {packets} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |
| f5.pool.member.name | The name of a Pool Member. | Any Str |
| f5.pool.member.ip_address | The IP Address of a Pool Member. | Any Str |

### f5.pool.member.packets_out

Cumulative number of packets transmitted from the pool member.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {packets} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |
| f5.pool.member.name | The name of a Pool Member. | Any Str |
| f5.pool.member.ip_address | The IP Address of a Pool Member. | Any Str |

### f5.pool.member.requests

Cumulative number of requests to the pool member.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {requests} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |
| f5.pool.member.name | The name of a Pool Member. | Any Str |
| f5.pool.member.ip_address | The IP Address of a Pool Member. | Any Str |

### f5.pool.member.session.count

Current number of sessions for the pool member.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {sessions} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |
| f5.pool.member.name | The name of a Pool Member. | Any Str |
| f5.pool.member.ip_address | The IP Address of a Pool Member. | Any Str |

### f5.pool.packets_in

Cumulative total number of packets transmitted to the pool.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {packets} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |

### f5.pool.packets_out

Cumulative total number of packets transmitted from the pool.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {packets} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |

### f5.pool.queue_age.average

Average age of queue entries in this pool, in mseconds

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| ms | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |

### f5.pool.queue_age.recent_max

Recent maximum age of queue entries in this pool, in mseconds

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| ms | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |

### f5.pool.requests

Cumulative total number of requests to the pool.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {requests} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |

### f5.pool.session.count

Current number of sessions to the pool.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {connections} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |

### f5.profile.client_ssl.active_handshake_rejects

The total active handshake rejects.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {handshake} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.client_ssl.name | The name of an SSL Profile | Any Str |

### f5.profile.client_ssl.bytes_in

The total bytes in by encryption status

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| By | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.client_ssl.name | The name of an SSL Profile | Any Str |
| encryption.state | The type of traffic encrypted/decrypted. | Str: ``encrypted``, ``decrypted`` |

### f5.profile.client_ssl.bytes_out

The total bytes out by encryption status

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| By | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.client_ssl.name | The name of an SSL Profile | Any Str |
| encryption.state | The type of traffic encrypted/decrypted. | Str: ``encrypted``, ``decrypted`` |

### f5.profile.client_ssl.cipher_uses

The total uses by Cipher

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {uses} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.client_ssl.name | The name of an SSL Profile | Any Str |
| f5.profile.client_ssl.ciphers | The ciphers enabled on an ssl profile | Any Str |

### f5.profile.client_ssl.connection.count

The SSL Client connections current value

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {connection} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.client_ssl.name | The name of an SSL Profile | Any Str |

### f5.profile.client_ssl.connection.max

The SSL Client connections maximum value

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {connection} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.client_ssl.name | The name of an SSL Profile | Any Str |

### f5.profile.client_ssl.connections

The SSL Client connections total value

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {connection} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.client_ssl.name | The name of an SSL Profile | Any Str |

### f5.profile.client_ssl.fatal_alerts

The total number of fatal alerts for the profile.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {alerts} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.client_ssl.name | The name of an SSL Profile | Any Str |

### f5.profile.client_ssl.generation

The config generation of a client SSL Profile

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.client_ssl.name | The name of an SSL Profile | Any Str |

### f5.profile.client_ssl.handshake.count

The current number of handshakes.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {handshake} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.client_ssl.name | The name of an SSL Profile | Any Str |

### f5.profile.client_ssl.handshake_failures

The total handshake failures.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {handshake} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.client_ssl.name | The name of an SSL Profile | Any Str |

### f5.profile.client_ssl.handshake_offloads

The total handshakes offloaded.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {handshake} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.client_ssl.name | The name of an SSL Profile | Any Str |

### f5.profile.client_ssl.handshake_softwares

The total handshakes processed in software.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {handshake} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.client_ssl.name | The name of an SSL Profile | Any Str |

### f5.profile.client_ssl.info

The information about a client SSL Profile

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.client_ssl.name | The name of an SSL Profile | Any Str |
| f5.description | Description string for the object | Any Str |
| f5.defaults_from.name | Name of the object from which default settings are inherited | Any Str |
| f5.ssl_certificate.name | The Full path name of the SSL cert or bundle | Any Str |
| f5.ssl_certificate.key_name | The certificate key name | Any Str |
| f5.profile.client_ssl.ciphers | The ciphers enabled on an ssl profile | Any Str |
| f5.profile.client_ssl.options | The options set on an SSL Profile | Any Str |
| f5.profile.client_ssl.renegotiation | The renegotiation setting of the SSL Profile | Any Str |

### f5.profile.client_ssl.insecure_handshake_accepts

The total insecure handshakes accepted.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {handshake} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.client_ssl.name | The name of an SSL Profile | Any Str |

### f5.profile.client_ssl.insecure_handshake_rejects

The total insecure handshakes rejected.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {handshake} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.client_ssl.name | The name of an SSL Profile | Any Str |

### f5.profile.client_ssl.peer_certificates

The cumulative total of peer certificates by validity

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {certificates} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.client_ssl.name | The name of an SSL Profile | Any Str |
| f5.peer_certificate.state | The state of the peer_certificate presented | Str: ``valid``, ``invalid``, ``none`` |

### f5.profile.client_ssl.premature_disconnects

The total number of premature disconnects.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {connections} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.client_ssl.name | The name of an SSL Profile | Any Str |

### f5.profile.client_ssl.protocol_uses

The total uses by protocol

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {uses} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.client_ssl.name | The name of an SSL Profile | Any Str |
| f5.profile.client_ssl.protocol | The SSL protocol used by a profile | Any Str |

### f5.profile.client_ssl.records_in

The total records into the SSL profile

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {record} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.client_ssl.name | The name of an SSL Profile | Any Str |

### f5.profile.client_ssl.records_out

The total records out of the SSL profile

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {record} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.client_ssl.name | The name of an SSL Profile | Any Str |

### f5.profile.client_ssl.rejected_renegotiations

The total aggregate rejected renegotiations for the profile

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {connections} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.client_ssl.name | The name of an SSL Profile | Any Str |

### f5.profile.client_ssl.secure_handshakes

The total secure handshakes processed.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {handshake} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.client_ssl.name | The name of an SSL Profile | Any Str |

### f5.profile.dns.axfr_queries

The number of axfr queries

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {queries} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.dns.name | The name of a dns profile | Any Str |

### f5.profile.dns.bits_in

The number of bits in

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| bits | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.dns.name | The name of a dns profile | Any Str |

### f5.profile.dns.bits_out

The number of bits out

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| bits | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.dns.name | The name of a dns profile | Any Str |

### f5.profile.dns.client_hits

The number of client hits

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {hits} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.dns.name | The name of a dns profile | Any Str |

### f5.profile.dns.client_hits_response_time

The response time of client hits

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| ms | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.dns.name | The name of a dns profile | Any Str |

### f5.profile.dns.client_misses

The number of client misses

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {misses} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.dns.name | The name of a dns profile | Any Str |

### f5.profile.dns.client_misses_response_time

The response time of client misses

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| ms | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.dns.name | The name of a dns profile | Any Str |

### f5.profile.dns.dnsx.query_type

The number of dnsx query by types

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {qtype} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.dns.name | The name of a dns profile | Any Str |
| f5.profile.dns.dnsx.qtype | The qtype for the dns dnsx dns query | Any Str |

### f5.profile.dns.dnsx_queries

The number of dnsx queries

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {queries} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.dns.name | The name of a dns profile | Any Str |

### f5.profile.dns.dnsx_responses

The number of dnsx responses

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {responses} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.dns.name | The name of a dns profile | Any Str |

### f5.profile.dns.edns.request

The number of DNS EDNS0CsQueries

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {requests} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.dns.name | The name of a dns profile | Any Str |

### f5.profile.dns.edns.response

The number of DNS EDNS0CsResponses

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {responses} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.dns.name | The name of a dns profile | Any Str |

### f5.profile.dns.generation

The config generation of a DNS Profile

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.dns.name | The name of a dns profile | Any Str |

### f5.profile.dns.info

The information about a DNS Profile

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.dns.name | The name of a dns profile | Any Str |
| f5.defaults_from.name | Name of the object from which default settings are inherited | Any Str |
| f5.profile.dns.app_service | The app service for the dns profile | Any Str |
| f5.profile.dns.security | The security for the dns profile | Any Str |
| f5.profile.dns.dns64 | The dns64 state for the dns profile | Str: ``true``, ``false`` |
| f5.profile.dns.local_bind | The local bind for the dns profile | Str: ``true``, ``false`` |
| f5.profile.dns.unhandled_query_action | The unhandled query action for the dns profile | Any Str |
| f5.profile.dns.cache.enabled | The enable cache for the dns profile | Str: ``true``, ``false`` |
| f5.profile.dns.dns_express.enabled | The enable dns express for the dns profile | Str: ``true``, ``false`` |
| f5.profile.dns.dns_firewall.enabled | The enable dns firewall for the dns profile | Str: ``true``, ``false`` |
| f5.profile.dns.dnssec.enabled | The enable dnssec for the dns profile | Str: ``true``, ``false`` |
| f5.profile.dns.gtm.enabled | The enable gtm for the dns profile | Str: ``true``, ``false`` |
| f5.profile.dns.hardware_query_validation.enabled | The enable hardware query validation for the dns profile | Str: ``true``, ``false`` |
| f5.profile.dns.hardware_response_cache.enabled | The enable hardware response cache for the dns profile | Str: ``true``, ``false`` |

### f5.profile.dns.ixfr_queries

The number of ixfr queries

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {queries} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.dns.name | The name of a dns profile | Any Str |

### f5.profile.dns.msg_evictions

The number of message evictions

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {evictions} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.dns.name | The name of a dns profile | Any Str |

### f5.profile.dns.msg_hits

The number of message hits

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {hits} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.dns.name | The name of a dns profile | Any Str |

### f5.profile.dns.msg_misses

The number of message misses

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {misses} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.dns.name | The name of a dns profile | Any Str |

### f5.profile.dns.msg_modifications

The number of message modifications

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {modifications} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.dns.name | The name of a dns profile | Any Str |

### f5.profile.dns.packets_in

The number of packets in

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| packets | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.dns.name | The name of a dns profile | Any Str |

### f5.profile.dns.packets_out

The number of packets out

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| packets | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.dns.name | The name of a dns profile | Any Str |

### f5.profile.dns.request

The number of DNS requests

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {requests} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.dns.name | The name of a dns profile | Any Str |

### f5.profile.dns.request_by_type

The number of DNS requests by type

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {requests} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.dns.name | The name of a dns profile | Any Str |
| f5.profile.dns.request_type | The request type for the dns profile | Any Str |

### f5.profile.dns.response

The number of DNS responses

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {responses} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.dns.name | The name of a dns profile | Any Str |

### f5.profile.dns.response_by_return_code

The number of DNS responses by return codes

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {responses} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.dns.name | The name of a dns profile | Any Str |
| f5.profile.dns.return_code_type | The return code type for the dns profile | Any Str |

### f5.profile.dns.response_by_type

The number of DNS responses by type

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {responses} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.dns.name | The name of a dns profile | Any Str |
| f5.profile.dns.response_type | The response type for the dns profile | Any Str |

### f5.profile.dns.server_queries

The number of server queries

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {queries} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.dns.name | The name of a dns profile | Any Str |

### f5.profile.dns.server_queries_rate

The rate of DNS queries

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| requests/s | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.dns.name | The name of a dns profile | Any Str |

### f5.profile.dns.server_responses

The number of server responses

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {responses} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.dns.name | The name of a dns profile | Any Str |

### f5.profile.dns.tcp_bits_in

The number of tcp bits in

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| bits | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.dns.name | The name of a dns profile | Any Str |

### f5.profile.dns.tcp_bits_out

The number of tcp bits out

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| bits | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.dns.name | The name of a dns profile | Any Str |

### f5.profile.dns.xfr_notifies_sent

The number of xfr notifies sent

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {notifies} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.dns.name | The name of a dns profile | Any Str |

### f5.profile.dos.generation

The config generation of a DOS Profile

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.dos.name | The name of a dos profile | Any Str |

### f5.profile.dos.info

The information about a DOS Profile

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.dos.name | The name of a dos profile | Any Str |
| f5.defaults_from.name | Name of the object from which default settings are inherited | Any Str |
| f5.description | Description string for the object | Any Str |
| f5.profile.dos.http_protection_state | Indicates whether the http(app) protection is enabled on the dos profile | Any Str |
| f5.profile.dos.network_protection_state | Indicates whether the network protection is enabled on the dos profile | Any Str |
| f5.profile.dos.dns_protection_state | Indicates whether the dns protection is enabled on the dos profile | Any Str |
| f5.profile.dos.sip_protection_state | Indicates whether the sip protection is enabled on the dos profile | Any Str |
| f5.profile.dos.custom_signature_protection_state | Indicates whether the custom signatures protection is enabled on the dos profile | Any Str |

### f5.profile.dos.last_modified_time

The last modified time of the DOS Profile

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {epoch_second} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.dos.name | The name of a dos profile | Any Str |

### f5.profile.fasthttp.client_accepts

The number of client accepts.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {connections} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.fasthttp.name | The name of a fasthttp profile | Any Str |

### f5.profile.fasthttp.client_syns

The number of client syns.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {connections} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.fasthttp.name | The name of a fasthttp profile | Any Str |

### f5.profile.fasthttp.connection_pool_size

The current connection pool size.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {connections} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.fasthttp.name | The name of a fasthttp profile | Any Str |

### f5.profile.fasthttp.exhausted_connection_pools

The number of exhausted connection pools.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {connections} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.fasthttp.name | The name of a fasthttp profile | Any Str |

### f5.profile.fasthttp.generation

The config generation of a FastHTTP Profile

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.fasthttp.name | The name of a fasthttp profile | Any Str |

### f5.profile.fasthttp.info

The information about a Fast HTTP Profile

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.fasthttp.name | The name of a fasthttp profile | Any Str |
| f5.defaults_from.name | Name of the object from which default settings are inherited | Any Str |
| f5.profile.fasthttp.conn_pool_max_size | The connection pool Max size for a fasthttp profile | Any Int |
| f5.profile.fasthttp.hardware_syn_cookie | Indicates if hardware syn cookie is enabled on the profile | Any Str |
| f5.profile.fasthttp.idle_timeout | Indicates the idle timeout on the fasthttp profile | Any Int |
| f5.profile.fasthttp.insertXforwarded_for | Indicates if the X-Forwarded-For header is enabled on the profile | Any Str |
| f5.profile.fasthttp.server_close_timeout | Indicates the server connection close time for the fasthttp profile | Any Int |

### f5.profile.fasthttp.pipelined_requests

The number of pipelined requests.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {requests} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.fasthttp.name | The name of a fasthttp profile | Any Str |

### f5.profile.fasthttp.requests

The number of requests.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {requests} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.fasthttp.name | The name of a fasthttp profile | Any Str |

### f5.profile.fasthttp.requests.by_method

The number of requests with the specified method.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {requests} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.fasthttp.name | The name of a fasthttp profile | Any Str |
| http.method | The HTTP request method. | Str: ``GET``, ``HEAD``, ``POST``, ``PUT``, ``DELETE``, ``TRACE``, ``OPTIONS``, ``PATCH`` |

### f5.profile.fasthttp.requests.by_version

The number of requests with the specified HTTP version.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {requests} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.fasthttp.name | The name of a fasthttp profile | Any Str |
| http.version | The HTTP version. | Str: ``v0.9``, ``v1.0``, ``v1.1``, ``v2.0``, ``v3.0`` |

### f5.profile.fasthttp.responses

The number of responses in the specified range.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {responses} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.fasthttp.name | The name of a fasthttp profile | Any Str |
| http.status_range | The HTTP Status code range in blocks of 100. | Str: ``1xx``, ``2xx``, ``3xx``, ``4xx``, ``5xx`` |

### f5.profile.fastl4.accept_fails

The number of connection accepts that failed

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {connections} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.fastl4.name | The name of a fastl4 profile | Any Str |

### f5.profile.fastl4.accepts

The number of connections accepted by the FastL4 profile

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {connections} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.fastl4.name | The name of a fastl4 profile | Any Str |

### f5.profile.fastl4.expires

The number of connections that expired

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {connections} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.fastl4.name | The name of a fastl4 profile | Any Str |

### f5.profile.fastl4.generation

The config generation of a FastL4 profile

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.fastl4.name | The name of a fastl4 profile | Any Str |

### f5.profile.fastl4.info

The information about a Fast L4 Profile

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.fastl4.name | The name of a fastl4 profile | Any Str |
| f5.defaults_from.name | Name of the object from which default settings are inherited | Any Str |
| f5.profile.fastl4.client_timeout | The client timeout for a fastl4 profile | Any Int |
| f5.profile.fastl4.hardware_syn_cookie | Indicates if hardware syn cookie is enabled on the profile | Any Str |
| f5.profile.fastl4.idle_timeout | Indicates the idle timeout on the fastl4 profile | Any Str |
| f5.profile.fastl4.loose_initialization | Indicates if loose initialization is enabled on the profile | Any Str |
| f5.profile.fastl4.loose_close | Indicates if loose close is enabled on the profile | Any Str |
| f5.profile.fastl4.pva_acceleration | Indicates if PVA Acceleration is enabled on the profile | Any Str |
| f5.profile.fastl4.mss_override | Indicates if mss overide is enabled on the profile | Any Str |
| f5.profile.fastl4.receive_window_size | Indicates the receive window size on the profile | Any Int |
| f5.profile.fastl4.reset_on_timeout | Indicates if reset on timeout is enabled on the profile | Any Str |
| f5.profile.fastl4.software_syn_cookie | Indicates if software syn cookie is enabled on the profile | Any Str |
| f5.profile.fastl4.syn_cookie_enable | Indicates if syn cookie is enabled on the profile | Any Str |
| f5.profile.fastl4.tcp_close_timeout | Indicates the tcp close timeout on the profile | Any Str |
| f5.profile.fastl4.tcp_handshake_timeout | Indicates the tcp handshake timeout on the profile | Any Str |

### f5.profile.fastl4.open

The number of connections opened

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {connections} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.fastl4.name | The name of a fastl4 profile | Any Str |

### f5.profile.fastl4.rx_badpkts

The number of bad packets received

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {packets} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.fastl4.name | The name of a fastl4 profile | Any Str |

### f5.profile.fastl4.rx_badsums

The number of bad checksums received

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {packets} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.fastl4.name | The name of a fastl4 profile | Any Str |

### f5.profile.fastl4.rx_unreachs

The number of unreachable packets received

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {packets} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.fastl4.name | The name of a fastl4 profile | Any Str |

### f5.profile.fastl4.syn_cookies_accepted

The number of syn cookies accepted

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {cookies} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.fastl4.name | The name of a fastl4 profile | Any Str |

### f5.profile.fastl4.syn_cookies_issued

The number of syn cookies issued

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {cookies} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.fastl4.name | The name of a fastl4 profile | Any Str |

### f5.profile.fastl4.syn_cookies_rejected

The number of syn cookies rejected

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {cookies} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.fastl4.name | The name of a fastl4 profile | Any Str |

### f5.profile.fastl4.tx_errors

The number of transmission errors

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {error} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.fastl4.name | The name of a fastl4 profile | Any Str |

### f5.profile.http.generation

The information about an HTTP Profile

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.http.name | The name of an HTTP Profile | Any Str |

### f5.profile.http.info

The information about an HTTP Profile

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.http.name | The name of an HTTP Profile | Any Str |
| f5.description | Description string for the object | Any Str |
| f5.defaults_from.name | Name of the object from which default settings are inherited | Any Str |
| f5.server_agent.name | The name of the server Agent | Any Str |
| f5.profile.http.enforcement.max_header_size | The configured enforcement max header size for the profile | Any Int |
| f5.profile.http.enforcement.pipeline | The configured enforcement pipeline action for the profile | Any Str |
| f5.profile.http.enforcement.unknown_method | The configured enforcement unknown method action for the profile | Any Str |
| f5.profile.http.enforcement.known_method.count | The configured enforcement count of known methods for the profile | Any Int |
| f5.profile.http.explicit_proxy.bad_request_message | The configured explicit proxy bad request message | Any Str |
| f5.profile.http.explicit_proxy.bad_response_message | The configured explicit proxy bad response message | Any Str |
| f5.profile.http.explicit_proxy.default_connect_handling | The configured explicit proxy default connect handling action | Any Str |

### f5.profile.http.requests

The number of client-side requests.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {requests} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.http.name | The name of an HTTP Profile | Any Str |

### f5.profile.http.requests.by_method

The number of client-side requests with the specified method.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {requests} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.http.name | The name of an HTTP Profile | Any Str |
| http.method | The HTTP request method. | Str: ``GET``, ``HEAD``, ``POST``, ``PUT``, ``DELETE``, ``TRACE``, ``OPTIONS``, ``PATCH`` |

### f5.profile.http.requests.by_version

The number of client-side requests with the specified HTTP version.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {requests} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.http.name | The name of an HTTP Profile | Any Str |
| http.version | The HTTP version. | Str: ``v0.9``, ``v1.0``, ``v1.1``, ``v2.0``, ``v3.0`` |

### f5.profile.http.requests.passthrough

The number of passthrough requests of the specified type

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {requests} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.http.name | The name of an HTTP Profile | Any Str |
| f5.profile.http.passthrough_type | The type of HTTP passthrough request | Str: ``unknown_method``, ``web_socket`` |

### f5.profile.http.responses.by_status

The number of server-side responses in the specified range.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {responses} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.http.name | The name of an HTTP Profile | Any Str |
| http.status_range | The HTTP Status code range in blocks of 100. | Str: ``1xx``, ``2xx``, ``3xx``, ``4xx``, ``5xx`` |

### f5.profile.http.responses.by_version

The number of server-side responses of the specified HTTP protocol version.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {responses} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.http.name | The name of an HTTP Profile | Any Str |
| http.version | The HTTP version. | Str: ``v0.9``, ``v1.0``, ``v1.1``, ``v2.0``, ``v3.0`` |

### f5.profile.http2.connection.accepts

The number of http2 connections accepted

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {connections} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.http2.name | The name of an HTTP2 Profile | Any Str |

### f5.profile.http2.connection.count

The current HTTP2 connection count

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {connections} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.http2.name | The name of an HTTP2 Profile | Any Str |

### f5.profile.http2.connection.max

The max concurrent HTTP2 connection count

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {connections} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.http2.name | The name of an HTTP2 Profile | Any Str |

### f5.profile.http2.flow.count

The current HTTP2 flow count

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {flows} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.http2.name | The name of an HTTP2 Profile | Any Str |

### f5.profile.http2.flow.max

The max concurrent HTTP2 flow count

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {flows} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.http2.name | The name of an HTTP2 Profile | Any Str |

### f5.profile.http2.flows

The number of http2 flows created

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {flows} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.http2.name | The name of an HTTP2 Profile | Any Str |

### f5.profile.http2.generation

The information about an HTTP2 Profile

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.http2.name | The name of an HTTP2 Profile | Any Str |

### f5.profile.http2.info

The information about an HTTP2 Profile

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.http2.name | The name of an HTTP2 Profile | Any Str |
| f5.description | Description string for the object | Any Str |
| f5.defaults_from.name | Name of the object from which default settings are inherited | Any Str |
| f5.profile.http2.concurrent_streams_per_connection | The number of concurrent streams per connection for a http2 profile | Any Int |
| f5.profile.http2.enforce_tls_requirements | The enforcement of TLS requirements for a http2 profile | Any Str |

### f5.profile.http2.request.bytes

The number of http2 request bytes processed

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| By | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.http2.name | The name of an HTTP2 Profile | Any Str |

### f5.profile.http2.request.frames

The number of http2 request frames processed

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {frames} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.http2.name | The name of an HTTP2 Profile | Any Str |

### f5.profile.http2.response.bytes

The number of http2 response bytes processed

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| By | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.http2.name | The name of an HTTP2 Profile | Any Str |

### f5.profile.http2.response.frames

The number of http2 response frames processed

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {frames} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.http2.name | The name of an HTTP2 Profile | Any Str |

### f5.profile.http3.generation

The config generation of an HTTP3 Profile

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.http3.name | The name of a http3 profile | Any Str |

### f5.profile.http3.info

The information about an HTTP3 Profile

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.http3.name | The name of a http3 profile | Any Str |
| f5.description | Description string for the object | Any Str |
| f5.defaults_from.name | Name of the object from which default settings are inherited | Any Str |
| f5.profile.http3.app_service | The app service for the http3 profile | Any Str |
| f5.profile.http3.header_table_size | The header table size for the http3 profile | Any Int |

### f5.profile.http3.request.bytes

The number of http3 request bytes processed

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| By | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.http3.name | The name of a http3 profile | Any Str |

### f5.profile.http3.request.frames

The number of http3 request frames processed

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {frames} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.http3.name | The name of a http3 profile | Any Str |

### f5.profile.http3.response.bytes

The number of http3 response bytes processed

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| By | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.http3.name | The name of a http3 profile | Any Str |

### f5.profile.http3.response.frames

The number of http3 response frames processed

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {frames} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.http3.name | The name of a http3 profile | Any Str |

### f5.profile.one_connect.connections

The number of connections for the One-Connect Profile

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {connections} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.one_connect.name | The name of a one_connect profile | Any Str |

### f5.profile.one_connect.generation

The config generation of a One-Connect Profile

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.one_connect.name | The name of a one_connect profile | Any Str |

### f5.profile.one_connect.info

The information about a One-Connect Profile

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.one_connect.name | The name of a one_connect profile | Any Str |
| f5.defaults_from.name | Name of the object from which default settings are inherited | Any Str |
| f5.profile.one_connect.max_size | The max size setting of a one_connect profile | Any Int |
| f5.profile.one_connect.max_reuse | The max reuse setting of a one_connect profile | Any Int |
| f5.profile.one_connect.share_pools | The share pools setting of a one_connect profile | Any Str |

### f5.profile.one_connect.reuses

The number of reuses for the One-Connect Profile

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {reuses} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.one_connect.name | The name of a one_connect profile | Any Str |

### f5.profile.quic.application.bytes_in

The number of application bytes received for the profile

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| By | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.quic.name | The name of a quic profile | Any Str |

### f5.profile.quic.application.bytes_out

The number of application bytes sent for the profile

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| By | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.quic.name | The name of a quic profile | Any Str |

### f5.profile.quic.connection.count

The current number of active quic connections

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {connections} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.quic.name | The name of a quic profile | Any Str |

### f5.profile.quic.connections

The number of accepted connections for the QUIC Profile

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {connections} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.quic.name | The name of a quic profile | Any Str |

### f5.profile.quic.generation

The config generation of a Quic Profile

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.quic.name | The name of a quic profile | Any Str |

### f5.profile.quic.info

The information about a Quic Profile

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.quic.name | The name of a quic profile | Any Str |
| f5.defaults_from.name | Name of the object from which default settings are inherited | Any Str |
| f5.profile.quic.uni_concurrent_streams_per_connection | The number of unidirectional concurrent streams per connection | Any Int |
| f5.profile.quic.bidi_concurrent_streams_per_connection | The number of bidirectional concurrent streams per connection | Any Int |

### f5.profile.quic.packets.accepted

The number of accepted packets for the profile

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {packets} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.quic.name | The name of a quic profile | Any Str |

### f5.profile.quic.packets.acked

The number of acked packets for the profile

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {packets} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.quic.name | The name of a quic profile | Any Str |

### f5.profile.quic.packets.dropped

The number of dropped packets for the profile

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {packets} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.quic.name | The name of a quic profile | Any Str |

### f5.profile.quic.packets.lost

The number of lost packets for the profile

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {packets} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.quic.name | The name of a quic profile | Any Str |

### f5.profile.quic.ping.frames_in

The number of ping frames received for the profile

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {frames} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.quic.name | The name of a quic profile | Any Str |

### f5.profile.quic.ping.frames_out

The number of ping frames sent for the profile

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {frames} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.quic.name | The name of a quic profile | Any Str |

### f5.profile.quic.stream.count

The current number of active quic streams

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {streams} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.quic.name | The name of a quic profile | Any Str |

### f5.profile.quic.streams

The number of streams created

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {streams} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.quic.name | The name of a quic profile | Any Str |

### f5.profile.server_ssl.active_handshake_rejects

The total active handshake rejects.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {handshake} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.server_ssl.name | The name of an SSL Profile | Any Str |

### f5.profile.server_ssl.bytes_in

The total bytes in by encryption status

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| By | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.server_ssl.name | The name of an SSL Profile | Any Str |
| encryption.state | The type of traffic encrypted/decrypted. | Str: ``encrypted``, ``decrypted`` |

### f5.profile.server_ssl.bytes_out

The total bytes out by encryption status

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| By | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.server_ssl.name | The name of an SSL Profile | Any Str |
| encryption.state | The type of traffic encrypted/decrypted. | Str: ``encrypted``, ``decrypted`` |

### f5.profile.server_ssl.cipher_uses

The total uses by Cipher

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {uses} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.server_ssl.name | The name of an SSL Profile | Any Str |
| f5.profile.server_ssl.ciphers | The ciphers enabled on an ssl profile | Any Str |

### f5.profile.server_ssl.connection.count

The SSL server connections current value

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {connection} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.server_ssl.name | The name of an SSL Profile | Any Str |

### f5.profile.server_ssl.connection.max

The SSL server connections maximum value

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {connection} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.server_ssl.name | The name of an SSL Profile | Any Str |

### f5.profile.server_ssl.connections

The SSL server connections total value

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {connection} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.server_ssl.name | The name of an SSL Profile | Any Str |

### f5.profile.server_ssl.fatal_alerts

The total number of fatal alerts for the profile.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {alerts} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.server_ssl.name | The name of an SSL Profile | Any Str |

### f5.profile.server_ssl.generation

The config generation of a server SSL Profile

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.server_ssl.name | The name of an SSL Profile | Any Str |

### f5.profile.server_ssl.handshake.count

The current number of handshakes.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {handshake} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.server_ssl.name | The name of an SSL Profile | Any Str |

### f5.profile.server_ssl.handshake_failures

The total handshake failures.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {handshake} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.server_ssl.name | The name of an SSL Profile | Any Str |

### f5.profile.server_ssl.handshake_offloads

The total handshakes offloaded.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {handshake} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.server_ssl.name | The name of an SSL Profile | Any Str |

### f5.profile.server_ssl.handshake_softwares

The total handshakes processed in software.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {handshake} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.server_ssl.name | The name of an SSL Profile | Any Str |

### f5.profile.server_ssl.info

The information about a server SSL Profile

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.server_ssl.name | The name of an SSL Profile | Any Str |
| f5.description | Description string for the object | Any Str |
| f5.defaults_from.name | Name of the object from which default settings are inherited | Any Str |
| f5.ssl_certificate.name | The Full path name of the SSL cert or bundle | Any Str |
| f5.ssl_certificate.key_name | The certificate key name | Any Str |
| f5.profile.server_ssl.ciphers | The ciphers enabled on an ssl profile | Any Str |
| f5.profile.server_ssl.max_active_handshakes | The renegotiation setting of the SSL Profile | Any Str |
| f5.profile.server_ssl.allow_expired_crl | The renegotiation setting of the SSL Profile | Any Str |
| f5.profile.server_ssl.renegotiation | The renegotiation setting of the SSL Profile | Any Str |

### f5.profile.server_ssl.insecure_handshake_accepts

The total insecure handshakes accepted.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {handshake} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.server_ssl.name | The name of an SSL Profile | Any Str |

### f5.profile.server_ssl.insecure_handshake_rejects

The total insecure handshakes rejected.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {handshake} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.server_ssl.name | The name of an SSL Profile | Any Str |

### f5.profile.server_ssl.peer_certificates

The cumulative total of peer certificates by validity

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {certificates} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.server_ssl.name | The name of an SSL Profile | Any Str |
| f5.peer_certificate.state | The state of the peer_certificate presented | Str: ``valid``, ``invalid``, ``none`` |

### f5.profile.server_ssl.premature_disconnects

The total number of premature disconnects.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {connections} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.server_ssl.name | The name of an SSL Profile | Any Str |

### f5.profile.server_ssl.protocol_uses

The total uses by protocol

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {uses} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.server_ssl.name | The name of an SSL Profile | Any Str |
| f5.profile.server_ssl.protocol | The SSL protocol used by a profile | Any Str |

### f5.profile.server_ssl.records_in

The total records into the SSL profile

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {record} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.server_ssl.name | The name of an SSL Profile | Any Str |

### f5.profile.server_ssl.records_out

The total records out of the SSL profile

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {record} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.server_ssl.name | The name of an SSL Profile | Any Str |

### f5.profile.server_ssl.secure_handshakes

The total secure handshakes processed.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {handshake} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.server_ssl.name | The name of an SSL Profile | Any Str |

### f5.profile.tcp.abandons

The number of connections abandoned with the TCP Profile

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {connections} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.tcp.name | The name of a tcp profile | Any Str |

### f5.profile.tcp.accept_fails

The number of connections accepted that failed with the TCP Profile

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {connections} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.tcp.name | The name of a tcp profile | Any Str |

### f5.profile.tcp.accepts

The number of connections accepted with the TCP Profile

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {connections} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.tcp.name | The name of a tcp profile | Any Str |

### f5.profile.tcp.connection_fails

The number of connections fails with the TCP Profile

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {connections} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.tcp.name | The name of a tcp profile | Any Str |

### f5.profile.tcp.connections

The number of connections with the TCP Profile

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {connections} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.tcp.name | The name of a tcp profile | Any Str |

### f5.profile.tcp.generation

The config generation of a TCP Profile

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.tcp.name | The name of a tcp profile | Any Str |

### f5.profile.tcp.info

The information about a TCP Profile

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.tcp.name | The name of a tcp profile | Any Str |
| f5.defaults_from.name | Name of the object from which default settings are inherited | Any Str |
| f5.profile.tcp.syn_cookie_enabled | Indicates if syn cookie is enabled on the profile | Any Str |
| f5.profile.tcp.hardware_syn_cookie | Indicates if hardware syn cookie is enabled on the profile | Any Str |
| f5.profile.tcp.fast_open | Indicates if fast open is enabled on the profile | Any Str |
| f5.profile.tcp.idle_timeout | Indicates the idle timeout on the tcp profile | Any Int |
| f5.profile.tcp.keep_alive_interval | Indicates the keep alive interval on the tcp profile | Any Int |
| f5.profile.tcp.max_segment_size | Indicates the max segment size on the tcp profile | Any Int |
| f5.profile.tcp.mptcp | Indicates if mptcp is enabled on the profile | Any Str |
| f5.profile.tcp.nagle | Indicates if nagle is enabled on the profile | Any Str |
| f5.profile.tcp.slow_start | Indicates if slow start is enabled on the profile | Any Str |
| f5.profile.tcp.receive_window_size | Indicates the receive window size on the profile | Any Int |
| f5.profile.tcp.send_buffer_size | Indicates the send buffer size on the profile | Any Int |
| f5.profile.tcp.tcp_options | Indicates the tcp options on the profile | Any Str |

### f5.profile.tcp.open

The number of open connections with the TCP Profile

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {connections} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.tcp.name | The name of a tcp profile | Any Str |

### f5.profile.tcp.rx_badsums

The number of received segments with bad checksums

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {segments} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.tcp.name | The name of a tcp profile | Any Str |

### f5.profile.tcp.tx_rexmits

The number of transmited rexmits

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {segments} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.tcp.name | The name of a tcp profile | Any Str |

### f5.profile.udp.accept_fails

The number of failed UDP accepts

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {connections} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.udp.name | The name of a udp profile | Any Str |

### f5.profile.udp.accepts

The number of UDP accepts

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {connections} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.udp.name | The name of a udp profile | Any Str |

### f5.profile.udp.connection_fails

The number of failed UDP connections

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {connections} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.udp.name | The name of a udp profile | Any Str |

### f5.profile.udp.connections

The number of UDP connections

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {connections} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.udp.name | The name of a udp profile | Any Str |

### f5.profile.udp.expires

The number of expired datagrams

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {datagrams} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.udp.name | The name of a udp profile | Any Str |

### f5.profile.udp.generation

The config generation of a UDP Profile

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.udp.name | The name of a udp profile | Any Str |

### f5.profile.udp.info

The information about a UDP Profile

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.udp.name | The name of a udp profile | Any Str |
| f5.defaults_from.name | Name of the object from which default settings are inherited | Any Str |
| f5.profile.udp.datagram_load_balancing_enabled | Indicates if datagram load balancing is enabled on the profile | Any Str |
| f5.profile.udp.idle_timeout | Indicates the idle timeout on the udp profile | Any Str |
| f5.profile.udp.perform_checksum | Indicates if checksum is performed on the profile | Any Str |
| f5.profile.udp.buffer_max_bytes | The maximum buffer size for the udp profile | Any Int |
| f5.profile.udp.send_buffer_size | The send buffer size for the udp profile | Any Int |

### f5.profile.udp.open

The number of open UDP connections

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {connections} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.udp.name | The name of a udp profile | Any Str |

### f5.profile.udp.rx_badsums

The number of received datagrams with bad checksums

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {datagrams} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.udp.name | The name of a udp profile | Any Str |

### f5.profile.udp.rx_unreachables

The number of received datagrams that were unreachable

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {datagrams} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.udp.name | The name of a udp profile | Any Str |

### f5.profile.udp.tx_dgrams

The number of transmitted datagrams

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {datagrams} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.udp.name | The name of a udp profile | Any Str |

### f5.profile.web_acceleration.cache.count

The number of cache entries

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {entries} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.web_acceleration.name | The name of a web acceleration profile | Any Str |

### f5.profile.web_acceleration.cache.hits

the total count of cache hits

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {requests} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.web_acceleration.name | The name of a web acceleration profile | Any Str |

### f5.profile.web_acceleration.cache.hits.bytes

The total bytes of cache hits

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| By | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.web_acceleration.name | The name of a web acceleration profile | Any Str |

### f5.profile.web_acceleration.cache.misses

The total count of cache misses

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {requests} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.web_acceleration.name | The name of a web acceleration profile | Any Str |

### f5.profile.web_acceleration.cache.misses.bytes

The total bytes of cache misses

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| By | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.web_acceleration.name | The name of a web acceleration profile | Any Str |

### f5.profile.web_acceleration.generation

The config generation of an web acceleration Profile

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.web_acceleration.name | The name of a web acceleration profile | Any Str |

### f5.profile.web_acceleration.info

The information about an web accelration Profile

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.web_acceleration.name | The name of a web acceleration profile | Any Str |
| f5.defaults_from.name | Name of the object from which default settings are inherited | Any Str |
| f5.profile.web_acceleration.cache.size | The cache size (in MB) for the web acceleration profile | Any Int |
| f5.profile.web_acceleration.cache.max_age | The max age (in seconds) for the web acceleration profile | Any Int |
| f5.profile.web_acceleration.cache.max_entries | The max entries for the web acceleration profile | Any Int |

### f5.profile.web_acceleration.remote.hits

The total count of remote cache hits

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {requests} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.web_acceleration.name | The name of a web acceleration profile | Any Str |

### f5.profile.web_acceleration.remote.hits.bytes

The total bytes of remote cache hits

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| By | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.web_acceleration.name | The name of a web acceleration profile | Any Str |

### f5.profile.web_acceleration.remote.misses

The total count of remote cache misses

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {requests} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.profile.web_acceleration.name | The name of a web acceleration profile | Any Str |

### f5.rule.aborts

The number of times this iRule was aborted when using the tagged event trigger

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {executions} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.rule.name | The name of a rule | Any Str |
| f5.rule.event_type | The rule event type associated for the metric | Any Str |

### f5.rule.average_cycles

The average cycle count for this iRule when invoked when using the tagged trigger event

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {cycles} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.rule.name | The name of a rule | Any Str |
| f5.rule.event_type | The rule event type associated for the metric | Any Str |

### f5.rule.executions

The number of times this iRule  was executed using the tagged event trigger

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {executions} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.rule.name | The name of a rule | Any Str |
| f5.rule.event_type | The rule event type associated for the metric | Any Str |

### f5.rule.failures

The number of times this iRule failed when using the tagged event trigger

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {executions} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.rule.name | The name of a rule | Any Str |
| f5.rule.event_type | The rule event type associated for the metric | Any Str |

### f5.rule.max_cycles

The maximum cycle count for this iRule when invoked when using the tagged trigger event

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {cycles} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.rule.name | The name of a rule | Any Str |
| f5.rule.event_type | The rule event type associated for the metric | Any Str |

### f5.rule.min_cycles

The minimum cycle count for this iRule when invoked when using the tagged trigger event

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {cycles} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.rule.name | The name of a rule | Any Str |
| f5.rule.event_type | The rule event type associated for the metric | Any Str |

### f5.ssl_certificate.expires_at

The expiration time of the SSL Cert or Bundle

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {epoch_second} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.ssl_certificate.name | The Full path name of the SSL cert or bundle | Any Str |
| is_bundle | Denotes whether the certificate file is a bundle | Str: ``true``, ``false`` |
| key_type | The certificate key type | Any Str |

### f5.system.cpu.io_wait

The io_wait utilization of the identified CPU over the last 5 seconds.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| 1 | Gauge | Double |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| cpu.id | The Integer ID of the CPU. | Any Int |
| slot.id | The chassis slot on the device | Any Int |

### f5.system.cpu.niced

The niced utilization of the identified CPU over the last 5 seconds.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| 1 | Gauge | Double |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| cpu.id | The Integer ID of the CPU. | Any Int |
| slot.id | The chassis slot on the device | Any Int |

### f5.system.cpu.system

The system utilization of the identified CPU over the last 5 seconds.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| 1 | Gauge | Double |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| cpu.id | The Integer ID of the CPU. | Any Int |
| slot.id | The chassis slot on the device | Any Int |

### f5.system.cpu.utilization

The utilization of the identified CPU over the last 5 seconds.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| 1 | Gauge | Double |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| cpu.id | The Integer ID of the CPU. | Any Int |
| slot.id | The chassis slot on the device | Any Int |

### f5.system.cpu.utilization.user

The user utilization of the identified CPU over the last 5 seconds.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| 1 | Gauge | Double |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| cpu.id | The Integer ID of the CPU. | Any Int |
| slot.id | The chassis slot on the device | Any Int |

### f5.system.failover.active_state

The failover state of the system.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| 1 | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |

### f5.system.failover.peer.active_state

The failover state of the peer system.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| 1 | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| failover.peer_name | The failover peer device name. | Any Str |

### f5.system.info

Asset information about the system

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.system.partition | The partition for the resource | Any Str |
| f5.system.baseMac | The base mac address for the device | Any Str |
| f5.system.chassisType | The base mac address for the device | Any Str |
| f5.system.marketing_name | The marketing name for the resource | Any Str |
| f5.instance.management_ip | The configured management IP for the device | Any Str |
| failover_state | The failover status. | Str: ``active``, ``inactive`` |
| system.id | Unique ID for the system | Any Str |
| system.name | The system Configured name | Any Str |
| system.product.name | The product type of the system | Any Str |
| system.version | The software version of the system | Any Str |

### f5.system.logical_disk.application.used

The application used of a logical disk

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| By | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.system.logical_disk.name | The name of a logical disk | Any Str |
| f5.system.logical_disk.application.name | The owner of the application partition | Any Str |

### f5.system.logical_disk.limit

The limit of a logical disk

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| By | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| disk.mode | The disk mode | Any Str |
| f5.system.logical_disk.name | The name of a logical disk | Any Str |

### f5.system.logical_disk.usage

The usage of a logical disk

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| By | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| state | The disk usage state. | Str: ``used``, ``free``, ``reserved`` |
| disk.mode | The disk mode | Any Str |
| f5.system.logical_disk.name | The name of a logical disk | Any Str |

### f5.system.memory.other.total

The total other system memory

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| By | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |

### f5.system.memory.other.used

The current other system memory used/free

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| By | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| state | The memory usage state. | Str: ``used``, ``free`` |

### f5.system.memory.swap.total

The total swap system memory

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| By | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |

### f5.system.memory.swap.used

The current swap system memory used/free

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| By | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| state | The memory usage state. | Str: ``used``, ``free`` |

### f5.system.memory.tmm.total

The total TMM system memory

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| By | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |

### f5.system.memory.tmm.used

The current TMM system memory used/free

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| By | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| state | The memory usage state. | Str: ``used``, ``free`` |

### f5.system.memory.total

The total system memory

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| By | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |

### f5.system.memory.used

The current system memory used/free

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| By | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| state | The memory usage state. | Str: ``used``, ``free`` |

### f5.system.process.cpu.top_10

The utilization of the top 10 processes by CPU (descending)

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| 1 | Gauge | Double |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| process.name | The name of a process. | Any Str |

### f5.system.process.memory.top_10

The memory utilzation of the top 10 processes by Memory Use (descending)

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| By | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| process.name | The name of a process. | Any Str |

### f5.system.state.up

Boolean value indicating whether the system is reachable

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| 1 | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |

### f5.system.subsystem.cpu.utilization

The CPU utilization for the given sub-system.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| 1 | Gauge | Double |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.subsystem.name | The name of a subsystem of the parent system | Any Str |

### f5.system.subsystem.memory_resident.used

The current resident memory usage for the given sub-system

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| By | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.subsystem.name | The name of a subsystem of the parent system | Any Str |

### f5.system.subsystem.memory_virtual.used

The current virtual memory usage for the given sub-system

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| By | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.subsystem.name | The name of a subsystem of the parent system | Any Str |

### f5.virtual_server.asm_cpu.utilization

CPU use by the ASM module for for this Virtual Server over the past 5 seconds

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| percent | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |

### f5.virtual_server.availability

Availability of the virtual server.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| 1 | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |
| availability.state | The availability state. | Str: ``offline``, ``unknown``, ``available`` |

### f5.virtual_server.clientside.bytes_in

Amount of data received by the virtual server.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| By | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |

### f5.virtual_server.clientside.bytes_out

Amount of data transmitted from the virtual server.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| By | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |

### f5.virtual_server.clientside.connection

Total number of clientside connections to the virtual server.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {connection} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |

### f5.virtual_server.clientside.connection.count

Current number of connections to the virtual server.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {connection} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |

### f5.virtual_server.clientside.connection.duration_mean

Average clientside connection duration for the lifetime of the VS

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| ms | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |

### f5.virtual_server.clientside.connection.evicted

Total number of evicted Clientside connections to the virtual server.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {connection} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |

### f5.virtual_server.clientside.connection.slow_killed

Total number of slow killed clientside connections to the virtual server.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {connection} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |

### f5.virtual_server.configured_object.count

The count of all configured rules, profiles, and policies on the virtual server.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {objects} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |

### f5.virtual_server.cpu.utilization

CPU Utilization for this Virtual server over the past 5 seconds.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| 5s | Gauge | Double |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |

### f5.virtual_server.enabled

Enabled state of of the virtual server.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| 1 | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |

### f5.virtual_server.ephemeral.connection

Total number of ephemeral connections to the virtual server.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {connection} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |

### f5.virtual_server.generation

Config Generation for this virtualserver.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {generation} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |

### f5.virtual_server.info

Config info for this virtualserver.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |
| f5.virtual_server.destination | The destination for the Virtual Server. | Any Str |
| f5.virtual_server.protocol | The protocol for a Virtual Server. | Any Str |
| f5.pool.name | The name of a Pool. | Any Str |

### f5.virtual_server.packets_in

Number of packets transmitted to and from the virtual server.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {packet} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |

### f5.virtual_server.packets_out

Number of packets transmitted to and from the virtual server.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {packet} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |

### f5.virtual_server.policy.firewall.rule_hits

The number of hits for a rule in the firewall policy

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {hits} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.policy.firewall.name | The name of the firewall policy. | Any Str |
| f5.policy.firewall.mode | The mode of the firewall policy | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |

### f5.virtual_server.profile.client_ssl.bytes_in

The total bytes in by encryption status

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| By | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |
| f5.profile.client_ssl.name | The name of an SSL Profile | Any Str |
| encryption.state | The type of traffic encrypted/decrypted. | Str: ``encrypted``, ``decrypted`` |

### f5.virtual_server.profile.client_ssl.bytes_out

The total bytes out by encryption status

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| By | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |
| f5.profile.client_ssl.name | The name of an SSL Profile | Any Str |
| encryption.state | The type of traffic encrypted/decrypted. | Str: ``encrypted``, ``decrypted`` |

### f5.virtual_server.profile.client_ssl.connection

The SSL Client connections total value

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {connection} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |
| f5.profile.client_ssl.name | The name of an SSL Profile | Any Str |

### f5.virtual_server.profile.client_ssl.connection.count

The SSL Client connections current value

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {connection} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |
| f5.profile.client_ssl.name | The name of an SSL Profile | Any Str |

### f5.virtual_server.profile.client_ssl.connection.max

The SSL Client connections maximum value

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {connection} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |
| f5.profile.client_ssl.name | The name of an SSL Profile | Any Str |

### f5.virtual_server.profile.client_ssl.handshake.count

The current number of handshakes.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {handshake} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |
| f5.profile.client_ssl.name | The name of an SSL Profile | Any Str |

### f5.virtual_server.profile.client_ssl.insecure_handshake_accepts

The total insecure handshakes accepted.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {handshake} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |
| f5.profile.client_ssl.name | The name of an SSL Profile | Any Str |

### f5.virtual_server.profile.client_ssl.insecure_handshake_rejects

The total insecure handshakes rejected.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {handshake} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |
| f5.profile.client_ssl.name | The name of an SSL Profile | Any Str |

### f5.virtual_server.profile.client_ssl.premature_disconnects

The total number of premature disconnects.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {connections} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |
| f5.profile.client_ssl.name | The name of an SSL Profile | Any Str |

### f5.virtual_server.profile.client_ssl.records_in

The total records into the SSL profile for this VS.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {record} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |
| f5.profile.client_ssl.name | The name of an SSL Profile | Any Str |

### f5.virtual_server.profile.client_ssl.records_out

The total records out of the SSL profile for this VS.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {record} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |
| f5.profile.client_ssl.name | The name of an SSL Profile | Any Str |

### f5.virtual_server.profile.client_ssl.renegotiations

The total midstream renegotiations.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {negotiation} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |
| f5.profile.client_ssl.name | The name of an SSL Profile | Any Str |

### f5.virtual_server.profile.client_ssl.secure_handshakes

The total secure handshakes processed.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {handshake} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |
| f5.profile.client_ssl.name | The name of an SSL Profile | Any Str |

### f5.virtual_server.profile.generation

Config Generation of the BIG-IP profile for this virtualserver.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {generation} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |
| f5.profile.name | The name of a profile of potentially many types | Any Str |

### f5.virtual_server.profile.http.requests.by_method

The number of client-side requests with the specified method.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {request} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |
| f5.profile.http.name | The name of an HTTP Profile | Any Str |
| http.method | The HTTP request method. | Str: ``GET``, ``HEAD``, ``POST``, ``PUT``, ``DELETE``, ``TRACE``, ``OPTIONS``, ``PATCH`` |

### f5.virtual_server.profile.http.responses.by_status

The number of server-side responses in the specified range.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {response} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |
| f5.profile.http.name | The name of an HTTP Profile | Any Str |
| http.status_range | The HTTP Status code range in blocks of 100. | Str: ``1xx``, ``2xx``, ``3xx``, ``4xx``, ``5xx`` |

### f5.virtual_server.profile.info

Info about a BIG-IP profile for this virtualserver.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| {info} | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |
| f5.profile.name | The name of a profile of potentially many types | Any Str |
| f5.profile.family | The family (ltm, apm, net, security) of a profile. | Any Str |
| f5.profile.type | The type of a profile of potentially many types | Any Str |

### f5.virtual_server.requests

Number of requests to the virtual server.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {request} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |

### f5.virtual_server.rule.enabled

Indicates that the specified iRule is enabled for the VS.

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| 1 | Gauge | Int |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |
| f5.rule.name | The name of a rule | Any Str |

### f5.virtual_server.syncookie.accepts

Number of syncookie accepts by the virtual server.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {accept} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |

### f5.virtual_server.syncookie.rejects

Number of syncookie rejects by the virtual server.

| Unit | Metric Type | Value Type | Aggregation Temporality | Monotonic |
| ---- | ----------- | ---------- | ----------------------- | --------- |
| {reject} | Sum | Int | Cumulative | true |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |
| f5.virtual_server.name | The name of a Virtual Server. | Any Str |

### scrape.duration

The total time spend scraping data from the target device

| Unit | Metric Type | Value Type |
| ---- | ----------- | ---------- |
| s | Gauge | Double |

#### Attributes

| Name | Description | Values |
| ---- | ----------- | ------ |
| dataType | The data type which signifies the schema for the metric | Any Str |

## Resource Attributes

| Name | Description | Values | Enabled |
| ---- | ----------- | ------ | ------- |
| f5.data_type | The type of data associated with the group of metrics | Any Str | true |
| f5.instance.name | The system Configured name | Any Str | true |
| f5.product.name | The product type of the system | Any Str | true |
| f5.product.version | The software version of the system | Any Str | true |
| f5.system.id | The unique ID for the system | Any Str | true |
| server.address | The <host> portion of the target’s URL that was scraped | Any Str | true |
| server.port | The <port> portion of the target’s URL that was scraped | Any Str | true |
| service.instance.id | The service instance id (default configured host:port of configured endpoint) | Any Str | true |
| service.name | The receiver service name (default f5.instance.name) | Any Str | true |
| service.namespace | The receiver service type (default 'bigip') | Any Str | true |
| url.scheme | The <port> portion of the target’s URL that was scraped | Str: ``http``, ``https`` | true |
