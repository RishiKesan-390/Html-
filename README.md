<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>To-Do List</title>
</head>
<body>
    <h1>My To-Do List</h1>
    <form method="POST">
        <input type="text" name="content" placeholder="Add new task">
        <input type="submit" value="Add">
    </form>
    <ul>
        {% for task in tasks %}
            <li>{{ task.content }}
                <a href="{{ url_for('delete', id=task.id) }}">Delete</a>
                <a href="{{ url_for('update', id=task.id) }}">Update</a>
            </li>
        {% endfor %}
    </ul>
</body>
</html>
