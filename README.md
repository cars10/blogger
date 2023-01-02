# README

## Project Setup

1. Install dependencies

```
bundle install
yarn install
```

2. Create `config/database.yml`

```
default: &default
  adapter: sqlite3
  pool: <%= ENV.fetch("RAILS_MAX_THREADS") { 5 } %>
  timeout: 5000

development:
  <<: *default
  database: db/development.sqlite3

production:
  <<: *default
  database: db/production.sqlite3
```

3. Setup database `rails db:setup`
4. Open a terminal and run `yarn build --watch` to build javascript
5. Open a second terminal and run `yarn build:css --watch` to build css
6. Open a third terminal and run rails `rails s`
