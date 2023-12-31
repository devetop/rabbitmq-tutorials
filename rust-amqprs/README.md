# Rust code for RabbitMQ tutorials (using amqprs)

Here you can find the Rust code examples for [RabbitMQ
tutorials](https://www.rabbitmq.com/getstarted.html).

The examples use [amqprs](https://github.com/gftea/amqprs) client library.

These tutorials assume a RabbitMQ server node running locally using default ports.

## Requirements

* [Rust and Cargo](https://www.rust-lang.org/tools/install)

## Code
Each cargo command should be launched in a separate shell.

#### [Tutorial one: "Hello World!"](https://www.rabbitmq.com/tutorials/tutorial-one-python.html)

    cargo run --bin receive
    cargo run --bin send

#### [Tutorial two: Work Queues](https://www.rabbitmq.com/tutorials/tutorial-two-python.html)

    cargo run --bin worker
    cargo run --bin new_task "hi" # specify a custom message

#### [Tutorial three: Publish/Subscribe](https://www.rabbitmq.com/tutorials/tutorial-three-python.html)

    cargo run --bin receive_logs
    cargo run --bin emit_log "hi" # specify a custom message

#### [Tutorial four: Routing](https://www.rabbitmq.com/tutorials/tutorial-four-python.html)

    cargo run --bin receive_logs_direct info error # specify log levels
    cargo run --bin emit_log_direct error "help!" # specify severity and custom message

#### [Tutorial five: Topics](https://www.rabbitmq.com/tutorials/tutorial-five-python.html)

    cargo run --bin receive_logs_topic kern.* # specify topic filter
    cargo run --bin emit_log_topic kern.mem "No memory left!" # specify topic and message
