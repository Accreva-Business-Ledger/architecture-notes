# Service boundaries

## Web application

The web application presents workflows and sends authenticated requests to the API. It holds no database credentials and performs no direct database writes.

## API

The API owns application rules and database access. Routers handle transport concerns. Services enforce domain rules. Repositories perform scoped ORM queries.

## Agent tooling

Agent components route user requests through defined tools and application services. They do not receive database credentials. A confirmation step protects actions that change financial records.

## Database

The database stores tenant-scoped application records and audit history. Application code uses ORM queries and validates tenant ownership before mutations.
