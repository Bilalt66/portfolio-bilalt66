<!DOCTYPE html>
<html lang="nl">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Bilal — Portfolio</title>

    <!-- Ingebedde CSS -->
    <style>
      :root {
        --bg: #ffffff;
        --header-bg: #0f1724;
        --accent: #ffffff;
      }

      html {
        scroll-behavior: smooth;
      }

      body {
        margin: 0;
        background: var(--bg);
        color: #111;
        font-family: Arial, Helvetica, sans-serif;
        font-weight: 700;
      }

      header {
        position: relative;
        padding: 15px 20px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        background: var(--header-bg);
        color: var(--accent);
        z-index: 100;
      }

      .logo {
        font-weight: bold;
      }

      /* mobiele menu knop */
      .menu-btn {
        font-size: 22px;
        background: transparent;
        color: var(--accent);
        border: 0;
        cursor: pointer;
        padding: 8px 10px;
        border-radius: 6px;
      }

      .menu-btn.open {
        background: rgba(255,255,255,0.06);
      }

      .menu {
        position: absolute;
        top: 64px;
        right: 20px;
        background: rgba(0, 0, 0, 0.85);
        padding: 15px 20px;
        border-radius: 10px;
        display: none;
        flex-direction: column;
        min-width: 160px;
        z-index: 50;
      }

      .menu a {
        color: white;
        text-decoration: none;
        margin: 8px 0;
      }

      .menu.open {
        display: flex;
      }

      /* Skills */
      .skill {
        margin: 20px 0;
      }

      .skill-name {
        display: block;
        margin-bottom: 5px;
        font-weight: bold;
      }

      .skill-bar {
        width: 100%;
        background: #ddd;
        border-radius: 20px;
        height: 25px;
        overflow: hidden;
      }

      .skill-fill {
        height: 100%;
        background: navy;
        width: 0;
        border-radius: 20px;
        transition: width 1s ease-in-out;
      }

      @media (min-width: 768px) {
        header {
          padding: 20px 40px;
        }

        .menu {
          display: flex !important;
          flex-direction: row;
          position: static;
          background: none;
          padding: 0;
        }

        .menu a {
          margin: 0 15px;
          color: var(--accent);
        }

        .menu-btn {
          display: none;
        }

        #skills .skill {
          display: flex;
          align-items: center;
          justify-content: space-between;
        }

        .skill-name {
          width: 120px;
        }

        .skill-bar {
          flex-grow: 1;
          margin-left: 20px;
        }
      }

      @media (min-width: 1024px) {
        header {
          padding: 25px 80px;
        }

        section {
          padding: 80px 60px;
        }

        .skill-name {
          width: 150px;
        }
      }

      main {
        text-align: center;
      }

      .contact-form {
        display: flex;
        flex-direction: column;
        gap: 15px;
        max-width: 600px;
      }

      .contact-form label {
        font-size: 16px;
        font-weight: 600;
        color: #333;
      }

      .contact-form input,
      .contact-form textarea {
        padding: 12px;
        font-size: 15px;
        border-radius: 6px;
        border: 1px solid #ccc;
        outline: none;
        transition: 0.2s;
      }

      .contact-form input:focus,
      .contact-form textarea:focus {
        border-color: navy;
        box-shadow: 0 0 4px #007bff55;
      }

      .contact-form button {
        width: fit-content;
        padding: 12px 20px;
        background: #007bff;
        color: white;
        border: none;
        cursor: pointer;
        border-radius: 6px;
        font-size: 16px;
        transition: 0.2s;
      }

      .contact-form button:hover {
        background: #005fcc;
      }

      .form-message {
        margin-top: 15px;
        font-size: 16px;
        font-weight: 600;
        display: none;
      }

      .form-message.success {
        color: green;
      }

      .form-message.error {
        color: red;
      }
    </style>
  </head>
  <body>
    <header>
      <div class="logo">Mijn Portfolio</div>

      <!-- menu knop toegevoegd zodat JS kan werken -->
      <button
        id="menu-btn"
        class="menu-btn"
        aria-expanded="false"
        aria-controls="menu"
        aria-label="Open menu"
      >
        ☰
      </button>

      <nav class="menu" id="menu" aria-hidden="true">
        <a href="#home">Home</a>
        <a href="#about">About Me</a>
        <a href="#skills">Skills</a>
        <a href="#projects">Projects</a>
        <a href="#contact">Contact</a>
      </nav>
    </header>

    <main>
      <h1>Hello, I am Bilal</h1>
      <p>I am a beginning Software Development student.</p>

      <section
        id="about"
        style="height: 100vh; padding: 50px; background: #ffffff"
      >
        <h2>About Me</h2>
        <p>
          Hello! My name is Bilal and I am currently studying Software
          Development. I enjoy creating websites, learning new programming
          skills.
        </p>

        <p>
          Besides coding, I also have editing skills. I create engaging content
          for social media, including TikTok, where I have experience reaching a
          large audience. This has helped me develop creativity, attention to
          detail, and an eye for design.
        </p>

        <p>
          My goal is to combine my programming and creative skills to build
          interactive and visually appealing projects. In my free time, I enjoy
          learning new tools, experimenting with designs, and improving my
          coding skills.
        </p>
      </section>

      <section
        id="skills"
        style="height: 100vh; padding: 50px; background: #ffffff"
      >
        <h2>Skills</h2>

        <div class="skill">
          <span class="skill-name">HTML</span>
          <div class="skill-bar">
            <div class="skill-fill" style="width: 50%"></div>
          </div>
        </div>

        <div class="skill">
          <span class="skill-name">CSS</span>
          <div class="skill-bar">
            <div class="skill-fill" style="width: 50%"></div>
          </div>
        </div>

        <div class="skill">
          <span class="skill-name">JavaScript</span>
          <div class="skill-bar">
            <div class="skill-fill" style="width: 25%"></div>
          </div>
        </div>

        <div class="skill">
          <span class="skill-name">Editing</span>
          <div class="skill-bar">
            <div class="skill-fill" style="width: 60%"></div>
          </div>
        </div>
      </section>

      <section
        id="projects"
        style="height: 100vh; padding: 50px; background: #ffffff"
      >
        <h2>projects</h2>
        <p>projecten</p>
      </section>

      <section
        id="contact"
        style="min-height: 100vh; padding: 50px; background: #ffffff"
      >
        <h2>Contact</h2>

        <form
          action="https://formspree.io/f/xanvgrno"
          method="POST"
          class="contact-form"
          style="max-width: 700px; margin-top: 20px"
        >
          <label for="name">Name</label><br />
          <input
            id="name"
            name="name"
            type="text"
            required
            style="width: 100%; padding: 8px; margin: 6px 0"
          />

          <label for="email">E-mail</label><br />
          <input
            id="email"
            name="email"
            type="email"
            required
            style="width: 100%; padding: 8px; margin: 6px 0"
          />
          <label for="phone-number">Phone number</label><br />
          <input
            id="phone-number"
            name="phone-number"
            type="tel"
            required
            style="width: 100%; padding: 8px; margin: 6px 0"
          />

          <label for="message">Message</label><br />
          <textarea
            id="message"
            name="message"
            rows="6"
            required
            style="width: 100%; padding: 8px; margin: 6px 0"
          ></textarea>

          <button
            type="submit"
            style="padding: 10px 16px; margin-top: 8px; cursor: pointer"
          >
            Send
          </button>
        </form>
      </section>
    </main>

    <!-- Ingebedde JavaScript -->
    <script>
      const menuBtn = document.getElementById('menu-btn');
      const menu = document.getElementById('menu');

      if (!menuBtn || !menu) {
        console.warn('menu-btn of menu niet gevonden. Controleer id\'s en dat dit script NA de HTML geladen is (of gebruik defer).');
      } else {
        function toggleMenu() {
          const isOpen = menu.classList.toggle('open');
          menuBtn.classList.toggle('open');
          menu.setAttribute('aria-hidden', (!isOpen).toString());
          menuBtn.setAttribute('aria-expanded', isOpen.toString());
        }

        menuBtn.addEventListener('click', toggleMenu);

        menu.querySelectorAll('a').forEach(a => {
          a.addEventListener('click', () => {
            menu.classList.remove('open');
            menuBtn.classList.remove('open');
            menu.setAttribute('aria-hidden', 'true');
            menuBtn.setAttribute('aria-expanded', 'false');
          });
        });

        document.addEventListener('click', (e) => {
          const target = e.target;

          if (!menu.contains(target) && !menuBtn.contains(target)) {
            menu.classList.remove('open');
            menuBtn.classList.remove('open');
            menu.setAttribute('aria-hidden', 'true');
            menuBtn.setAttribute('aria-expanded', 'false');
          }
        });


        menuBtn.addEventListener('keydown', (e) => {

          const isEnter = e.key === 'Enter' || e.code === 'Enter';
          const isSpace = e.key === ' ' || e.key === 'Spacebar' || e.code === 'Space';
          if (isEnter || isSpace) {
            e.preventDefault();
            toggleMenu();
          }
        });
      }

      // Contact formulier (Formspree)
      document.addEventListener("DOMContentLoaded", () => {
        const form = document.querySelector(".contact-form");
        const messageBox = document.createElement("div");
        messageBox.classList.add("form-message");

        if (form) {
          form.appendChild(messageBox);

          form.addEventListener("submit", async (event) => {
            event.preventDefault();

            const data = new FormData(form);

            try {
              const response = await fetch(form.action, {
                method: "POST",
                body: data,
                headers: { Accept: "application/json" }
              });

              if (response.ok) {
                messageBox.textContent = "Your message has been sent succesfully!";
                messageBox.classList.add("success");
                messageBox.classList.remove("error");
                messageBox.style.display = "block";
                form.reset();
              } else {
                messageBox.textContent = "Something went wrong, try again please!";
                messageBox.classList.add("error");
                messageBox.classList.remove("success");
                messageBox.style.display = "block";
              }
            } catch (err) {
              messageBox.textContent = "Network error: probeer het later opnieuw.";
              messageBox.classList.add("error");
              messageBox.classList.remove("success");
              messageBox.style.display = "block";
              console.error(err);
            }
          });
        }
      });
    </script>
  </body>
</html>
