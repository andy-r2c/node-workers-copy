# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [2.4.0] - 2021-12-03

### Added

- new options `resourceLimits`, See [Node.js new Worker options](https://nodejs.org/api/worker_threads.html#worker_threads_new_worker_filename_options)

## [2.3.1] - 2021-05-05

### Changed

- replaced inspector module usage in favor of native worker `getHeapSnapshot()` method
- node 15/16 supported

## [2.3.0] - 2020-11-24

### Added

- new options `asyncWorkerInitialization` that enable async initialization of worker

## [2.2.1] - 2020-09-17

### Changed

- Bump lodash from 4.17.15 to 4.17.19

## [2.2.0] - 2020-09-17

### Added

- new method: `workerNodes.getUsedWorkers` that return list with used workers in pool

## [2.1.0] - 2020-07-07

### Added

- add new method: `workerNodes.profiler` for CPU Profiling
- add new method: `workerNodes.takeSnapshot` for memory Heap Snapshot

## [2.0.0] - 2020-07-02

### Breaking

- drop support for deprecated Node versions

### Added

- eslint configuration

### Changed

- use experimental worker_threads to run tasks (@slonka)
- drop -alpha.x as worker_threads are exposed by default (since node.js 11.7.0) and some issues with inspecting them were resolved (since 11.10.0)
- test runner changed to [AVA](https://github.com/avajs/ava)
- dependencies update
- CI / Publish by github actions

## 1.6.1 - 2018-06-20

### Changed

- support for `--inspect-brk` flag added (@lev-kazakov)

## 1.6.0 - 2017-09-12

### Changed

- message-pack streaming disabled
- typescript definitions added (@MariusAlch)
- readme typo fixes (@crcastle)

## [1.5.0] - 2017-06-22

### Added

- message-pack streaming (@noam-almog)

## [1.4.0] - 2017-05-29

### Changed

- bson serializer replaced with message-pack (@noam-almog)

## [1.3.1] - 2017-02-05

### Fixed

- Minor performance fix: getting rid of array destructuring as it prevents code runtime optimization in current v8

## [1.3.0] - 2017-01-23

### Changed

- Workers do not accept work when they are in process of booting up (@mheiniger)

## [1.2.1] - 2016-12-19

### Changed

- Dependencies update

## 1.2.0 - 2016-11-08

### Changed

- Moved away from sending data through `'ipc'` channel in favour of a specialized `'pipe'`.

### Removed

- `<code>useCompression</code>` option (because it seems pointless when a new transfer format is in use).

## 1.1.0 - 2016-11-02

### Added

- `<code>useCompression</code>` option

## 1.0.0 - 2016-11-01

Initial release

[2.4.0]: https://github.com/allegro/node-worker-nodes/releases/tag/v2.4.0
[2.3.1]: https://github.com/allegro/node-worker-nodes/releases/tag/v2.3.1
[2.3.0]: https://github.com/allegro/node-worker-nodes/releases/tag/v2.3.0
[2.2.1]: https://github.com/allegro/node-worker-nodes/releases/tag/v2.2.1
[2.2.0]: https://github.com/allegro/node-worker-nodes/releases/tag/v2.2.0
[2.1.0]: https://github.com/allegro/node-worker-nodes/releases/tag/v2.1.0
[2.0.0]: https://github.com/allegro/node-worker-nodes/releases/tag/v2.0.0
[1.5.0]: https://github.com/allegro/node-worker-nodes/releases/tag/v1.5.0
[1.4.0]: https://github.com/allegro/node-worker-nodes/releases/tag/v1.4.0
[1.3.1]: https://github.com/allegro/node-worker-nodes/releases/tag/v1.3.1
[1.3.0]: https://github.com/allegro/node-worker-nodes/releases/tag/v1.3.0
[1.2.1]: https://github.com/allegro/node-worker-nodes/releases/tag/v1.2.1
