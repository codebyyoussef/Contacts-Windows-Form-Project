# Contacts Windows Forms App

A structured Windows Forms application for managing a list of contacts, built using a **3-tier architecture** to separate concerns and ensure maintainability. It supports full **CRUD operations** — users can **create**, **read**, **update**, and **delete** contact entries.

## Architecture of project
- **Presentation Layer**: Windows form with a simple design.
- **Business Logic Layer (BLL)**: Contains two classes (`clsContact`, `clsCountry`) responsible for handling contact and country data.
- **Data Access Layer (DAL)**: Contains classes to Communicates with SQL Server for data operations.

## Technologies Used
- **C#**, **SQL Server** 

## Features
- Display all contacts in a structured list
- Add new contacts
- Edit and update existing contact details
- Delete contacts with confirmation prompts
- Filter and sort contacts by various fields
- Clean separation of logic for scalability and testing

## Screenshots

### Main UI – Contact List with Filtering, Sorting and Add/Edit Contact
![Main UI](screenshots/01-MainForm.png)

### ➕ Add/Edit Contact Form – Add New Contact Details
- Fill contact info, choose image and click save to store data in database.
![Add new contact](screenshots/03-AddNewContact.png)
- As you see the new contact was added successfully.
![New contact Info](screenshots/04-RecordAddedSuccessfully.png)

### Edit or Delete
- You can edit or delete a contact by click right on specific contact.
![Add/Edit contact form](screenshots/05-EditOrDelete.png)

### ✏️ Edit Contact Form – Update Existing Contact Information(FirstName, remove image)
- You can update anything you want, I changed firstname from Yousef to Youssef and I removed the image.
![Edit Name and remove image of contact](screenshots/07-EditContact(UpdateNameandRemoveImage).png)
![Contact updated Successuflly](screenshots/07-RecordUpdatedSuccessfully.png)

## 📌 Notes
- I didin't put any validations because the goal of this project was to learn how to connect to database and retrieve, store or manipilate data.

## 🚀 How to Run
1. Download "Contacts - WinForms.rar" above, click on it and then click on view raw and the file will start downloading.
2. Download Contacts database:
   - Open SQL Server Management Studio 21
   - Click on New query and write this script: restore database ContactsDB from disk = 'DatabasePath\DatabaseName.bak' // don't forget .bak
3. On Visul studio open file explorer(ctrl + alt + L) and click on ContactsDataAccessLayer you will find a class named clsContactsDataAccessSettings
   Change connectionString with your database connection info(User ID, Password)
