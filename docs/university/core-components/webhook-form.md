---
description: >-
  Webhook Hook Forms enable form submissions to get sent to an email address and
  optionally third-party services like Airtable, n8n, or Zapier.
---

# ✍️ Webhook Form

{% hint style="info" %}
**Name change:** Webhook Forms used to be called "Forms." However, [Forms](form.md) are now a different component intended for building searches and filters.
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=eE-CkewQHMs" %}

## Receiving Form Submissions

Webhook Forms are used when you need to send form submission data to an external service, rather than modifying page content like searches and filters.

### Email Notifications

By default, submissions are sent to the Project owner.

{% hint style="info" %}
**Pro feature:** You can customize the recipient of email notifications by navigating to **Project Settings > General**.

![Field to customize the recipient of the form submissions](../../.gitbook/assets/form-recipient.png)
{% endhint %}

### Webhooks

You can also send form submission data to a webhook—an external URL that receives the data and triggers an action, such as adding a contact to an email automation platform.

1. Obtain a webhook URL from a third-party platform such as [Airtable](../integrations/airtable-1.md).
2. Paste the URL into the `Action` field in **Webhook Form > Settings**.

Once set up, every form submission will send a payload (form fields and values) to the webhook URL.

## Using the Webhook Form Component

You can add a Webhook Form Component to your canvas from **Components Panel > Data section**.

{% hint style="warning" %}
Webhook Forms do not submit inside the Builder, including in Preview. They only submit on the published site.
{% endhint %}

### Webhook Form Structure

A Webhook Form consists of three nested instances:

1. **Form Content** – The primary form fields.
2. **Success Message** – Displayed upon successful submission.
3. **Error Message** – Shown when an error occurs.

You can [add new Components](form.md#form-inputs) to further expand and modify your form.

### Form States

Webhook Forms automatically switch between states based on submission results.

#### Success Message

When a submission is successful, users will see a success message. To customize it:

1. Select the main "Form" instance and go to **Settings**.
2. Change the **State** from "Initial" to "Success."
3. Edit the success message directly on the canvas.

#### Error Message

If there’s an error during submission, users will see an error message. To modify it:

1. Select the Webhook Form Component.
2. Set the **State** to "Error" to preview and edit the error message.

## Form Inputs

{% hint style="warning" %}
Each input field must have a `name` attribute for its data to appear in email notifications and webhook payloads.
{% endhint %}

Ensure every form input has a value for the `name` field to be included in submissions.

<figure><img src="../../.gitbook/assets/form-name.png" alt="Form input name"><figcaption></figcaption></figure>

For a full list of input types, including checkboxes and radio buttons, refer to [Form Inputs](form.md#form-inputs).
