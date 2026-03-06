# SwiftMail Documentation

## Overview
SwiftMail is an easy-to-use library for sending and managing emails within Swift applications. It provides a simple API to integrate email functionalities quickly and efficiently.

## Setup Instructions
1. **Installation**  
   You can install SwiftMail using CocoaPods by adding the following line to your Podfile:
   ```ruby
   pod 'SwiftMail'
   ```  
   After adding the line, run `pod install` in your terminal.

2. **Importing SwiftMail**  
   Import the library into your Swift file:
   ```swift
   import SwiftMail
   ```

3. **Configuration**  
   Set up your SMTP settings using the following code:
   ```swift
   let mailConfig = MailConfig(host: "smtp.example.com", port: 587, username: "your_email@example.com", password: "your_password")
   ```

## API Endpoints
### Sending Email
- **Endpoint**: `/send`
- **Method**: `POST`
- **Parameters**:
  - `to`: String - Recipient email address
  - `subject`: String - Subject of the email
  - `body`: String - Content of the email

- **Example Request**:
   ```swift
   let email = Email(to: "recipient@example.com", subject: "Hello!", body: "This is a test email.")
   mailService.send(email: email)  
   ```

### Fetching Emails
- **Endpoint**: `/emails`
- **Method**: `GET`

- **Example Request**:
   ```swift
   mailService.fetchEmails()  
   ```

## Architecture Overview
SwiftMail is built using the MVC architecture pattern, promoting separation of concerns. The key components include:
- **Model**: Represents the data structure for emails.
- **View**: UI components displaying the email interface.
- **Controller**: Handles business logic, interacting with models and coordinating view updates.

SwiftMail's modular approach allows for smooth integration and easy maintenance.