# GTM Event Cookie Counter

## Overview
The **GTM Cookie Counter** tag template is designed to count and track user interactions, such as pageviews, product page views within a session or across visits. It checks if a cookie exists, increments its value if found, or creates it if missing. Optionally, it pushes an event to the Data Layer upon execution.

## Features
- Checks for an existing cookie and updates its value.
- Creates the cookie if it does not exist.
- Configurable expiration time (seconds, minutes, hours, or days).
- Supports custom domain and path settings.
- Option to push a Data Layer event when the cookie updates.
- Customizable event name for Data Layer push.

## Installation

1. Open **Google Tag Manager**.
2. Navigate to **Templates** and click **New** under **Tag Templates**.
3. Click **Import** and upload the GTM Cookie Counter template.
4. Save the template and publish your GTM container.

## Configuration

### Required Fields
- **Cookie Name:** The name of the cookie that stores the counter.
- **Cookie Duration:** Select how long the cookie should persist (Seconds, Minutes, Hours, or Days).
- **Cookie Lifespan:** Enter the lifespan value corresponding to the selected duration unit.

### Optional Settings
- **Push to Data Layer:** Enables pushing an event to the Data Layer when the cookie updates.
- **Use Custom Event Name:** Allows customization of the Data Layer event name.
- **Custom Event Name:** If enabled, this is the event name that will be pushed.
- **Advanced Configuration:**
  - **Set Custom Domain:** Define a specific domain for the cookie.
  - **Set Custom Path:** Define a specific path for the cookie.

## Example Use Case
**Scenario:** Track the number of pageviews for a user session.

1. Set the cookie name to `gtm_pageview_counter`.
2. Choose `Session` duration (e.g., 30 minutes in minutes).
3. Enable Data Layer push to track the count with each execution.
4. Use a GTM event trigger to fire this tag on each pageview.

## Data Layer Event Example
If "Push to Data Layer" is enabled, the following event will be pushed:

```javascript
{
  "event": "gtm_temp_dd_eventUpdate", // or custom name if specified
  "gtm_current_value": 3 // The updated cookie value
}
```

## License
This project is licensed under the APACHE License.

Developed by **Jude Nwachukwu Onyejekwe** for [**DumbData**](https://dumbdata.co/). where you can find more analytics resources in the **Measurement Resource Hub**.

