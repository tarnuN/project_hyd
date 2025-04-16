# Angular JSON Forms Demo App

A modern web application built using Angular 15, JSON Forms, and Tailwind CSS. The app demonstrates dynamic form generation, responsive design, and real-time validation using JSON Schema and UI Schema. It allows rendering of customizable forms directly from JSON schemas, showcasing a sleek user interface with instant validation and submission feedback.

## Core Features

- **Sleek UI** with smooth transitions and modern design
- **Fully responsive** for all screen sizes and devices
- **Real-time validation** to ensure accurate data entry
- **Instant submission feedback** to improve user experience
- **Built with Angular Material and JSON Forms** for efficient form management
- **Customizable themes** to suit different branding styles

## Requirements

- Node.js version 14 or higher
- npm version 6 or higher

## Installation & Setup

1. **Install Angular CLI globally**:

   ```bash
   npm install -g @angular/cli




git clone url


cd Assignment

npm install
ng serve  # or npm start





Running Tests
To execute unit tests:


ng test/npm start

To run end-to-end tests:


ng e2e




Data Model:

interface LoanApplicationData {
  firstName: string;  // Minimum length: 2
  lastName: string;   // Minimum length: 2
  email: string;      // Must be a valid email format
  existingCustomer: boolean;  // Whether the user is a returning customer
  customerNumber?: string;    // Required if existingCustomer is true
  loanType: string;   // Options: personal, business, mortgage, auto
  loanAmount: number; // Minimum amount: 1000
  address: {
    street: string;   // Minimum length: 5, maximum length: 100
    city: string;     // Only alphabetic characters, minimum length: 2
    state: string;    // Only alphabetic characters, minimum length: 2
    postalCode: string;  // 5-6 digit postal code
    country: string;  // Only alphabetic characters, minimum length: 2
  };
  agreeToTerms: boolean;  // Must be true to submit
}



Form Submission:

Currently simulates form submission via an API (not yet implemented).

Upon successful submission, a success message is displayed.

The form resets after successful submission to allow for new applications.

Validation:

All validation is performed client-side.

Basic email format validation is provided; more sophisticated checks are not implemented.

User Experience:

Form is responsive and adapts to both mobile and desktop environments.

Instant validation feedback is provided as users fill out the form.

No data persistence (session or local storage) is implemented.

Data Privacy:

User data is not encrypted.

No compliance with GDPR or similar data protection regulations at this time.

Form data is not stored beyond the user session.
