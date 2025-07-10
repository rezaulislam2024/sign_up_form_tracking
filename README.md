# EduTech Form Tracking with Google Tag Manager

This project demonstrates how to track a Ninja Forms submission using Google Tag Manager (GTM) and push custom event data to the `dataLayer`.

## Features

- Ninja Forms hook: `nfFormSubmitResponse`
- Clean field processing (e.g., phone formatting)
- Pushes to `dataLayer` with custom event: `sign_up_for_tutoring`
- Pre-configured for GTM/GA4 integration

## Setup Steps

1. Replace `GTM-XXXXXXX` with your GTM container ID.
2. In Google Tag Manager:
   - Create **Custom Event Trigger** for `sign_up_for_tutoring`
   - Create **Data Layer Variables** (e.g., `inputs.name`, `inputs.email`)
   - Create **GA4 Event Tag** to capture and send form data
3. Test using GTM Preview mode or Google Tag Assistant

## Sample DataLayer Output

```json
{
  "event": "sign_up_for_tutoring",
  "form_id": "1",
  "inputs": {
    "name": "John Doe",
    "email": "john@example.com",
    "phone": "1234567890"
  }
}
