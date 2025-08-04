<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Nitesh Kumar - Portfolio</title>
  <script src="https://cdn.jsdelivr.net/npm/react@18.2.0/umd/react.development.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/react-dom@18.2.0/umd/react-dom.development.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/@babel/standalone@7.20.15/babel.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/framer-motion@10.12.16/dist/framer-motion.js"></script>
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    body {
      font-family: 'Inter', sans-serif;
      background: linear-gradient(135deg, #1e3a8a, #1e40af);
      color: #1f2937;
      margin: 0;
      padding: 0;
    }
    .section {
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      padding: 2rem;
    }
  </style>
</head>
<body>
  <div id="root"></div>
  <script type="text/babel">
    const { motion } = window.FramerMotion;

    const socialLinks = [
      { name: 'LinkedIn', url: 'https://www.linkedin.com/in/nitesh-kumar-67970125b/', icon: 'https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white' },
      { name: 'Portfolio', url: 'https://nitesh-kumar-singh-portfolio.netlify.app/', icon: 'https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=web&logoColor=white' },
      { name: 'LeetCode', url: 'https://leetcode.com/u/niteshsingh6206/', icon: 'https://img.shields.io/badge/LeetCode-FFA116?style=for-the-badge&logo=leetcode&logoColor=black' },
      { name: 'GeeksforGeeks', url: 'https://www.geeksforgeeks.org/user/niteshsimeew/', icon: 'https://img.shields.io/badge/GeeksforGeeks-308D46?style=for-the-badge&logo=geeksforgeeks&logoColor=white' },
      { name: 'Email', url: 'mailto:niteshsingh6206@gmail.com', icon: 'https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white' },
    ];

    const techStack = [
      { name: 'Java', icon: 'https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white' },
      { name: 'Spring Boot', icon: 'https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white' },
      { name: 'JavaScript', icon: 'https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black' },
      { name: 'React', icon: 'https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black' },
      { name: 'Redux', icon: 'https://img.shields.io/badge/Redux-764ABC?style=for-the-badge&logo=redux&logoColor=white' },
      { name: 'Python', icon: 'https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white' },
      { name: 'Django', icon: 'https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white' },
      { name: 'TypeScript', icon: 'https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white' },
      { name: 'MySQL', icon: 'https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white' },
      { name: 'MongoDB', icon: 'https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white' },
      { name: 'Docker', icon: 'https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white' },
      { name: 'Git', icon: 'https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white' },
      { name: 'npm', icon: 'https://img.shields.io/badge/npm-CB3837?style=for-the-badge&logo=npm&logoColor=white' },
      { name: 'Postman', icon: 'https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white' },
      { name: 'Tailwind CSS', icon: 'https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white' },
    ];

    const projects = [
      {
        name: 'Crowd-Source-Issues-Tracker',
        url: 'https://github.com/Nitesh6206/Crowd-Source-Issues-Tracker',
        description: 'A collaborative platform for tracking and managing project issues with real-time updates.',
        tech: 'Java, Spring Boot, MySQL',
      },
      {
        name: 'BookVerse-Secure-Online-Bookstore',
        url: 'https://github.com/Nitesh6206/BookVerse-Secure-Online-Bookstore',
        description: 'A secure e-commerce platform for browsing and purchasing books with payment integration.',
        tech: 'Java, Spring Boot, MySQL, React',
      },
      {
        name: 'PulseFit-Fitness-App-Backend',
        url: 'https://github.com/Nitesh6206/PulseFit-Fitness-App-Backend',
        description: 'RESTful backend for a fitness app to track workouts, nutrition, and user progress.',
        tech: 'Python, Django, MySQL',
      },
      {
        name: 'Emergency-Alert-System-Microservices',
        url: 'https://github.com/Nitesh6206/Emergency-Alert-System-Microservices',
        description: 'A microservices-based system for real-time emergency alerts and user management.',
        tech: 'JavaScript, Node.js, MongoDB, Docker',
      },
      {
        name: 'PulseFit-Fitness-App-Frontend',
        url: 'https://github.com/Nitesh6206/PulseFit-Fitness-App-Frontend',
        description: 'Responsive frontend for a fitness app with dashboards for tracking goals.',
        tech: 'JavaScript, React, Tailwind CSS, Redux',
      },
    ];

    const Header = () => (
      <motion.div
        className="section text-center text-white"
        initial={{ opacity: 0, y: -50 }}
        animate={{ opacity: 1, y: 0 }}
        transition={{ duration: 0.8 }}
      >
        <h1 className="text-4xl md:text-5xl font-bold mb-4">👋 Hey there, I'm Nitesh Kumar!</h1>
        <h3 className="text-xl md:text-2xl mb-6">Full-Stack Developer | Software Engineer | Lifelong Learner</h3>
        <div className="flex justify-center gap-4 flex-wrap">
          {socialLinks.map((link, index) => (
            <motion.a
              key={index}
              href={link.url}
              target="_blank"
              rel="noopener noreferrer"
              whileHover={{ scale: 1.1 }}
              whileTap={{ scale: 0.95 }}
            >
              <img src={link.icon} alt={link.name} className="h-8" />
            </motion.a>
          ))}
        </div>
      </motion.div>
    );

    const About = () => (
      <motion.div
        className="section bg-white/90 rounded-lg shadow-xl p-8 mx-auto max-w-4xl"
        initial={{ opacity: 0, x: -100 }}
        whileInView={{ opacity: 1, x: 0 }}
        transition={{ duration: 0.8 }}
        viewport={{ once: true }}
      >
        <h2 className="text-3xl font-bold text-center mb-6">About Me 🚀</h2>
        <p className="text-lg text-center mb-4">
          👨‍💻 I'm a passionate <strong>Software Engineer</strong> with a strong foundation in <strong>full-stack development</strong>. I specialize in building scalable, user-focused applications that solve real-world problems.
        </p>
        <p className="text-lg text-center mb-4">
          💡 My journey is fueled by a curiosity for <strong>microservices</strong>, a passion for <strong>fitness tech</strong>, and a commitment to crafting secure and efficient platforms. I'm always eager to learn new technologies and contribute to meaningful projects.
        </p>
        <p className="text-lg text-center">
          🌱 When I'm not coding, you can find me tackling LeetCode challenges or exploring new ways to turn coffee into code.
        </p>
      </motion.div>
    );

    const TechStack = () => (
      <motion.div
        className="section bg-white/90 rounded-lg shadow-xl p-8 mx-auto max-w-4xl"
        initial={{ opacity: 0, x: 100 }}
        whileInView={{ opacity: 1, x: 0 }}
        transition={{ duration: 0.8 }}
        viewport={{ once: true }}
      >
        <h2 className="text-3xl font-bold text-center mb-6">My Technical Toolkit 🛠️</h2>
        <div className="flex justify-center gap-4 flex-wrap">
          {techStack.map((tech, index) => (
            <motion.img
              key={index}
              src={tech.icon}
              alt={tech.name}
              className="h-8"
              whileHover={{ scale: 1.1 }}
              whileTap={{ scale: 0.95 }}
            />
          ))}
        </div>
      </motion.div>
    );

    const Projects = () => (
      <motion.div
        className="section bg-white/90 rounded-lg shadow-xl p-8 mx-auto max-w-5xl"
        initial={{ opacity: 0, y: 100 }}
        whileInView={{ opacity: 1, y: 0 }}
        transition={{ duration: 0.8 }}
        viewport={{ once: true }}
      >
        <h2 className="text-3xl font-bold text-center mb-6">🏆 My Projects</h2>
        <div className="overflow-x-auto">
          <table className="w-full text-left">
            <thead>
              <tr className="bg-gray-100">
                <th className="p-4 font-semibold">Name</th>
                <th className="p-4 font-semibold">Description</th>
                <th className="p-4 font-semibold">Technologies</th>
              </tr>
            </thead>
            <tbody>
              {projects.map((project, index) => (
                <motion.tr
                  key={index}
                  className="border-b hover:bg-gray-50"
                  initial={{ opacity: 0 }}
                  animate={{ opacity: 1 }}
                  transition={{ delay: index * 0.2 }}
                >
                  <td className="p-4">
                    <a href={project.url} target="_blank" rel="noopener noreferrer" className="text-blue-600 hover:underline">
                      {project.name}
                    </a>
                  </td>
                  <td className="p-4">{project.description}</td>
                  <td className="p-4">{project.tech}</td>
                </motion.tr>
              ))}
            </tbody>
          </table>
        </div>
      </motion.div>
    );

    const App = () => (
      <div>
        <Header />
        <About />
        <TechStack />
        <Projects />
      </div>
    );

    ReactDOM.render(<App />, document.getElementById('root'));
  </script>
</body>
</html>
