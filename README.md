# Corporate Office Portal - Python Flask Project

This Python - Flask project implements a corporate Office Portal, offering various tools and programs for internal company use. One of the primary tools available in this portal is a **PDF document comparison tool**. This tool compares uploaded PDF files against a master DOCX file and visually displays the differences on the web interface. Differences are highlighted in green for similarities and red for differences, allowing users to quickly identify changes between the documents. Additionally, the portal includes a **login system** to ensure secure access, with hashed passwords for authentication.

## Features

### 1. Document Comparison
- **Functionality:** Compares a user-uploaded PDF document with a master DOCX file.
- **Visual Differences:** Green highlights indicate matching content between the PDF and DOCX. Red highlights indicate differing content.
- **Supported Formats:** 
  - **Input:** `.pdf` (user-uploaded document) and `.docx` (master document).

### 2. Login System
- **Secure Authentication:** Users must log in to access the tools within the portal.
- **Password Hashing:** Passwords are securely stored using bcrypt hashing, ensuring user credentials are not stored in plain text.
- **User Sessions:** After logging in, the user's session is maintained, allowing access to the comparison tool until they log out.

### 3. Cache Control and Session Handling
- **Session Management:** The session is cleared upon logging out, and the cache is invalidated to prevent unauthorized access via browser navigation (e.g., back button).
- **No Caching:** Ensures that sensitive data is not stored or accessible after logout by disabling page caching.

### 4. Error Handling and File Validation
- **File Type Validation:** The system validates file formats before processing, ensuring that only PDF and DOCX files are allowed. Unsupported formats prompt an error message.
- **Error Feedback:** If an error occurs (e.g., missing file, incorrect format), the user is notified with a clear message via Flask's flash mechanism.

### 5. Visual and User-Friendly Interface
- **Intuitive Interface:** Designed for simplicity and ease of use, enabling employees to upload and compare documents effortlessly.
- **Responsive Design:** The interface is responsive and accessible from various devices, including desktops and mobile devices.
