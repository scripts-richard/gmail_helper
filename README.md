# Gmail Helper

Simple helper script for sending emails using the Gmail API. Copied and updated for Python 3 from the Google Gmail [Quickstart](https://developers.google.com/gmail/api/quickstart/python) guide.

## Getting Started

Follow the Google [Quickstart](https://developers.google.com/gmail/api/quickstart/python) guide.

### Prerequisites

Python 3

Gmail account configured as per [Quickstart](https://developers.google.com/gmail/api/quickstart/python) guide.

### Usage

Place or link gmail_helper.py to project folder and import into project:

```
import gmail_helper
```

Your Google API key is loaded from secrets.py (needs to be created):

```
API_KEY = 'api key'
```

Emails are loaded from a file with the sender on the first line and recipients on the following lines:

```
sender@email.com
recipient1@email.com
recipient2@email.com
...
recipientn@email.com
```

Load emails from the file and then send:

```
sender, recipients = gmail_helper.get_emails(emails_filename)
gmail_helper.email(sender, recipients, 'Subject', 'Message Text', '<html>Message html</html>')
```
