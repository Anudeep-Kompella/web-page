<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Raw Clicks by Ram</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            text-align: center;
            background-color: white;
        }
        header {
            background: #333;
            color: white;
            padding: 20px;
            font-size: 24px;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
        }
        header img {
            height: 50px;
            width: 50px;
            border-radius: 50%;
            object-fit: cover;
        }
        .gallery {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
            justify-content: center;
            padding: 20px;
        }
        .photo-container {
            position: relative;
            background: white;
            padding: 10px;
            border-radius: 10px;
            box-shadow: 2px 2px 10px rgba(0,0,0,0.3);
        }
        .gallery img {
            width: 100%;
            max-width: 400px;
            border-radius: 10px;
            transition: transform 0.3s ease-in-out;
        }
        .gallery img:hover {
            transform: scale(1.05);
        }
        .actions {
            margin-top: 10px;
        }
        .like-btn, .comment-btn {
            padding: 5px 10px;
            margin: 5px;
            cursor: pointer;
            border: none;
            border-radius: 5px;
            font-size: 18px;
        }
        .like-btn {
            background-color: #007bff;
            color: white;
        }
        .comment-btn {
            background-color: #28a745;
            color: white;
        }
        .comment-section {
            display: none;
            margin-top: 10px;
        }
        .book-btn {
            display: block;
            margin: 20px auto;
            padding: 15px 30px;
            font-size: 18px;
            background-color: #ff4500;
            color: white;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            text-decoration: none;
        }
        .book-btn:hover {
            background-color: #cc3700;
        }
    </style>
    <script>
        function toggleLike(button) {
            if (button.classList.contains("liked")) {
                button.classList.remove("liked");
                button.innerHTML = "👍";
            } else {
                button.classList.add("liked");
                button.innerHTML = "❤️";
            }
        }

        function toggleCommentSection(button) {
            let commentSection = button.nextElementSibling;
            if (commentSection.style.display === "none" || commentSection.style.display === "") {
                commentSection.style.display = "block";
            } else {
                commentSection.style.display = "none";
            }
        }
    </script>
</head>
<body>
    <header>
        <img src="logo.jpg" alt="Logo">
        Raw Clicks <sub><i>by Ram</i></sub>
    </header>
    
    <section class="gallery">
        <div class="photo-container"><img src="RE.jpg" alt="My Photo">
            <div class="actions">
                <button class="like-btn" onclick="toggleLike(this)">👍</button>
                <button class="comment-btn" onclick="toggleCommentSection(this)">💬</button>
                <div class="comment-section">
                    <input type="text" placeholder="Add a comment...">
                </div>
            </div>
        </div>
        <div class="photo-container"><img src="PIC2.jpg" alt="My Photo">
            <div class="actions">
                <button class="like-btn" onclick="toggleLike(this)">👍</button>
                <button class="comment-btn" onclick="toggleCommentSection(this)">💬</button>
                <div class="comment-section">
                    <input type="text" placeholder="Add a comment...">
                </div>
            </div>
        </div>
        <div class="photo-container"><img src="PIC3.jpg" alt="My Photo">
            <div class="actions">
                <button class="like-btn" onclick="toggleLike(this)">👍</button>
                <button class="comment-btn" onclick="toggleCommentSection(this)">💬</button>
                <div class="comment-section">
                    <input type="text" placeholder="Add a comment...">
                </div>
            </div>
        </div>
        <div class="photo-container"><img src="PIC4.jpg" alt="My Photo">
            <div class="actions">
                <button class="like-btn" onclick="toggleLike(this)">👍</button>
                <button class="comment-btn" onclick="toggleCommentSection(this)">💬</button>
                <div class="comment-section">
                    <input type="text" placeholder="Add a comment...">
                </div>
            </div>
        </div>
    </section>
    
    <a href="#" class="book-btn">Book Your Dates</a>
    
    <section class="about">
        <h2>About</h2>
        <p>Welcome to my photography page! I love capturing beautiful moments and sharing them with the world.</p>
    </section>
    
    <section class="contact">
        <h2>Contact</h2>
        <p>Follow me on social media:</p>
        <p><a href="https://www.instagram.com/life.of_ram?igsh=emRyZG1qZDVsYnpw" target="_blank">Instagram</a> | <a href="#">Facebook</a> | <a href="#">Twitter</a></p>
    </section>
    
    <footer>
        &copy; 2025 Photography by Ram. All rights reserved.
    </footer>
</body>
</html>
