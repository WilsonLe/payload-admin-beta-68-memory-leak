# Testing different versions of payload beta

- beta 68: `pnpm payload migrate:create` works great.
- beta 69: `pnpm payload migrate:create` fails. This error is fixed in beta 70.
- beta 70: `pnpm payload migrate:create` works great.
- beta 71: `pnpm payload migrate:create` works great.
- beta 72: `pnpm payload migrate:create` fails with the following error:

```sh
file:///~/Code/payload-reproduce/node_modules/.pnpm/payload@3.0.0-beta.72_@swc+core@1.7.5_@swc+helpers@0.5.11__@swc+types@0.1.12_graphql@16.8.1_typescript@5.5.4/node_modules/payload/dist/bin/migrate.js:75
                throw new Error(`Error creating migration: ${err.message}`);
                      ^

Error: Error creating migration: [
  {
    "received": "5",
    "code": "invalid_literal",
    "expected": "7",
    "path": [
      "version"
    ],
    "message": "Invalid literal value, expected \"7\""
  },
  {
    "received": "pg",
    "code": "invalid_literal",
    "expected": "postgresql",
    "path": [
      "dialect"
    ],
    "message": "Invalid literal value, expected \"postgresql\""
  },
  {
    "code": "invalid_type",
    "expected": "object",
    "received": "string",
    "path": [
      "tables",
      "users",
      "indexes",
      "users_created_at_idx",
      "columns",
      0
    ],
    "message": "Expected object, received string"
  },
  {
    "code": "invalid_type",
    "expected": "object",
    "received": "string",
    "path": [
      "tables",
      "users",
      "indexes",
      "users_email_idx",
      "columns",
      0
    ],
    "message": "Expected object, received string"
  },
  {
    "code": "invalid_type",
    "expected": "object",
    "received": "string",
    "path": [
      "tables",
      "media",
      "indexes",
      "media_created_at_idx",
      "columns",
      0
    ],
    "message": "Expected object, received string"
  },
  {
    "code": "invalid_type",
    "expected": "object",
    "received": "string",
    "path": [
      "tables",
      "media",
      "indexes",
      "media_filename_idx",
      "columns",
      0
    ],
    "message": "Expected object, received string"
  },
  {
    "code": "invalid_type",
    "expected": "object",
    "received": "string",
    "path": [
      "tables",
      "payload_preferences",
      "indexes",
      "payload_preferences_key_idx",
      "columns",
      0
    ],
    "message": "Expected object, received string"
  },
  {
    "code": "invalid_type",
    "expected": "object",
    "received": "string",
    "path": [
      "tables",
      "payload_preferences",
      "indexes",
      "payload_preferences_created_at_idx",
      "columns",
      0
    ],
    "message": "Expected object, received string"
  },
  {
    "code": "invalid_type",
    "expected": "object",
    "received": "string",
    "path": [
      "tables",
      "payload_preferences_rels",
      "indexes",
      "payload_preferences_rels_order_idx",
      "columns",
      0
    ],
    "message": "Expected object, received string"
  },
  {
    "code": "invalid_type",
    "expected": "object",
    "received": "string",
    "path": [
      "tables",
      "payload_preferences_rels",
      "indexes",
      "payload_preferences_rels_parent_idx",
      "columns",
      0
    ],
    "message": "Expected object, received string"
  },
  {
    "code": "invalid_type",
    "expected": "object",
    "received": "string",
    "path": [
      "tables",
      "payload_preferences_rels",
      "indexes",
      "payload_preferences_rels_path_idx",
      "columns",
      0
    ],
    "message": "Expected object, received string"
  },
  {
    "code": "invalid_type",
    "expected": "object",
    "received": "string",
    "path": [
      "tables",
      "payload_migrations",
      "indexes",
      "payload_migrations_created_at_idx",
      "columns",
      0
    ],
    "message": "Expected object, received string"
  }
]
    at migrate (file:///~/Code/payload-reproduce/node_modules/.pnpm/payload@3.0.0-beta.72_@swc+core@1.7.5_@swc+helpers@0.5.11__@swc+types@0.1.12_graphql@16.8.1_typescript@5.5.4/node_modules/payload/dist/bin/migrate.js:75:23)
    at process.processTicksAndRejections (node:internal/process/task_queues:95:5)

Node.js v20.15.1
```