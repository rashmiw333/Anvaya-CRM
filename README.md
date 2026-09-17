# Anvaya CRM

A full-stack Lead Management CRM application built to manage leads
through different stages of the sales lifecycle.

Built with React JS frontend, Node.js/Express backend, MongoDB
database, and Chart.js for reporting and data visualization.

------------------------------------------------------------------------

 Quick Start:

Frontend:

``` bash
git clone https://github.com/rashmiw333/Anvaya-FrontEnd
cd https://github.com/rashmiw333/Anvaya-FrontEnd
npm install
npm run dev
```

 Backend:

``` bash
git clone https://github.com/rashmiw333/Anvaya_Backend
cd https://github.com/rashmiw333/Anvaya_Backend
npm install
node index.js
```

------------------------------------------------------------------------

 Technologies:

-   React JS
-   React Router
-   JavaScript
-   Node.js
-   Express
-   MongoDB
-   Mongoose
-   Chart.js
-   Bootstrap
-   REST APIs
-   Vercel

------------------------------------------------------------------------

## Features

 Dashboard:

-   View important lead management information.
-   View total leads in the pipeline.
-   View total closed leads.
-   View lead status distribution.
-   View leads closed by sales agent.

Lead Management:

-   Display a list of all leads.
-   Add a new lead.
-   View detailed lead information.
-   Edit lead details.
-   Update lead status.
-   Assign sales agents to leads.
-   Set lead priority.
-   Add and manage lead tags.
-   Track time to close.
-   Delete leads.

 Lead Details:

-   View complete lead information.
-   View assigned sales agent.
-   View lead source, status, priority, tags, and time to close.
-   Add comments or updates to a lead.
-   View comments associated with a lead.

Sales Agent Management:

-   Add sales agents.
-   View all sales agents.
-   Prevent duplicate sales-agent email addresses.

Reports:

-   View leads closed during the last seven days.
-   View total leads currently in the pipeline.
-   View total closed leads.
-   View closed leads grouped by sales agent.
-   View lead status distribution.
-   Visualize report data using charts.

------------------------------------------------------------------------

Lead Lifecycle:

Leads can move through the following statuses:

``` text
New
  ↓
Contacted
  ↓
Qualified
  ↓
Proposal Sent
  ↓
Closed
```

The application also supports lead priorities:

``` text
High
Medium
Low
```

Lead sources include:

``` text
Website
Referral
Cold Call
Advertisement
Email
Other
```

------------------------------------------------------------------------

## API Reference

 Sales Agents

 POST `/api/agents`

Create a new sales agent.

Example request:

``` json
{
  "name": "John Doe",
  "email": "john@example.com"
}
```

GET `/api/agents`

Get all sales agents.

------------------------------------------------------------------------

 Leads

 POST `/api/leads`

Create a new lead.

 GET `/api/leads`

Get all leads.

 GET `/api/leads/:id`

Get details of a single lead.

 PUT `/api/leads/:id`

Update an existing lead.

 DELETE `/leads/:id`

Delete a lead.

> Note: The delete route in the current backend implementation is
> `/leads/:id` rather than `/api/leads/:id`.

------------------------------------------------------------------------

 Comments:

POST `/api/leads/:id/comments`

Add a comment to a lead.

Example request:

``` json
{
  "author": "SALES_AGENT_ID",
  "commentText": "Reached out to lead, waiting for response."
}
```

#### GET `/api/leads/:id/comments`

Get all comments for a lead.

------------------------------------------------------------------------

 Reports

 GET `/api/report/last-week`

Get leads that were closed during the last seven days.

 GET `/api/report/pipeline`

Get the total number of leads currently in the pipeline.

Example response:

``` json
{
  "totalLeadsInPipeline": 10
}
```

 GET `/api/report/closed`

Get the total number of closed leads.

Example response:

``` json
{
  "totalClosedLeads": 5
}
```

 GET `/api/report/closed-by-agent`

Get closed leads grouped by sales agent.

Example response:

``` json
{
  "John Doe": 3,
  "Jane Doe": 2
}
```

 GET `/api/report/status-distribution`

Get the distribution of leads across different statuses.

Example response:

``` json
{
  "New": 4,
  "Contacted": 3,
  "Qualified": 2,
  "Proposal Sent": 1,
  "Closed": 5
}
```

------------------------------------------------------------------------

 Backend Structure

The backend uses separate models for the main CRM entities:

``` text
models/
├── salesAgent.model.js
├── lead.model.js
├── comment.model.js
└── tag.model.js
```

The Express server provides REST APIs for:

-   Sales agents
-   Leads
-   Comments
-   Reports

MongoDB is used for persistent application data, with Mongoose used for
database operations.

------------------------------------------------------------------------

 Project Highlights

-   Built a complete CRUD workflow for lead management.
-   Implemented relationships between leads and sales agents using
    MongoDB references.
-   Added comments and updates for individual leads.
-   Added reporting APIs for pipeline, closed leads, agent performance,
    and status distribution.
-   Integrated Chart.js to visualize CRM reports.
-   Added loading and error handling in the React frontend.
-   Used React Router for navigation between CRM sections.
-   Deployed the backend using Vercel.

------------------------------------------------------------------------

 Repository

 Frontend
(https://github.com/rashmiw333/Anvaya-FrontEnd)

 Backend
(https://github.com/rashmiw333/Anvaya_Backend)

------------------------------------------------------------------------

 Vercel

 Frontend: https://anvaya-front-end.vercel.app/

 Backend: https://vercel.com/rashmiw333s-projects/anvaya-backend

------------------------------------------------------------------------

 Contact

For bugs or feature requests, please reach out to:

rashmiwankhade99@gmail.com
