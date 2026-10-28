# Qiyam — Candidate Assessment & Interview Management

### A structured workflow for interview sessions, candidate evaluations, and management review

Qiyam brings interview administration and candidate evaluation into one bilingual web application. It connects candidate records, interview sessions, assigned evaluators, assessment questions, results, and reporting through role-specific interfaces.

## The Idea

Interview information can become fragmented across candidate files, evaluation forms, and separate reports. Qiyam organizes these steps into a shared workflow, making it easier to manage sessions, collect evaluations, compare results, and review outcomes.

## Development Highlights

- Built an Arabic/English interface for candidate assessment and interview management.
- Organized workflows around administrator, data-entry, evaluator, and manager roles.
- Connected candidate registration, CV attachments, interview sessions, and evaluator assignments.
- Added structured evaluation workflows, score summaries, and candidate comparison views.
- Provided management dashboards, evaluator analytics, reports, and review history.
- Packaged the application as separate frontend, backend, and PostgreSQL services using Docker Compose.

## Roles & Workflows

| Role | Main workflow |
| --- | --- |
| Administrator | Manage users, roles, assessment questions, reference lists, and system settings |
| Data Entry | Register candidates and organize interview sessions |
| Evaluator | Access assigned candidates and complete evaluations |
| Manager | Review results, compare assessments, and record final decisions |

## Features

### Interview Sessions
- Create and manage sessions with job vacancy and department information.
- Assign evaluators and register candidates within a session.
- Activate, close, archive, and reopen sessions.
- Review session details and candidate assessment summaries.

### Candidate Records
- Register and update candidate profiles.
- Upload, view, and manage CV attachments.
- Schedule interviews and manage evaluator assignments.
- Track candidate and assessment status.

### Structured Evaluation
- Maintain assessment questions.
- Capture and submit evaluator responses.
- Present score summaries and decision categories.
- Compare candidate results within an interview session.
- Support manager review and decision overrides.

### Reporting & Administration
- Manager dashboard and evaluator analytics.
- Reports covering candidates, evaluators, sessions, and results.
- CSV and Excel export options.
- Notifications and review/audit views.
- User, role, reference-list, and system-setting administration.
- Arabic and English interface options.

### Candidate Summary Interface
The interface includes an AI-summary view for candidates. The available deployment package does not establish how summaries are generated, so no specific AI provider, model, or generation method is claimed here.

## Architecture

| Layer | Technology / function |
| --- | --- |
| Frontend | React interface with Redux state-management bundles and Axios API requests |
| Web serving | Nginx serving the frontend and proxying API traffic |
| Backend | ASP.NET Core / .NET API |
| Application structure | API, Application, Domain, and Infrastructure assemblies |
| Data access | Entity Framework Core with Npgsql |
| Database | PostgreSQL |
| Authentication | JWT-based authentication components |
| Password handling | BCrypt dependency |
| File integration | Cloudinary SDK and upload-storage configuration |
| Deployment | Docker images coordinated through Docker Compose |

## Application Flow

1. An administrator configures accounts, reference lists, and assessment questions.
2. Interview sessions and candidate records are created.
3. Evaluators are assigned to sessions or candidates.
4. Evaluators complete their assessments.
5. Managers review summaries, comparisons, and supporting records.
6. Reports can be exported for further review.

## Practical Value

- Consolidates candidate information and interview activity into one workflow.
- Supports consistent evaluation through a managed question set.
- Separates responsibilities across role-specific interfaces.
- Provides summaries and comparison views for management review.
- Makes reporting outputs available in common spreadsheet formats.

## Project Documentation

This overview is based on inspection of the supplied deployment package, interface routes, and application assemblies. Features describe the available implementation evidence; runtime behavior and the AI generation workflow have not been independently verified.
