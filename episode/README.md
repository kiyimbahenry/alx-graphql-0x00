# GraphQL Character Queries

This repository contains GraphQL queries to fetch character information by ID from a GraphQL API.

## Project Structure
character/
├── README.md
├── character-id-1.graphql
├── character-id-1.output.json
├── character-id-2.graphql
├── character-id-2.output.json
├── character-id-3.graphql
├── character-id-3.output.json
├── character-id-4.graphql
└── character-id-4.output.json


## Files Description

- **`character-id-{1-4}.graphql`**: GraphQL query files for fetching character details with IDs 1 through 4
- **`character-id-{1-4}.output.json`**: JSON responses from executing the corresponding GraphQL queries

## GraphQL Queries

Each query file follows the same structure:

```graphql
{
  character(id: [ID]) {
    id
    name
    status
    species
    type
    gender
  }
}

Fields Requested
All queries request the following character fields:

id: Character's unique identifier

name: Character's name

status: Character's status (Alive, Dead, unknown)

species: Character's species

type: Character's type/subspecies

gender: Character's gender

How to Execute Queries
Using GraphQL Playground:
Open the GraphQL Playground interface

Paste the query from any .graphql file into the left panel

Click the "Play" button (▶️) to execute

View the JSON response in the right panel

Endpoint
All queries are executed against the GraphQL endpoint provided in the learning platform.

Learning Objectives
Write GraphQL queries to fetch specific data

Understand GraphQL query structure and syntax

Retrieve specific character information using ID parameters

Work with GraphQL response formats

# Paginated Characters Queries

This directory contains GraphQL queries for retrieving paginated lists of characters.

## Files

- `characters-page-1.graphql` - Query for page 1 characters
- `characters-page-1-output.json` - JSON response for page 1
- `characters-page-2.graphql` - Query for page 2 characters
- `characters-page-2-output.json` - JSON response for page 2
- `characters-page-3.graphql` - Query for page 3 characters
- `characters-page-3-output.json` - JSON response for page 3
- `characters-page-4.graphql` - Query for page 4 characters
- `characters-page-4-output.json` - JSON response for page 4

## Query Structure

Each query follows this pattern:

```graphql
query {
  characters(page: [PAGE_NUMBER]) {
    results {
      id
      name
      status
      image
    }
  }
}

Fields Requested
For each character in the results:

id: Unique identifier

name: Character's name

status: Character's status (Alive, Dead, or unknown)

image: URL to the character's image

Pagination
Uses the characters(page: Int) field with page numbers 1 through 4

Each page typically contains 20 characters (depends on API configuration)

Pagination allows retrieving manageable chunks of data
