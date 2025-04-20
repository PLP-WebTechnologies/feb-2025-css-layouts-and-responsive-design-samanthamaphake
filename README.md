<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Responsive Layout</title>

</head>
<body>

  <nav>
    <div class="logo">MySite</div>
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Services</a></li>
      <li><a href="#">Contact</a></li>
    </ul>
  </nav>

  <div class="container">
    <div class="sidebar">Sidebar Content</div>
    <div class="main-content">Main Content Area</div>
    <div class="extra-content">Extra Content (visible on wide screens)</div>
  </div>

</body>
</html>

*{
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
}

nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: #333;
    padding: 1rem;
    color: white;
}

nav .logo {
    font-size: 1.5rem;
}

nav ul {
    display: flex;
    list-style: none;
    gap: 1rem;
}

nav ul li a {
    color: white;
    text-decoration: none;
}

.container {
    display: grid;
    grid-template-columns: 1fr 3fr;
    gap: 1rem;
    padding: 1rem;
}

.sidebar {
    background-color: #f4f4f4;
    padding: 1rem;
}

.main-content {
    background-color: #eaeaea;
    padding: 1rem;
}

@media (max-width: 768px) {
    .container {
      grid-template-columns: 1fr;
    }

nav {
      flex-direction: column;
      align-items: flex-start;
    }

nav ul {
      flex-direction: column;
      width: 100%;
      gap: 0.5rem;
    }
}

@media (min-width: 1200px) {
    .container {
      grid-template-columns: 1fr 2fr 1fr;
    }

.extra-content {
      background-color: #d1d1d1;
      padding: 1rem;
    }
}
