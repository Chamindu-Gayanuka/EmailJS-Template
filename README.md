# EmailJS Portfolio Email Templates

A collection of clean, modern, dark-themed HTML email templates designed for portfolio contact forms using **EmailJS**.

The templates are optimized for professional portfolio websites and provide a consistent communication flow between the website visitor and the portfolio owner.

## 📧 Templates

This repository contains two email templates:

### 1. `AutoReply.html`

An automatic confirmation email sent to the person who submits the contact form.

**Purpose:**

* Confirms that the message was successfully received.
* Thanks the visitor for contacting you.
* Lets the visitor know that a response will follow.

**Template variables:**

| Variable   | Description    |
| ---------- | -------------- |
| `{{name}}` | Visitor's name |

---

### 2. `ContactUS.html`

An email notification sent to the portfolio owner whenever someone submits the contact form.

**Purpose:**

* Displays the sender's information.
* Shows the submitted message.
* Includes the received time.
* Provides a clear "New Inquiry" status.

**Template variables:**

| Variable      | Description             |
| ------------- | ----------------------- |
| `{{name}}`    | Visitor's name          |
| `{{email}}`   | Visitor's email address |
| `{{message}}` | Submitted message       |
| `{{time}}`    | Message received time   |

---

## ✨ Features

* 🌑 Modern dark-themed design
* 💜 Purple accent color scheme
* 📱 Responsive email-friendly layout
* 📩 Designed specifically for EmailJS
* 📨 Separate notification and auto-reply templates
* 🧩 Simple EmailJS template variables
* 📋 Table-based HTML structure for better email-client compatibility
* 🎨 Inline CSS for reliable email rendering
* ✦ Minimal and professional portfolio aesthetic
* 🔒 No external CSS or JavaScript dependencies

## 📁 Project Structure

```text
emailjs-portfolio-templates/
│
├── AutoReply.html
├── ContactUS.html
└── README.md
```

## ⚙️ EmailJS Setup

### 1. Create an EmailJS account

Create an account on EmailJS and configure your email service.

### 2. Add the templates

Create two EmailJS email templates:

```text
Auto Reply
Contact Notification
```

Copy the contents of:

```text
AutoReply.html
```

into the **Auto Reply** template.

Then copy:

```text
ContactUS.html
```

into the **Contact Notification** template.

### 3. Configure template variables

Make sure the variable names used by your website match the variables expected by the templates.

#### Auto Reply

```text
{{name}}
```

#### Contact Notification

```text
{{name}}
{{email}}
{{message}}
{{time}}
```

## 🔗 Example EmailJS Workflow

A typical portfolio contact form can use the following flow:

```text
Visitor
   │
   ▼
Portfolio Contact Form
   │
   ▼
EmailJS
   │
   ├──────────────► ContactUS Template
   │                     │
   │                     ▼
   │              Portfolio Owner
   │
   └──────────────► AutoReply Template
                         │
                         ▼
                    Website Visitor
```

This allows the portfolio owner to receive the inquiry while the visitor immediately receives a confirmation email.

## 🧑‍💻 Example JavaScript Integration

Example EmailJS implementation:

```javascript
emailjs.send(
    "YOUR_SERVICE_ID",
    "YOUR_CONTACT_TEMPLATE_ID",
    {
        name: name,
        email: email,
        message: message,
        time: new Date().toLocaleString()
    }
);
```

For the automatic reply:

```javascript
emailjs.send(
    "YOUR_SERVICE_ID",
    "YOUR_AUTOREPLY_TEMPLATE_ID",
    {
        name: name
    }
);
```

Replace the placeholder values with your actual EmailJS configuration.

## 🎨 Design

The templates use a minimal dark interface inspired by modern developer portfolios.

### Color Palette

| Element              | Color     |
| -------------------- | --------- |
| Background           | `#09090b` |
| Card                 | `#111113` |
| Secondary Background | `#18181b` |
| Border               | `#27272a` |
| Primary Text         | `#fafafa` |
| Secondary Text       | `#a1a1aa` |
| Muted Text           | `#71717a` |
| Purple Accent        | `#8b5cf6` |
| Light Purple         | `#a78bfa` |
| Success              | `#6ee7b7` |

## 📱 Email Compatibility

The templates are built using email-compatible HTML techniques, including:

* HTML tables for layout
* Inline CSS
* Presentation attributes
* Simple typography
* No JavaScript
* No external stylesheets
* No external UI frameworks

However, email clients can render HTML differently. Always test the templates with the email providers and clients you intend to support.

## 🔐 Security Notes

Do not place sensitive information inside the HTML templates.

EmailJS public configuration values such as the **Public Key** are intended to be used client-side, but sensitive credentials should never be exposed in frontend code.

Never include:

```text
Email passwords
SMTP passwords
Private API keys
Database credentials
Secret tokens
```

in these templates or your public repository.

## 🛠️ Customization

You can easily customize:

* Name
* Job title
* Accent colors
* Background colors
* Email text
* Footer text
* Status labels
* Portfolio branding
* Template width
* Typography

For example, replace:

```html
Chamindu Gayanuka
```

with your own name and update:

```html
Software Engineering Undergraduate · Developer
```

to your preferred professional title.

## 📄 License

You are free to use, modify, and adapt these templates for your own portfolio or personal projects.

If you redistribute a modified version, attribution is appreciated but not required.

---

## ⭐ Support

If these templates are useful for your portfolio, consider giving the repository a ⭐ on GitHub.

Built with ❤️ using HTML and EmailJS.
