# Full-stack real-time chat

- **Data:** PostgeSQL managed by [Supabase](https://supabase.io/) [@supabase_io](https://twitter.com/supabase_io) (awsome real-time API).
- **Front-end**: React + Vite
- **UI library**: [chakra-ui](https://chakra-ui.com/) [@chakra_ui](https://twitter.com/chakra_ui)
- **Hosting**: [Netlify](https://www.netlify.com/)
- Country flags from [Flagpedia](https://flagpedia.net)

## Install

`npm install` to setup dependencies

## Supabase variables

Create a `.env` file with `VITE_SUPABASE_URL` and `VITE_SUPABASE_KEY` (see env.example)

## Setup your Supabase project

The following database table is required:

| Field    | Type    |
| -------- | ------- |
| id       | BIGINT  |
| username | VARCHAR |
| country  | VARCHAR |
| text     | TEXT    |

SQL query if not using the Supabase interface:

```sql
CREATE TABLE messages (
  id bigint GENERATED BY DEFAULT AS IDENTITY PRIMARY KEY,
  username VARCHAR NOT NULL,
  country VARCHAR,
  text TEXT NOT NULL
);
```

## Dev

`npm run dev` to run server on port 3000

## Build

`npm run build` to build the react client

# Example

!['example'](https://i.ibb.co/2d7Pzyb/random-chat.png "example")
