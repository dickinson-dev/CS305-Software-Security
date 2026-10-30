# CS 305: Software Security

This repository contains my portfolio artifact and reflection for SNHU's CS 305 Software Security course.

## Portfolio Artifact

- [Artemis Financial Vulnerability Assessment Report](CS-305-Project-One-Dickinson.docx) — Manual security review, OWASP Dependency-Check findings, and a mitigation plan for the Artemis Financial application.

## Reflection

### Client and software requirements

Artemis Financial was the client, and Global Rain modernized its software. The central concern was protecting sensitive customer and financial information while maintaining reliable application services. My assessment considered secure communications, input validation, API access, database security, error handling, and third-party dependencies. The project information didn't specify Artemis Financial’s operating regions or exact regulatory obligations, so I flagged those as requirements the team would need to confirm.

### What I did well and why secure coding matters

I connected findings to specific code and explained their potential impact without claiming that every risk was already exploitable. My review identified issues such as hardcoded database credentials, unclosed database connections, insufficient deposit validation, possible integer overflow, and missing access controls for the read endpoint. Secure coding helps protect customer information, preserve financial data integrity, maintain service availability, and support customer trust. Those protections also reduce the risk of incidents that could disrupt the company or damage its reputation.

### Most challenging or helpful part

The dependency scan was especially helpful because it revealed risks beyond the application’s own source code. OWASP Dependency-Check reported findings across multiple dependencies. Interpreting those results required care: the report included repeated vulnerability findings, and a flagged dependency alone does not prove the application is exploitable. Connecting automated findings with manual code review helped me build a more useful assessment.

### Security layers and future assessment

I recommended several layers of protection, including protected credential configuration, least-privilege database access, reliable connection cleanup, input validation, encapsulation of account balances, authentication and authorization for sensitive endpoints, and HTTPS. In future assessments, I would combine manual code review with dependency scanning, focused testing, and deployment configuration review. I would verify each finding against the application’s actual code, components, and environment before selecting or documenting a mitigation.

### Checking functionality and security

My mitigation plan calls for building and testing the application after changes, including endpoint behavior, database operations, transaction boundaries, access controls, and HTTPS. It also calls for running Dependency-Check again and comparing the results with the original scan. These checks help identify regressions and remaining dependency risks. The submitted report documents proposed mitigations and validation steps; it does not claim that those remediations were implemented.

### Useful resources, tools, and practices
I can carry these practices into future development work: 
OWASP Dependency-Check, manual review of source code and configuration, secure credential management, least privilege, input validation, controlled error handling, and repeatable testing. I also learned to distinguish confirmed code findings from risks that depend on deployment details or how a component is used.

### Work to show an employer

I would show the vulnerability assessment report as evidence that I can review an application systematically, explain technical risks in context, and propose prioritized mitigations. The report also demonstrates experience using a dependency-scanning tool and communicating limitations, assumptions, and verification steps.
