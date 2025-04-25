# docs: enhance database operation examples (fixes #12216)

## Overview
This PR enhances the database operations documentation with practical examples to address issue #12216, where users are having difficulty with database access in Medusa v2 (particularly when trying to use old v1 import paths like `@medusajs/medusa/loaders/database`).

## Changes
I've enhanced the existing documentation at `/learn/fundamentals/modules/db-operations/page.mdx` with:

1. Practical examples of common repository operations using realistic e-commerce product data
2. Custom repository methods examples with specialized queries 
3. A comprehensive transaction example showing multiple operations in one transaction
4. Advanced SQL query examples for e-commerce reporting needs

These enhancements make the documentation more applicable to real-world scenarios and should help developers better understand how to properly access the database in Medusa v2.

Fixes #12216 