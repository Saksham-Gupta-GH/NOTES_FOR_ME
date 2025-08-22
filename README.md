# 📒 Personal Knowledge Hub

A simple, lightweight personal note-taking application built with Flask and SQLite - your own mini OneNote clone! Perfect for organizing thoughts, ideas, and knowledge without the complexity of JavaScript.

## ✨ Features

- **📝 Create Notes**: Add notes with titles, content, and tags
- **✏️ Edit & Delete**: Full CRUD operations for your notes
- **🔍 Search**: Search through titles, content, and tags
- **🏷️ Tags**: Organize notes with comma-separated tags
- **📅 Timestamps**: Automatic date tracking for all notes
- **💻 Clean UI**: Responsive design with HTML + CSS only
- **🗄️ SQLite Storage**: Lightweight local database
- **⚡ No JavaScript**: Simple and fast with server-side rendering

## 🏗️ Project Structure

```
personal_knowledge_hub/
│
├── app.py                # Flask backend application
├── notes.db              # SQLite database (auto-created)
├── README.md             # This file
│
├── static/
│   └── style.css         # CSS styling
│
└── templates/
    ├── base.html         # Common layout template
    ├── index.html        # Homepage showing all notes
    ├── add_note.html     # Form to add new notes
    ├── edit_note.html    # Edit existing notes
    └── search.html       # Search functionality
```

## 🚀 Quick Start

### Prerequisites

- Python 3.6 or higher
- pip (Python package installer)

### Installation

1. **Clone or download the project**
   ```bash
   git clone <your-repo-url>
   cd personal_knowledge_hub
   ```

2. **Install Flask**
   ```bash
   pip install flask
   ```
   > SQLite comes pre-installed with Python

3. **Run the application**
   ```bash
   python app.py
   ```

4. **Open in your browser**
   ```
   http://127.0.0.1:5000
   ```

That's it! Your Personal Knowledge Hub is now running locally.

## 🎯 How to Use

### Adding Notes
1. Click "Add Note" in the navigation
2. Enter a title for your note
3. Write your content in the text area
4. Add tags (comma-separated) for better organization
5. Click "Save Note"

### Managing Notes
- **View All**: The homepage shows all your notes in chronological order
- **Edit**: Click the "✏ Edit" link on any note
- **Delete**: Click the "🗑 Delete" link to remove a note
- **Search**: Use the search function to find notes by title, content, or tags

### Search Tips
- Search works across titles, content, and tags
- Partial matches are supported
- Case-insensitive searching

## 🗄️ Database Schema

The SQLite database (`notes.db`) contains a single table:

```sql
CREATE TABLE notes (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    title TEXT NOT NULL,
    content TEXT NOT NULL,
    tags TEXT,
    date TEXT
);
```

## 🎨 Customization

### Styling
Modify `static/style.css` to change:
- Color scheme
- Fonts and typography
- Layout and spacing
- Button styles

### Features
The modular Flask structure makes it easy to add:
- Categories/folders
- Rich text formatting
- File attachments
- Export functionality
- User authentication

## 📝 Example Usage

```
Title: "Python Flask Tutorial Notes"
Content: "Flask is a lightweight web framework..."
Tags: "python, web development, flask"
```

## 🔧 Configuration

### Development Mode
The app runs in debug mode by default. For production, modify:

```python
if __name__ == "__main__":
    app.run(debug=False, host='0.0.0.0', port=5000)
```

### Database Location
By default, the SQLite database is created in the project root. To change the location, modify the connection string in `app.py`:

```python
conn = sqlite3.connect("/path/to/your/notes.db")
```

## 🚧 Limitations

- **No JavaScript**: Intentionally simple - no rich text editor or dynamic features
- **Single User**: No authentication system (suitable for personal use)
- **Local Only**: Runs on localhost (can be deployed to a server)
- **Basic Search**: Simple text matching (no advanced search operators)

## 🌟 Future Enhancements

Potential improvements you could add:
- [ ] Markdown support for rich text
- [ ] Note categories/folders
- [ ] Export to PDF/HTML
- [ ] Import from other note apps
- [ ] Dark mode toggle
- [ ] Note templates
- [ ] Backup/restore functionality

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🤝 Contributing

This is a simple educational project, but contributions are welcome:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 🆘 Troubleshooting

### Common Issues

**Database not found error:**
- The SQLite database is created automatically on first run
- Ensure you have write permissions in the project directory

**Flask not found:**
- Install Flask: `pip install flask`
- Check your Python environment

**Port already in use:**
- Change the port in `app.py`: `app.run(port=5001)`
- Or stop other applications using port 5000

**CSS not loading:**
- Ensure the `static` folder structure is correct
- Check browser console for 404 errors

## 📞 Support

For issues or questions:
1. Check the troubleshooting section above
2. Review the code comments in `app.py`
3. Create an issue in the repository

---

**Happy note-taking! 📝✨**
