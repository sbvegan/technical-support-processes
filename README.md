# Technical Support Processes

The following technical support process takes into account high-level areas:

- **Ticketing System** - A central location to manage issues.
- **Intake and Triage** - Gather information about the issue and client, assess, and determine the *categorization and prioritization*.
    - todo: sub-process map
- **Categorization and Prioritization** - Categorize the technical realm the issue falls under. Prioritize issue based on the urgency and impact of the issue.
    - todo: resource of category descriptions
    - todo: sub-process map for prioritization
- **Initial Response** - Acknowledge the clients issue and provide estimated time for fix. *Note: idk about this one. its good to keep continual communication and updates, but I want to manage expectations. I'll need to get into the weeds before I can even provide accurate time estimates.*
    - todo: resource: HOW to respond/response template
- **Troubleshooting and Resolution** - Assign the task of servicing the issue (ideally to a domain expert), they investigate, identify the root cause, and then resolve the issue.
    - todo: sub-process: identify WHO is responsible
    - todo: resource: HOW to troubleshoot guide
- **Communication and Updates** - Maintain continuous communication with the client on updates throughout the *troubleshooting and resolution* sub-process.
    - todo: resource: guide on HOW to keep a client updated 
- **Escalation** - When an issue is blocked, a sub-process for dealing with more complex issues is spun up. Continue with *Communication and Updates* until resolution.
    - todo: guide: HOW/WHEN to escalate an issue
- **Resolution and Closure** - Notify the client when you have a fix, receive client verification of resolution, and then close the issue.
    - todo: resource: closure protocol
- **Documentation and Knowledge Base** - Document the steps taken to resolve the issue. Both troubleshooting and the fix. Build up a knowledge base of case studies.
    - todo: sub-process: issue closure post-mortem
- **Analysis and Continuous Improvement** - Utilize your *Knowledge Base* to identify key insights. Ex. trends, recurring issues, and general hotspots.
    - todo: resource: tips and tricks

## Process Map

***Note: this diagram utilizes Universal Process Notation (UPN), but with minor modifications to be more cohesive with GitHub (i.e. top to bottom, resource and sub-process links below).***

```mermaid
---
title: Technical Support Process
---
stateDiagram-v2
    SUBMIT: 1. Submit issue\nR - Client
    INTAKE: 2. Gather information\nRA - TSM
    TRIAGE: 3. Categorize, prioritize, and acknowledge\nRA - TSM
    RESOLVE: 4. Resolve issue\nRA - TSM
    COMMUNICATE: 5. Communicate progress.\nRA - TSM\nI - Client
    ESCALATE: 6. Escalate issue\nRA - TSM\nC - Engineering
    CLOSE: 7. Close issue\nRA - TSM\nI - Client
    DOCUMENTATION: 8. Update knowledge base\nRA - TSM

    [*] --> SUBMIT: client finds issue
    SUBMIT --> INTAKE: Technical issue
    INTAKE --> TRIAGE: 
    TRIAGE --> RESOLVE: troubleshoot
    RESOLVE --> COMMUNICATE: Fix in progress
    RESOLVE --> ESCALATE: Not resolved
    RESOLVE --> CLOSE: Resolved
    ESCALATE --> CLOSE: Resolved
    CLOSE --> DOCUMENTATION: Document
    DOCUMENTATION --> [*]: client issue resolved

    NOTE: ---Key---\nRACI (Responsible, Accountable, Consulted, Informed)\nTSM = Technical Support Manager

    note right of DOCUMENTATION
        As you build your knowledge base,
        perform analysis to identify trends,
        recurring issues, hotspots, etc.
    end note
```

### Sup-processes and resources

todo: define subprocesses and link the markdown files

todo: add resource attachments