I want the application to use aggregate tables to display accurate payment and funding counts,
and enforce role-based access (Admin, Operator, Participant) using Amplify,
so that I can confidently monitor activity and ensure each user sees only what they're authorized to manage.

GIVEN
A user logs into the application

WHEN

The user accesses the Payments or Funding view

The system retrieves totals from Aggregates tables

The user is assigned one of the roles: Admin, Operator, or Participant from the Users Page

THEN

The payment and funding counts are accurate, up-to-date, and retrieved from aggregate tables

The application behavior is adjusted based on the user's role:

Admin: full access to all users and data

Operator: can manage and correct submitted data

Participant: can only view and submit their own payment/funding entries

Unauthorized actions and views are restricted at both frontend and backend (AppSync resolver) levels

