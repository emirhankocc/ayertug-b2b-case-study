# System Architecture

## Application Structure

The project uses a monorepo structure with separate applications for the corporate website and dealer portal.

apps/
├── web/
├── bayi-web/
└── api/

Request Flow:

The user interacts with the Next.js frontend.
The frontend communicates with the NestJS API.
The API validates authentication and role permissions.
Prisma performs database operations.
Files and product assets are stored in Cloudflare R2.
Exchange-rate data is retrieved from an external service.

Authentication Flow:

Short-lived access tokens
Refresh-token flow
Backend role guards
Dealer-level data isolation
Main Roles:

Dealer;

Browse products
Create orders
Track account balance
View assigned salesperson
Salesperson;

Manage assigned dealers
Create orders for dealers
Record collections
Update delivery information
Administrator;

Manage users and products
Approve dealer applications
Manage orders and limits
Access reporting interfaces

Data Isolation:

Dealer users can only access data belonging to their own dealer account. Authorization checks are applied at the service and database-query level.
