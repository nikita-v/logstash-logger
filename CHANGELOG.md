## 0.10.3
- Merge URI and non-URI configuration. [#54](https://github.com/dwbutler/logstash-logger/pull/54) 

## 0.10.2
- Fix for Custom Events can't access tags from Tagged Logging. [#48](https://github.com/dwbutler/logstash-logger/issues/48)

## 0.10.1
- Fix for Redis URI parsing issue. [#41](https://github.com/dwbutler/logstash-logger/issues/41)

## 0.10.0
- Support for logging to Kafka. [#37](https://github.com/dwbutler/logstash-logger/issues/37)

## 0.9.0
- Support for customizing the fields on all logged messages via configuration. [#32](https://github.com/dwbutler/logstash-logger/pull/32)

## 0.8.0
- Support for logging to stderr. [#24](https://github.com/dwbutler/logstash-logger/pull/25)
- Support multiple log outputs. [#28](https://github.com/dwbutler/logstash-logger/pull/28)

## 0.7.0
- Support for logging to a generic IO object.
- Support for overriding IO in stdout logger. [#20](https://github.com/dwbutler/logstash-logger/pull/20)
- Support for configuring logger with a URI. [#22](https://github.com/dwbutler/logstash-logger/pull/22)
- Support logging any object. [#23](https://github.com/dwbutler/logstash-logger/issues/23)

## 0.6.2
- Allow type to be specified as a string. [#19](https://github.com/dwbutler/logstash-logger/pull/19)

## 0.6.1
- Don't mutate options passed to LogStashLogger. [#18](https://github.com/dwbutler/logstash-logger/pull/18)

## 0.6.0
- Support for logging to a file.
- Support for logging to a Redis list.
- Support for logging to a local Unix socket.
- Railtie supports file logger, using default log path and `config.autoflush_log` configuration.
- All `LogStashLogger` types now support a `sync` option, which controls if each message is automatically flushed.

## 0.5.0
- Support for tagged logging. The interface was extracted from `ActiveSupport::TaggedLogging`
and outputs to the `tags` key.
- The `(host, port, type)` constructor has been deprecated in favor of an options hash constructor.
- Support for using SSL for TCP connections.
- Support for configuring logger to write to STDOUT.
- Support for Rails configuration.
- Fixed output to STDOUT in Rails console (Rails 4+).
- `host` is no longer required for TCP/UDP. It will default to `0.0.0.0`, the same default port that logstash listens on.
- Changed event key `source` to `host` to match what the latest logstash expects.
- Output event timestamp consistently even if `Time#to_json` is overridden.
- Major refactoring which will lead the way to support other log types.

## 0.4.1
- Fixed support for `LogStash::Event` v1 format when logging a hash. Extra data
now goes to the top level instead of into the `@fields` key.

## 0.4.0
- Support for new `LogStash::Event` v1 format. v0 is supported in 0.3+.

## 0.3.0
- Added support for logging to a UDP listener.

## 0.2.1
- Fixed to use Logstash's default time format for timestamps.

## 0.2.0
- Better use of Ruby Logger's built-in LogDevice.

## 0.1.0
- Initial release. Support for logging to a TCP listener.
