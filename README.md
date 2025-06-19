# Task Scheduler

A PHP-based task management system with email notifications and subscription functionality.

## 🚀 Features

- ✅ **Task Management**: Add, complete, and delete tasks
- 📧 **Email Subscriptions**: Subscribe to receive task reminders
- 🔐 **Email Verification**: Secure email verification process
- ⏰ **Automated Reminders**: Hourly email notifications for pending tasks
- 🚫 **Easy Unsubscribe**: One-click unsubscribe functionality
- 📁 **File-based Storage**: No database required - uses JSON text files

## 🛠️ Technologies Used

- **PHP 8.3** (recommended)
- **HTML5 & CSS3**
- **JavaScript (Vanilla)**
- **JSON** for data storage
- **Cron Jobs** for automation

## 📋 Prerequisites

- XAMPP/WAMP/LAMP or any PHP server
- PHP 8.0 or higher
- Mail server configuration (for email functionality)

## 🔧 Installation & Setup

### 1. Clone the Repository
git clone https://github.com/dhyanendra-dhyani/task-scheduler.git
cd task-scheduler

### 2. Setup with XAMPP

1. Copy the project to your XAMPP htdocs directory:
C:\xampp\htdocs\task-scheduler\

2. Start XAMPP and ensure Apache is running

3. Initialize data files:

cd src
echo [] > tasks.txt
echo [] > subscribers.txt
echo {} > pending_subscriptions.txt

### 3. Access the Application

Open your browser and navigate to:

http://localhost/task-scheduler/src/

## 📁 Project Structure

task-scheduler/
├── README.md
├── .gitignore
└── src/
├── functions.php # Core application functions
├── index.php # Main user interface
├── verify.php # Email verification handler
├── unsubscribe.php # Unsubscribe functionality
├── cron.php # Automated reminder system
├── setup_cron.sh # Cron job setup script
├── tasks.txt # Task storage (JSON)
├── subscribers.txt # Verified subscribers (JSON)
└── pending_subscriptions.txt # Pending verifications (JSON)

## 🎯 How to Use

### Adding Tasks
1. Enter a task name in the input field
2. Click "Add Task"
3. Tasks appear in the list below
4. Check the checkbox to mark as complete
5. Use the delete button to remove tasks

### Email Subscriptions
1. Enter your email address
2. Click "Submit" to subscribe
3. Check your email for verification link
4. Click the verification link to confirm
5. You'll receive hourly reminders for pending tasks

## ⚙️ Cron Job Setup

To enable automated hourly reminders:
Make the script executable
chmod +x src/setup_cron.sh

Run the setup script
./src/setup_cron.sh

## 🔒 Data Storage

All data is stored in JSON format in text files:

- **tasks.txt**: Stores all tasks with ID, name, and completion status
- **subscribers.txt**: Stores verified email addresses
- **pending_subscriptions.txt**: Stores pending email verifications with codes

## 🚨 Important Notes

- Ensure your server can send emails via PHP's `mail()` function
- Data files need write permissions for the web server
- For production, configure a proper mail server
- The application uses file-based storage (no database required)

## 🐛 Troubleshooting

### White Page Issue
- Enable PHP error reporting
- Check file permissions
- Ensure Apache is running in XAMPP

### Email Not Sending
- Configure PHP mail settings
- Use MailHog for development testing
- Check server mail configuration

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 👨‍💻 Author

**Vivek Kumar**
- GitHub: [@developervivek](https://github.com/dhyanendra-dhyani)

## 🙏 Acknowledgments

- Built as part of a PHP development assignment
- Focuses on file-based data storage and email automation
- Implements modern web development practices

---

⭐ **Star this repository if you found it helpful!**


