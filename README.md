## Features
User authentication (login, logout, register)
User profile management (view, update)
User deletion functionality (new feature)
Other features...
User Deletion Functionality

## Description
The user deletion functionality allows for the removal of user accounts from the system. This feature is implemented to be performed only after user authentication, ensuring that only recognized users can attempt to delete accounts. However, additional checks and considerations are needed to ensure robust security.

## Security Considerations
This feature includes both authentication and authorization to enhance security. Here's an analysis of why both are important:

### Authentication vs. Authorization
## Authentication:

### Definition: 
Authentication is the process of verifying the identity of a user, typically using credentials like a username and password or tokens.
### Purpose: 
It ensures that the user is who they claim to be. Once authenticated, the system knows the identity of the user making the request.

## Authorization:

### Definition: 
Authorization is the process of determining whether an authenticated user has permission to perform a specific action.
### Purpose: 
It ensures that only users with the necessary privileges can perform sensitive actions, such as deleting user accounts.

## Analysis
The requirement for the delete user functionality to be done after authentication is a partial good idea:

### Pros: 
Requiring authentication prevents unauthorized external users from deleting accounts. It ensures that only identified users can interact with the system.
### Cons: 
Authentication alone does not provide sufficient protection. Without proper authorization, any authenticated user, including those with malicious intent, could misuse the delete functionality. This could lead to data loss, security breaches, or service disruption.

## Conclusion
To fully secure the delete user functionality, both authentication and authorization are necessary:

Authentication verifies the user's identity.
Authorization ensures that only users with appropriate permissions (e.g., administrators) can delete accounts.
This layered approach protects the system's integrity and maintains user trust by ensuring that data is handled securely.

## Example Usage
Here’s how you might interact with the delete user functionality:

The user must be authenticated by logging in and providing valid credentials.
After successful authentication, the system will check the user’s role/permissions.
If the user has the required permissions (e.g., admin role), they will be allowed to delete a user account. If not, the system will deny the action.

## NB
To run cd to back-end then use node app.js on the terminal
For the frontend, install live server extension then right click index.html and open with live server
Make sure to change `http://127.0.0.1:4001/` to your API url
