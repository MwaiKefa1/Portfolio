# Portfolio
<?php
// Database Connection
$host = "localhost";
$user = "root";
$password = "";
$database = "portfolio";
$conn = mysqli_connect($host, $user, $password, $database);
if (!$conn) {
  die("Database Connection Failed: " . mysqli_connect_error());
}
?>

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kefa Mwai - Portfolio</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; font-family: Arial, sans-serif; }
        body { background: #f4f4f4; color: #333; text-align: center; }
        header { background: #1a1a2e; color: #fff; padding: 2rem; }
        header h1 { margin-bottom: 0.5rem; }
        section { padding: 2rem; max-width: 900px; margin: auto; }
        .projects-container { display: flex; flex-wrap: wrap; justify-content: center; gap: 20px; }
        .project { background: white; padding: 1rem; border-radius: 10px; width: 280px; box-shadow: 0 0 10px rgba(0, 0, 0, 0.1); transition: transform 0.3s; }
        .project:hover { transform: scale(1.05); }
        .project a { text-decoration: none; color: #0077cc; display: inline-block; margin-top: 0.5rem; }
        footer { background: #222; color: #aaa; padding: 1rem; margin-top: 2rem; }
    </style>
</head>
<body>

    <header>
        <h1>Hi, I'm Kefa Mwai </h1>
        <p>💻 Web Developer | 🎨 Designer | 🚀 Creator</p>
    </header>

    <section id="about">
        <h2>About Me</h2>
        <p>I am a passionate developer specializing in web technologies, UI/UX, and automation.</p>
    </section>

    <section id="projects">
        <h2>Featured Projects</h2>
        <div class="projects-container">
            <?php
            $result = mysqli_query($conn, "SELECT * FROM projects ORDER BY created_at DESC LIMIT 6");
            while ($row = mysqli_fetch_assoc($result)) {
                echo "<div class='project'>";
                echo "<h3>{$row['title']}</h3>";
                echo "<p>{$row['description']}</p>";
                echo "<a href='{$row['link']}' target='_blank'>View Project</a>";
                echo "</div>";
            }
            ?>
        </div>
    </section>

    <section id="contact">
        <h2>Contact Me</h2>
        <p>Email: mwaikefa05@gmail.com| LinkedIn: linkedin.com/in/mwaikefa</p>
    </section>

    <footer>
        <p>&copy; <?php echo date('Y'); ?> Kefa Mwai | Built with 💖</p>
    </footer>

</body>
</html>
