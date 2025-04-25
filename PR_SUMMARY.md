# docs: enhance database operation examples (fixes #12216)

I've noticed that many developers have been facing challenges with database access in Medusa v2, particularly when attempting to use the import path `@medusajs/medusa/loaders/database` which was available in v1 but no longer exists in v2 (as referenced in issue #12216).

After receiving feedback on my previous PR (#12291), I understand that creating a new documentation page wasn't the optimal approach. Instead, I've focused on enhancing the existing documentation at `/learn/fundamentals/modules/db-operations/page.mdx` with more detailed and practical examples:

- Added realistic examples of common data model repository operations using e-commerce product data
- Included examples of custom repository methods with specialized queries for common use cases
- Created a more comprehensive transaction example demonstrating multiple operations within a single atomic transaction
- Provided advanced SQL query examples that showcase practical e-commerce database operations (product analytics, sales reporting)

These improvements should help both new and experienced developers better understand how to effectively work with MikroORM in Medusa v2, especially those transitioning from v1 who might be struggling with the architectural differences.

Thank you for considering this contribution. I appreciate the feedback on my previous PR that helped guide this improvement.

Fixes #12216 