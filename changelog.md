# Changelog

<a name="master"></a>
## Master

<a name="0.11.1"></a>
## 0.11.0 (2017-06-25)

#### Features

* Support direct creation of OwnedMessages.

<a name="0.11.0"></a>
## 0.11.0 (2017-06-20)

#### Features

* The topic partition list object from librdkafka is now completely accessible
  from Rust.
* The test suite will now run both unit tests and integration tests in
  valgrind, and it will also check for memory leaks.
* rdkafka-sys will use the system librdkafka if it's already installed.
* rdkafka-sys will verify that the crate version corresponds to the librdkafka
  version during the build.
* Timestamp is now Copy.
* Message has been renamed to BorrowedMessage. Borrowed messages can be transformed
  into owned messages. Both implement the new Message trait.
* Improved error enumerations.

#### Bugs

* Fix memory access bug in statistics callback.
* Fix memory leak in topic partition list.
* Messages lifetime is now explicit (issue [#48](https://github.com/fede1024/rust-rdkafka/issues/48))

<a name="0.10.0"></a>
## 0.10.0 (2017-05-15)

#### Features

* Consumer commit callback
* Add configurable poll timeout
* Add special error code for message not received within poll time
* Add topic field for messages
* Make the topic partition list optional for consumer commit
* Add `store_offset` to consumer
* Add at-least-once delivery example

<a name="0.9.1"></a>
## 0.9.1 (2017-04-19)

#### Features

* OpenSSL dependency optional
* librdkafka 0.9.5

<a name="0.9.0"></a>
## 0.9.0 (2017-04-16)

#### Bugs

* Fix termination sequence

#### Features

* Integration tests running in docker and valgrind
* Producer topics are not needed anymore

<a name="0.8.1"></a>
## 0.8.1 (2017-03-21)

##### Bugs

* Implement Clone for `BaseProducerTopic`

#### Features

<a name="0.8.0"></a>
## 0.8.0 (2017-03-20)

#### Features

* Add timestamp support
* librdkafka 0.9.4
* Add client statistics callback and parsing

<a name="0.7.0"></a>
## 0.7.0 (2017-02-18)

#### Features

* Asynchronous message processing example based on tokio
* More metadata for consumers
* Watermark API
* First iteration of integration test suite
