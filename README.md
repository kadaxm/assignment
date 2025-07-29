



# 📞 Workflow 1: Triggering Vapi Call from Tally Form Submission

[for demo of [form.JSON ](https://github.com/kadaxm/assignment/blob/da1302857f63bd5b2e37dd14deb79d378a8a2260/form.JSON)] 

## 🔗 Live Tally Form
[**➡️ Fill this form to start the process**](https://tally.so/r/w84Gkx)

> 📞 After submission, you will receive an automated call from the Twilio number: **+1 320-429-6710**

---

## 🧠 What Does This Workflow Do?

This workflow automates the journey from a form submission to receiving a call from an AI voice bot.  
It consists of the following steps:

---

## 🧩 Workflow Breakdown

### ✅ Step 1: Tally Form Submission
- A user submits a response on the Tally form.
- Responses include user details like **name, number, purpose**, etc.

### ✅ Step 2: Webhook Node
- The form submission is sent to a **Webhook URL** inside your workflow.
- This node acts as a **trigger** to start the automation.
- It listens for **incoming data from Tally**.

### ✅ Step 3: Airtable Node (Database Update)
- The data received via the Webhook is sent to **Airtable**.
- Airtable stores each response in a structured table.
- Airtable acts as the **backend database** for tracking submissions.

### ✅ Step 4: HTTP Request to Vapi
- Once the data is stored, the workflow sends an **HTTP POST request** to [**Vapi.ai**](https://vapi.ai).
- This request includes:
  - The **user’s phone number**
  - The **Vapi assistant ID**
- The Vapi AI Voice Bot then **calls the user** using the **Twilio phone number**.

---

## 📞 Phone Call Demo

Once you fill out the [form](https://tally.so/r/w84Gkx):

1. ✅ Your data is saved to **Airtable**
2. ✅ An **AI Voice Call** is triggered via **Vapi & Twilio**
3. ✅ You’ll receive a **real-time call** from the Vapi assistant

---

> ℹ️ _Ensure your webhook URL is connected properly inside Tally's integration settings. Airtable columns should match incoming data fields. The HTTP request must use correct Vapi credentials and Assistant ID._
