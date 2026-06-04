# DeskPilot 2.4 release notes

DeskPilot 2.4 includes updates to help support teams work faster, manage automations more safely, and view ticket and customer information more clearly. This release also includes several fixes for SLA time display, ticket merging, and saved reply formatting.

## New features

### Folders for saved replies

Support agents and team leads can now organise saved replies into folders.

Folders appear in the saved replies panel when composing a ticket reply, making it easier to find the right response when teams have many approved replies across different topics.

Existing saved replies are not automatically sorted into folders. They remain uncategorised until they are moved manually.

### Customer profile activity timeline

Customer profiles now include a read-only activity timeline.

The timeline shows recent customer activity directly on the customer profile page, so agents can review recent context without opening multiple previous tickets.

Timeline entries cannot be edited.

## Improvements

### Faster ticket search

Ticket search now returns results more quickly when searching by ticket ID, customer name, email address, or keywords.

This helps agents find the right ticket faster, especially during busy support periods.

### Redesigned ticket details panel

The ticket details panel has been reorganised to make key ticket information easier to scan.

Priority, status, assignee, tags, customer plan, and SLA due time are now grouped into clearer sections. No ticket data has changed, but some fields have moved to new positions.

### First response time filter in reports

Reporting views now include a first response time filter.

Team leads and managers can use this filter to review report data by response time ranges and identify queues, teams, or ticket types where initial responses may be delayed.

This filter does not affect SLA calculations.

## Admin updates

### Separate permission for automation management

Workspace admins can now use a separate **Manage automations** permission.

This permission allows selected users to create, edit, pause, and delete automation rules without giving them access to all workspace settings.

Existing admin access is unchanged.

## Fixes

### SLA due times now display in the workspace timezone

SLA due times now display consistently using the workspace timezone across ticket lists, ticket details, and reports.

Previously, some views used the agent’s browser timezone, which could cause distributed teams to see different SLA due times.

This is a display fix only. SLA calculation rules have not changed.

### Duplicate tags removed after ticket merge

When tickets are merged, duplicate tags are now automatically removed from the merged record.

This keeps merged ticket records cleaner and easier to read.

### Bullet list formatting preserved in saved replies

Saved replies that contain bullet lists now retain their formatting when inserted into a ticket reply.

Agents no longer need to manually fix list spacing before sending the reply.

## Known issues

### Large CSV exports may be delayed during peak usage

CSV exports containing more than 50,000 rows may take several minutes to generate during peak usage.

Exports continue processing in the background, and users can continue working while waiting. The export will complete once processing is finished.

Admins and team leads running large reporting exports should allow extra time during busy periods.