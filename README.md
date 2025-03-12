
<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>काम वाली वेबसाइट</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: skyblue;
            color: black;
            margin: 0;
            padding: 0;
        }

        header {
            background-color: red;
            color: white;
            padding: 10px 20px;
            text-align: center;
        }

        header h1 {
            margin: 0;
        }

        nav ul {
            list-style-type: none;
            padding: 0;
        }

        nav ul li {
            display: inline;
            margin-right: 15px;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
        }

        section {
            padding: 20px;
            margin: 20px;
            background-color: white;
            border-radius: 8px;
        }

        .search-bar input {
            padding: 10px;
            width: 70%;
            border: 1px solid red;
            border-radius: 5px;
        }

        .search-bar button {
            padding: 10px;
            background-color: red;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        form label {
            display: block;
            margin-top: 10px;
        }

        form input {
            width: 100%;
            padding: 10px;
            margin-top: 5px;
            border: 1px solid red;
            border-radius: 5px;
        }

        form button {
            background-color: red;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            margin-top: 10px;
            cursor: pointer;
        }

        footer {
            text-align: center;
            padding: 10px;
            background-color: red;
            color: white;
            position: fixed;
            bottom: 0;
            width: 100%;
        }
    </style>
</head>
<body>
    <header>
        <h1>काम वाली वेबसाइट</h1>
        <nav>
            <ul>
                <li><a href="#home">होम</a></li>
                <li><a href="#jobs">नौकरियां</a></li>
                <li><a href="#profile">प्रोफाइल</a></li>
                <li><a href="#login">लॉगिन</a></li>
            </ul>
        </nav>
    </header>

    <section id="home">
        <h2>आपका स्वागत है!</h2>
        <p>यहां आपको सही काम और काम करने वाले मिलेंगे।</p>
    </section>

    <section id="jobs">
        <h2>नौकरियां</h2>
        <div class="search-bar">
            <input type="text" placeholder="नौकरी खोजें..." id="jobSearch">
            <button onclick="searchJobs()">खोजें</button>
        </div>
        <div id="jobResults">
            <!-- AI Job Match Results will appear here -->
        </div>
    </section>

    <section id="profile">
        <h2>प्रोफाइल</h2>
        <form id="profileForm">
            <label for="name">नाम:</label>
            <input type="text" id="name" name="name" required>
            <label for="skills">कौशल:</label>
            <input type="text" id="skills" name="skills" required>
            <label for="experience">अनुभव:</label>
            <input type="text" id="experience" name="experience" required>
            <button type="submit">सहेजें</button>
        </form>
    </section>

    <section id="login">
        <h2>लॉगिन</h2>
        <form id="loginForm">
            <label for="username">उपयोगकर्ता नाम:</label>
            <input type="text" id="username" name="username" required>
            <label for="password">पासवर्ड:</label>
            <input type="password" id="password" name="password" required>
            <button type="submit">लॉगिन</button>
        </form>
    </section>

    <footer>
        <p>&copy; 2023 काम वाली वेबसाइट</p>
    </footer>

    <script>
        // Function to handle job search
        function searchJobs() {
            const searchTerm = document.getElementById('jobSearch').value;
            const jobResults = document.getElementById('jobResults');
            // Simulate AI job matching (replace with actual AI logic)
            jobResults.innerHTML = `<p>आपकी खोज "${searchTerm}" के लिए नौकरियां:</p>
                                <ul>
                                    <li>नौकरी 1</li>
                                    <li>नौकरी 2</li>
                                    <li>नौकरी 3</li>
                                </ul>`;
        }

        // Handle profile form submission
        document.getElementById('profileForm').addEventListener('submit', function (event) {
            event.preventDefault();
            alert('प्रोफाइल सहेजी गई!');
        });

        // Handle login form submission
        document.getElementById('loginForm').addEventListener('submit', function (event) {
            event.preventDefault();
            const username = document.getElementById('username').value;
            const password = document.getElementById('password').value;
            // Simulate login (replace with actual authentication logic)
            if (username === "user" && password === "password") {
                alert('लॉगिन सफल!');
            } else {
                alert('गलत उपयोगकर्ता नाम या पासवर्ड!');
            }
        });
    </script>
</body>
</html>
