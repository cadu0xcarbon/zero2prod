# Zero To Production In Rust

## Requirements

- docker
- rust

## Running locally

To initialize database locally:

```bash
./scripts/init_db.sh
```

To build the project:

```bash
cargo build
```

To run the project:

```bash
cargo run
```

<http://127.0.0.1:8000> should be up and running

## Notes

When you want to see all logs coming out of a certain test case to debug it you can run:

```bash
TEST_LOG=true cargo test health_check_works | bunyan
```

To generate a new migration script:

```bash
sqlx migrate add create_subscription_tokens_table
```

To run docker zero2prod build:

```bash
docker build --tag zero2prod --file Dockerfile .
```

To run the container:

```bash
docker run -p 8000:8000 zero2prod
```

To run migrations locally:

```bash
SKIP_DOCKER=true ./scripts/init_db.sh
```

To scan for unused crates in Cargo:

```bash
cargo +nightly udeps
```
