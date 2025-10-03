# How to configure Webhooks

### What is a Webhook?

Think of a webhook as a **doorbell for your apps**. When something happens in XLPrompt (like converting Excel data to JSON), it can automatically "ring the doorbell" of another app by sending the data there instantly.

### Why Use Webhooks with XLPrompt?

XLPrompt's webhook feature lets you **automate what happens** after you convert your Excel data to JSON. Instead of manually copying and pasting data into other tools, webhooks send it automatically.

#### Common Use Cases

✅ **Send data to AI tools** - Automatically process your Excel data with ChatGPT, Claude, or custom AI models\
✅ **Update databases** - Push converted data directly into Airtable, Google Sheets, or your database\
✅ **Trigger workflows** - Start automated processes in your business tools\
✅ **Log and track** - Keep records of all data conversions in your CRM or project management tool\
✅ **Notify teams** - Send Slack/Teams messages when data is processed

### Webhook Integration with No-Code Tools

The best part? You don't need to be a programmer! Popular no-code automation platforms make it easy to receive data from XLPrompt:

#### &#x20;Popular No-Code Platforms

| Platform                                                         |
| ---------------------------------------------------------------- |
| [**Zapier**](https://zapier.com/)                                |
| [**Make.com**](https://make.com/)                                |
| [**Pabbly Connect**](https://pythonandvba.com/go/pabbly-connect) |
| [**n8n**](https://n8n.io/)                                       |

All of these platforms provide a **webhook URL** that you can paste into XLPrompt's settings.

***

### How to Set Up Webhooks in XLPrompt

#### Step 1: Get Your Webhook URL

First, create a webhook in your automation platform:

**Example: Pabbly Connect**

1. Create a new workflow
2. Select **"Webhook"** as the trigger
3. Copy the webhook URL

#### Step 2: Configure XLPrompt

1. Open XLPrompt settings
2. Go to the **"Webhook"** tab
3. Check **"Enable Webhook Integration"**
4. Paste your webhook URL
5. Click **"Save & Close"**

#### Step 3: Test the Connection

1. Click the **"Test Webhook"** button in settings
2. Check your automation platform - you should see a test message arrive
3. If successful, you're ready to go!&#x20;

### Advanced Configuration

#### Authentication (Optional)

Some webhooks require authentication for security:

1. **Header Name**: The authentication header (e.g., `Authorization`, `X-API-Key`)
2. **Header Value**: Your secret token or API key (e.g., `Bearer abc123xyz`)

**Example:**

```
Header Name: X-API-KeyHeader Value: your-secret-key-here
```

#### Response Output Options

Choose where XLPrompt shows the webhook response:

* **Show in MessageBox**: Simple popup with success/error message (default)
* **Create New Sheet**: Response appears in a new Excel worksheet
* **Output to Selected Cell**: Response goes into the cell you selected

#### Timeout Settings

**Timeout (seconds)**: How long to wait for a response (default: 30 seconds)

* Increase for slow APIs or complex processing
* Range: 1-300 seconds (5 minutes max)

### Understanding the Data Format

XLPrompt sends your Excel data as **JSON** (a universal data format that all modern tools understand).

#### Example: What Gets Sent

When you select this Excel data:

| Name  | Age | City |
| ----- | --- | ---- |
| Alice | 28  | NYC  |
| Bob   | 35  | LA   |

XLPrompt sends this JSON:

```
json{  "data": [    {"Name": "Alice", "Age": 28, "City": "NYC"},    {"Name": "Bob", "Age": 35, "City": "LA"}  ]}
```

You can also include:

* **Custom prompts**: Instructions for AI processing
* **Context**: Additional information about the data
* **Metadata**: Workbook name, sheet name, timestamp, etc.

### Troubleshooting

#### ❌ "Webhook request failed"

**Possible causes:**

* Invalid webhook URL - double-check you copied it correctly
* Webhook expired - some platforms have temporary URLs
* Network connection issue - check your internet

**Solution**: Click "Test Webhook" to verify the URL works

#### ❌ Timeout Error

**Possible causes:**

* Webhook endpoint is slow to respond
* Complex processing taking too long

**Solution**: Increase timeout in settings (30-60 seconds usually works)

#### ❌ Authentication Failed

**Possible causes:**

* Wrong header name or value
* Expired API key

**Solution**: Verify authentication details with your platform's documentation

### Security Best Practices

* **Keep your webhook URLs private** - They're like passwords for your automations
* **Use authentication** when available - Adds an extra security layer
* **Monitor usage** - Check your automation platform for unexpected activity
