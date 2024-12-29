# Forum Management System

Welcome to the **Forum Management System** repository! This project is a web application that allows users to create, explore, and participate in discussions on various topics.  

---

## 📹 Demo  
A full demonstration of the project is available in [this video recording](#urlOfVideo).  

---

## 🌟 Features  

- **User Authentication:** Users can register and log in securely.  
- **Topic Creation:** Users can create discussion topics.  
- **Commenting System:** Users can respond to topics with comments.  
- **Category Management:** Discussions are organized into categories for better navigation.  

---

## 🛠️ Technologies  

### **Frontend:**  
- **HTML5:** Structuring web pages.  
- **CSS3:** Styling and layouts.  
- **JavaScript:** Adding interactivity.  

### **Backend:**  
- **PHP** or **Django**: Handling server-side logic.  

### **Database:**  
- **MySQL:** Storing users, categories, topics, and comments.  

---

## 📂 Database Schema  

### **`utilisateurs` Table**  
| Field           | Type          | Description             |  
|------------------|---------------|-------------------------|  
| `ID`            | INT (PK)      | Unique identifier.      |  
| `nom`           | VARCHAR(255)  | User name.              |  
| `email`         | VARCHAR(255)  | User email.             |  
| `mot_de_passe`  | VARCHAR(255)  | Encrypted password.     |  

### **`categories` Table**  
| Field   | Type         | Description        |  
|---------|--------------|--------------------|  
| `ID`    | INT (PK)     | Unique identifier. |  
| `nom`   | VARCHAR(255) | Category name.     |  

### **`sujets` Table**  
| Field           | Type          | Description                      |  
|------------------|---------------|----------------------------------|  
| `ID`            | INT (PK)      | Unique identifier.              |  
| `utilisateur_id`| INT (FK)      | Author of the topic.            |  
| `categorie_id`  | INT (FK)      | Category of the topic.          |  
| `titre`         | VARCHAR(255)  | Title of the topic.             |  
| `contenu`       | TEXT          | Main content of the topic.      |  
| `date_creation` | DATETIME      | Date of topic creation.         |  

### **`commentaires` Table**  
| Field           | Type          | Description                      |  
|------------------|---------------|----------------------------------|  
| `ID`            | INT (PK)      | Unique identifier.              |  
| `sujet_id`      | INT (FK)      | Related topic.                  |  
| `utilisateur_id`| INT (FK)      | Author of the comment.          |  
| `contenu`       | TEXT          | Comment content.                |  
| `date`          | DATETIME      | Date of the comment.            |  

---

## 🚀 Installation  

### **Requirements:**  
- PHP (if using PHP backend) or Django (if using Django backend).  
- MySQL server.  
- A web server like Apache or Nginx.  

### **Steps to Run the Project:**  
1. Clone this repository:  
   ```bash  
   git clone https://github.com/your-username/forum-management.git  
   cd forum-management  
