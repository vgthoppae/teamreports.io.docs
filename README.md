# teamreports.io - User Guide

## What?

teamreports is a SaaS platform for teams to collabartivaely build reports and share them with stakeholders. Typically SaaS platforms provide a service that can be used by subscribers. In addition to being a simple Saas Platform, teamreports.io provides capabilities for each organization to dynamically configure and customize the behavior in a way typical to a No Code platform.

## Why?

The use case of team based reports building is often overlooked and teams usually resort to manual process of collecting information from the team members, iteratively refining them going back and forth before emailing to stakeholders. This manual process is fraught with too many problems including redundancy, error-prone, time-consuming and inefficent simply. This practice is accepted in the industry and there is a good amount of innovation and automation possible in this space, where teamreports is taking a small step forward.

## Where?

The process of collaboratively building reports is not only limited to status reports meant for stakeholders. It can be used in several other use cases such as

- Performance Appraisal Reports, where an individual self-apprises his or her performance which gets reviewed by the manager and feedback is provided before publishing
- Organizations often engage external consulting services and are required to provide a report of the engagement to the higher management
- Enterprises may have several ongoing efforts and a report on progress of one or more would be often necessary
- Agile Retrospective Reports, where agile teams report on what went well and otherwise
- Outage Summary Report to summarize an outage that may have occurred

The possiblities are almost endless on where teamreports could be used.

## How?

### Dynamic Report templates

Each team has a unique need for specific use case. There cannot be a one-size fit all approach with the templates. Hence teamreports allows teams define their own template for each reporting needs.

### Role based

In the process of building the reports, team members don different roles each with a specific responsibility.

### Workflow driven Reporting Process

The entire report generation process is driven by a workflow where team members with a specific role participate at corresponding step.

### Configurabe Workflow

The workflow itself is configurable at each level to give flexibility to teams on driving the report behavior.

## Concepts and Features

### Report Template

At a fundamental level, ignoring the cosmetic aspects, a report is nothing but a simple collection of labels and information corresponding to each of that. A Report Template consists of such a collection of labels with a UI control corresponding to each. Currently two popular below mentioned controls are supported for the MVP release. As the teamreports community grows, it is straightforward and non-invasive adding new controls to support a variety of behaviors. React UI engine renders report forms dynamically based on the configured template.

Simple Edit Control - As per the name, it is a simple control that accepts user inputs.

Rich Edit Control - It accepts the user inputs and allows user to beautify and format the contents.

### Report Types

A report can be Adhoc or Recurring in nature.

Adhoc Reports are used for one-off use where once its lifecycle completes, it is only available for viewing.

Recurring Reports can recur periodically such as weekly, monthly etc., This means a new report content can be provided every period, where each periodic report goes through its own cycle. Currently supported periods are Daily, Weekly, Monthly, Quarterly and Yearly.

### Report Ownership

User(s) contributing content to the report is(are) considered the report owner(s). There are two types of ownership possible.

- Individual team member, where each contributor has their own copy which flows through its own lifecycle
- Two or more team members collectively contribute content to a report copy

The second option is part of a future release.

### Report Actors (Roles)

As mentioned earlier, the team members play different roles in the report generation process.

Admin user has following responsibilities.

- Assign roles to team members
- Customize workflow for different reports
- Assign report specific roles

Author configures report templates
Contributor contributes content to reports
Reviewer reviews reports and provides feedback for go-ahead or request rework
Publisher accepts the reviewer recommendation and publishes the report for readers visibility
Readers view the published reports

### RBAC (Role Based Access Control)

Depending on the role assigned to a user (Author, Contributor etc.,) he or she can perform only the corresponding permitted actions as explained above. However a user can be assigned with more than one role and has an option to choose one of the granted roles to perform corresponding actions. But this role applies globally across all the reports. If report specific role is desired, read the following section.

### Report Specific Access Control

As the number of reports grows, it may not be desirable to have users having same level of permission for all reports. The feature of report specific access control overcomes that problem by restricting the permission level at report level. For example, if John and Lisa have contributor roles, you could say only Lisa could work contribute on 'Report A'. For the MVP release, this permission is not enforced though the screen does exist to configure the permission.

### Report Workflow (Lifecycle)

Out of the box, all reports go through the below standard steps.

Contribute - Review &#9658; &#47;
