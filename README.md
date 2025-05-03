# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
Make the webpage responsive using media queries.
Ensure proper alignment and spacing.

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.

Happy Coding! 💻✨


<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Responsive Layout Example</title>
  <style>
    :root {
      --primary-color: #3498db;
      --secondary-color: #2c3e50;
      --light-color: #ecf0f1;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: Arial, sans-serif;
      background-color: var(--light-color);
      color: var(--secondary-color);
    }

    /* Grid Layout */
    .container {
      display: grid;
      grid-template-areas:
        "header"
        "nav"
        "main"
        "sidebar"
        "footer";
      grid-template-columns: 1fr;
      grid-gap: 10px;
      padding: 10px;
    }

    header {
      grid-area: header;
      background: var(--primary-color);
      color: white;
      padding: 1rem;
      text-align: center;
    }

    nav {
      grid-area: nav;
      background: white;
      display: flex;
      justify-content: space-around;
      padding: 1rem;
      border-radius: 5px;
    }

    nav a {
      color: var(--secondary-color);
      text-decoration: none;
      font-weight: bold;
    }

    main {
      grid-area: main;
      background: white;
      padding: 1rem;
      border-radius: 5px;
    }

    .cards {
      display: flex;
      flex-wrap: wrap;
      gap: 1rem;
      margin-top: 1rem;
    }

    .card {
      background: var(--primary-color);
      color: white;
      flex: 1 1 calc(33.333% - 1rem);
      padding: 1rem;
      border-radius: 8px;
      min-width: 200px;
    }

    aside {
      grid-area: sidebar;
      background: white;
      padding: 1rem;
      border-radius: 5px;
    }

    footer {
      grid-area: footer;
      background: var(--secondary-color);
      color: white;
      text-align: center;
      padding: 1rem;
      border-radius: 5px;
    }

    /* Responsive Layout */
    @media (min-width: 768px) {
      .container {
        grid-template-areas:
          "header header"
          "nav nav"
          "main sidebar"
          "footer footer";
        grid-template-columns: 2fr 1fr;
      }
    }

    @media (min-width: 1024px) {
      .cards {
        flex-wrap: nowrap;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <header>
      <h1>My Responsive Website</h1>
    </header>

    <nav>
      <a href="#">Home</a>
      <a href="#">About</a>
      <a href="#">Services</a>
      <a href="#">Contact</a>
    </nav>

    <main>
      <h2>Welcome</h2>
      <p>This page uses Grid and Flexbox to be responsive and beautiful on all screens.</p>

      <div class="cards">
        <div class="card">Card 1</div>
        <div class="card">Card 2</div>
        <div class="card">Card 3</div>
      </div>
    </main>

    <aside>
      <h3>Sidebar</h3>
      <p>Here is a sidebar with more info.</p>
    </aside>

    <footer>
      <p>&copy; 2025 Responsive Website</p>
    </footer>
  </div>
</body>
</html>

