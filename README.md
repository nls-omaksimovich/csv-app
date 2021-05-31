# csv-app

Kotlin multi-module app with Gradle's Kotlin DSL and Spring Boot

1. [api](./api) app interfaces
2. [backend](./backend) service layer implementation
3. [cli](./cli) user's command line interface
4. [common](./common) contains models, mappers and utility classes

* [db/observation.mwb](./db/observation.mwb) - database schema design to store data from CSV
* [db/migration](./db/migration) - stores migration `.sql` files with the next pattern:

```
<Prefix><Version>__<Description>.sql
```

Example: `V1_0__create_observation_table.sql`

# Build

Run a clean build of the project with the following

```
./gradlew clean build
```

# Run migration

Run from parent project folder

```
./gradlew flywayMigrate
```
