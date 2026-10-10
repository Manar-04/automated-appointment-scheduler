# Automated Appointment Scheduling & Confirmation System

A no-code scheduling workflow built with **Zapier**, **Google Forms**, **Google Calendar**, and **Gmail**. When someone submits an appointment request, the Zap creates a detailed calendar event using the submitted fields and then runs a Gmail **Send Email** action for initial appointment communication.

> **Scope:** This project handles an initial confirmation or invitation, **not** a separate advance reminder. The screenshots show the configured workflow and tested Zap steps.
## Workflow

```text
Google Forms — New Form Response (trigger)
           ↓
Google Calendar — Create Detailed Event (action)
           ↓
Gmail — Send Email (action)
```

![Three-step Zap workflow](screenshots/workflow-overview.png)

## Implementation details

1. **Trigger:** Zapier listens for a **New Form Response** in Google Forms.
2. **Calendar action:** **Create Detailed Event** adds a new event to an appointment calendar. The event's summary includes the submitted name, and the description maps the appointment type, phone number, and notes from the form response.
3. **Email action:** A Gmail **Send Email** step provides initial appointment communication. The provided screenshots show the action and test status, but not its recipient/subject/body configuration.

## Tools and skills

| Tool | Role |
| --- | --- |
| Google Forms | Appointment request input |
| Zapier | Trigger-action orchestration and field mapping |
| Google Calendar | Detailed appointment event creation |
| Gmail | Initial email communication |

**Skills demonstrated:** workflow automation, SaaS application integration, event-driven triggers, field mapping, system testing, and documentation.

## Screenshots

- [Full workflow](screenshots/workflow-overview.png)
- [Google Forms trigger](screenshots/google-forms-trigger.png)
- [Calendar event configuration](screenshots/calendar-event-action.png)
- [Gmail action](screenshots/gmail-action.png)

The screenshots have been **redacted to remove identifiable contact and appointment details**. Do not commit account credentials, real client records, exported test payloads, or private Zap links.

## Recreate the workflow

1. Create a Google Form that collects appointment request details.
2. In Zapier, create a Zap with **Google Forms → New Form Response** as the trigger, connecting your own account.
3. Add **Google Calendar → Create Detailed Event** and map the form's responses into the event fields. Configure time and date fields to match your form.
4. Add **Gmail → Send Email** and configure the intended recipient, confirmation subject, and message using your own test data.
5. Test all steps with fictional sample data, verify the calendar entry and message, then publish/enable the Zap if appropriate.

This repository is **documentation**, not an importable Zap or source-code implementation. Exact email mappings and some calendar field settings are not included in the provided screenshots.

## Potential improvements

- Add separate advance reminders.
- Check for scheduling conflicts and duplicate requests.
- Add input validation and error alerts.
- Support cancellation and rescheduling.
- Reduce storage of personal information in calendar descriptions where possible.
