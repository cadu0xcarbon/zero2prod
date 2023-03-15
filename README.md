TODO

### See all logs

When you want to see all logs coming out of a certain test case to debug it you can run:
$ TEST_LOG=true cargo test health_check_works | bunyan

### Generate new migration script

sqlx migrate add create_subscription_tokens_table

### Run docker zero2prod

$ docker build --tag zero2prod --file Dockerfile .
$ docker run -p 8000:8000 zero2prod

### Initialize database locally

```
./scripts/init_db.sh
```

### Run migrations locally

```
SKIP_DOCKER=true ./scripts/init_db.sh
```

### TODO add lib to scan for unused crates in Cargo.toml
