# Book Library Management

## Introduction

This project comprises two main components: a front-end developed using React + React-Router + Antd, and a back-end developed using the Flask framework in Python. The application provides a comprehensive set of features for both regular users and administrators.

## Functionalities

### Regular Users

1. **Login and Registration:**

   - Users can register and log in securely.

2. **User Profile Management:**

   - Modify personal information and password.

3. **Motto Management:**

   - Publish and delete personal mottos.

4. **Book Information:**

   - Search and view book information with multi-category support.

5. **Library Interactions:**

   - View popular borrowings, collections, and newly added books.

6. **Bulletin Board:**

   - Leave messages with support for replies, text input, emojis, images, and likes.

7. **Library Transactions:**

   - Borrow and return books.

8. **Library Collections:**

   - Collect books and export information.

9. **Data Analysis:**

   - Generate user profiles/labels and analyze book data.

10. **Personalized Recommendations:**
    - Receive personalized book recommendations.

### Admin Users

In addition to regular user functionalities, administrators can:

1. **Bulletin Board Management:**

   - Pin, unpin, and delete comments on the bulletin board.

2. **Library Administration:**

   - Review information about books returned by users.
   - Add new book information with verification for new entries.
   - Edit, modify, and delete existing book information.

3. **User Management:**

   - View basic information, book preferences, and statistical analysis charts of regular users.
   - Edit basic information and delete user accounts.

4. **Statistics:**
   - View statistics of all users' collections, borrowings, and top ten rankings.

## Additional Features

1. **Security:**

   - Route protection for pages when users are not logged in.
   - Slide verification on the login page. After three login failures, the account is locked for a period.

2. **User Interface:**

   - Breadcrumb navigation functionality.
   - Rich and comprehensive prompt messages.
   - Provide a preview interface ("Browse around") to search and view book information.

3. **Library Operations:**
   - Record overdue books, impose fines, and restrict borrowing for overdue cases.

## How to Use the Project

1. **Clone the Project:**

   - Clone the project code using `git clone`.

2. **Backend Setup:**

   - Navigate to the backend folder.
   - Create a Python 3 virtual environment using `python -m venv testvenv` and activate it (`testvenv\scripts\activate`).
   - Install dependencies within the virtual environment using `pip install -r requirements.txt`.
   - Create a `.env` file in the backend directory with the specified content.

     ```bash
     DATABASE_URL=mysql+pymysql://root:123456@localhost:3306/bookms
     SQLALCHEMY_TRACK_MODIFICATIONS=False
     ```

   - Run `flask initdb` to initialize the database.
   - Run `flask build` to populate preset data.
   - Finally, run `flask run` and access the project at http://127.0.0.1:5000/.

3. **Handling Duplicate Data:**

   - If duplicate data issues occur, run `flask initdb --drop` and then run `flask build`.

4. **Default Accounts:**
   - Default admin account: "zzc"
   - Regular accounts: "mav"
   - All passwords are set to "123456"
