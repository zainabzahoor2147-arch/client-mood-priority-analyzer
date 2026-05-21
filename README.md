# client-mood-priority-analyzer
## Overview
Client Mood & Priority Analyzer is an AI-powered customer support assistant built using Claude AI.
The tool analyzes customer messages and automatically detects:
- Customer Mood
- Priority Level
- Recommended Action
- Professional Support Response
- Internal CRM Notes
This helps support teams respond faster, maintain professionalism, and improve customer satisfaction.
## Features
Mood Detection
Detects emotions such as:
- Angry
- Frustrated
- Happy
- Confused
- Neutral
### Priority Classification
Classifies support urgency into:
- High Priority
- Medium Priority
- Low Priority
### AI Suggested Actions
Provides recommended next steps for support specialist.
### Professional Reply Generator
Creates polite and professional customer responses.
### Internal CRM Notes
Generates internal notes for support teams that are not visible to customers.
## Example Workflow
### Customer Message
"Hi team,my onbaording has been delayed for several days what are you doingggggg i am struggling to get updates.This is effecting our operations.
Whyy its delayed i need urgent assistant."
### AI Analysis
#### Mood
Highly Frustrated 
#### Priority
Critical/ urgent
#### Recommended Action
call immediately etc.
#### Professional Response
[attached in video]
## Technologies Used
- Claude AI
- Prompt Engineering
- GitHub
- Loom
This project demonstrates how AI can improve customer support operations through intelligent message analysis and automated assistance.
## Demo Video
(https://www.loom.com/share/8db8d383b24c45d6b1a2f9f81087e1c0).
## Author
Zainab Zahoor
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Client Onboarding System</title>

  <style>

    body {
      font-family: Arial, sans-serif;
      background-color: #f4f6f9;
      padding: 20px;
    }

    .container {
      max-width: 700px;
      background: white;
      margin: auto;
      padding: 25px;
      border-radius: 10px;
      box-shadow: 0px 0px 10px rgba(0,0,0,0.1);
    }

    h1 {
      text-align: center;
      margin-bottom: 30px;
    }

    h3 {
      margin-top: 25px;
      color: #333;
    }

    label {
      font-weight: bold;
      display: block;
      margin-top: 15px;
    }

    input,
    select,
    textarea {
      width: 100%;
      padding: 10px;
      margin-top: 5px;
      border-radius: 5px;
      border: 1px solid #ccc;
      font-size: 14px;
    }

    textarea {
      height: 150px;
    }

    button {
      width: 100%;
      margin-top: 25px;
      padding: 12px;
      background-color: #007bff;
      color: white;
      border: none;
      border-radius: 5px;
      font-size: 16px;
      cursor: pointer;
    }

    button:hover {
      background-color: #0056b3;
    }

  </style>
</head>

<body>

  <div class="container">

    <h1>Client Onboarding System</h1>

    <!-- CLIENT INFORMATION -->
    <h3>Client Information</h3>

    <label>Full Name</label>
    <input type="text" placeholder="Enter client name">

    <label>Email</label>
    <input type="email" placeholder="Enter email">

    <label>Phone Number</label>
    <input type="text" placeholder="Enter phone number">

    <label>Company Name</label>
    <input type="text" placeholder="Enter company name">

    <!-- SERVICE DETAILS -->
    <h3>Service Details</h3>

    <label>Service Type</label>

    <select>
      <option>Support</option>
      <option>CRM Setup</option>
      <option>Website Development</option>
      <option>Mobile App</option>
    </select>

    <label>Expected Start Date</label>
    <input type="date">

    <!-- AI ANALYSIS -->
    <h3>AI Client Analysis</h3>

    <label>Client Mood</label>

    <select id="clientMood">

      <option>Happy 🙂</option>
      <option>Confused 😕</option>
      <option>Angry 😡</option>
      <option>Neutral 😐</option>

    </select>

    <label>Priority Level</label>

    <select id="priorityLevel">

      <option>Low</option>
      <option>Medium</option>
      <option>High</option>
      <option>Urgent</option>

    </select>

    <label>Project Description / CRM Notes</label>

    <textarea id="projectDescription"
      placeholder="Client details and onboarding notes will appear here...">
    </textarea>

    <button onclick="submitForm()">
      Submit Onboarding
    </button>

  </div>



  <!-- JAVASCRIPT STARTS HERE -->
  <script>

    const moodField = document.getElementById("clientMood");

    const priorityField =
      document.getElementById("priorityLevel");

    const projectField =
      document.getElementById("projectDescription");


    moodField.addEventListener("change", function () {

      const mood = moodField.value;


      if (mood.includes("Angry")) {

        priorityField.value = "Urgent";

        projectField.value =
`Priority Level: Urgent

Recommended Action:
Assign senior onboarding specialist immediately.

Professional Response:
We sincerely apologize for the inconvenience and will prioritize your concern urgently.

Internal CRM Note:
Client is frustrated and requires escalation handling.`;

      }


      else if (mood.includes("Confused")) {

        priorityField.value = "High";

        projectField.value =
`Priority Level: High

Recommended Action:
Provide detailed onboarding guidance and clarification.

Professional Response:
Thank you for your patience. We’ll guide you carefully through the onboarding process.

Internal CRM Note:
Client requires additional onboarding assistance.`;

      }


      else if (mood.includes("Happy")) {

        priorityField.value = "Medium";

        projectField.value =
`Priority Level: Medium

Recommended Action:
Proceed with standard onboarding process.

Professional Response:
We’re excited to assist you with your onboarding journey.

Internal CRM Note:
Client is cooperative and onboarding is progressing smoothly.`;

      }


      else {

        priorityField.value = "Low";

        projectField.value =
`Priority Level: Low

Recommended Action:
Follow regular onboarding workflow.

Professional Response:
Thank you for contacting us.

Internal CRM Note:
General onboarding inquiry.`;

      }

    });


    function submitForm() {

      alert("Client onboarded successfully!");

    }

  </script>

</body>
</html>
