<template>
  <div class="container">
    <div class="content" data-aos="fade-up">
      <div class="profile-image">
        <img src="image.jpeg" alt="Profile Picture" />
      </div>
      
      <div class="intro-text">
        <h1>
          <span class="greeting">你好, 我是</span>
          <span class="name">Nightwish</span>
        </h1>
        
        <h2 class="title">前端开发工程师</h2>
        
        <p class="description">
          这里是你的个人简介。你可以描述你的专业技能、工作经验、个人兴趣等。
          让我们用简洁有力的语言，展现你的个性和专业能力。
        </p>

        <div class="skills">
          <h3>技术栈</h3>
          <div class="skill-tags">
            <span>Vue.js</span>
            <span>Svelte</span>
            <span>Node.js</span>
            <span>TypeScript</span>
            <span>Electron</span>
            <span>uniapp</span>
          </div>
        </div>

        <div class="contact">
          <a href="mailto:1140918095@qq.com" class="contact-btn">
            联系我
          </a>
        </div>
        <div class="social-links">
          <a href="https://www.zhihu.com/people/gala-37-94" target="_blank" rel="noopener noreferrer">Zhihu</a>
          <a href="https://space.bilibili.com/300863406?spm_id_from=333.1007.0.0" target="_blank" rel="noopener noreferrer">Bilibili</a>
          <a href="https://github.com/bibibala" target="_blank" rel="noopener noreferrer">GitHub</a>
          <a href="https://x.com/bababaZhao" target="_blank" rel="noopener noreferrer">Twitter</a>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
.container {
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: clamp(1rem, 5vw, 2rem);
  width: 100%;
}

.content {
  max-width: min(1200px, 90vw);
  width: 100%;
  display: flex;
  gap: clamp(2rem, 5vw, 4rem);
  align-items: center;
  padding: clamp(1.5rem, 3vw, 2.5rem);
  background: rgba(255, 255, 255, 0.05);
  border-radius: 20px;
  backdrop-filter: blur(10px);
  margin: 0 auto;
}

.profile-image {
  flex-shrink: 0;
}

.profile-image img {
  width: clamp(180px, 25vw, 280px);
  height: clamp(180px, 25vw, 280px);
  border-radius: 50%;
  object-fit: cover;
  border: 4px solid var(--primary-color);
  transition: transform 0.3s ease;
  box-shadow: 0 0 20px rgba(100, 255, 218, 0.2);
}

.profile-image img:hover {
  transform: scale(1.05);
}

.intro-text {
  flex: 1;
  min-width: 0; /* Prevent flex item from overflowing */
}

.greeting {
  font-size: clamp(1.1rem, 2vw, 1.5rem);
  color: var(--primary-color);
  display: block;
  margin-bottom: 0.5rem;
}

.name {
  font-size: clamp(2rem, 5vw, 3rem);
  font-weight: bold;
  color: var(--text-primary);
  display: block;
  margin-bottom: 0.5rem;
  line-height: 1.2;
}

.title {
  font-size: clamp(1.5rem, 3vw, 2rem);
  color: var(--text-secondary);
  margin-bottom: 1.5rem;
  line-height: 1.3;
}

.description {
  color: var(--text-secondary);
  line-height: 1.6;
  margin-bottom: 2rem;
  font-size: clamp(0.9rem, 2vw, 1.1rem);
  max-width: 600px;
}

.skills {
  margin-bottom: 2rem;
}

.skills h3 {
  color: var(--primary-color);
  margin-bottom: 1rem;
  font-size: clamp(1rem, 2vw, 1.2rem);
}

.skill-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 0.8rem;
  margin: -0.4rem;
}

.skill-tags span {
  background: rgba(100, 255, 218, 0.1);
  color: var(--primary-color);
  padding: 0.5rem 1rem;
  border-radius: 20px;
  font-size: clamp(0.8rem, 1.5vw, 0.9rem);
  transition: all 0.3s ease;
  margin: 0.4rem;
  white-space: nowrap;
}

.skill-tags span:hover {
  background: rgba(100, 255, 218, 0.2);
  transform: translateY(-2px);
}

.contact {
  margin-bottom: 2rem;
}

.contact-btn {
  display: inline-block;
  padding: clamp(0.6rem, 2vw, 0.8rem) clamp(1.5rem, 3vw, 2rem);
  background-color: transparent;
  border: 2px solid var(--primary-color);
  color: var(--primary-color);
  text-decoration: none;
  border-radius: 5px;
  transition: all 0.3s ease;
  font-size: clamp(0.9rem, 1.5vw, 1rem);
}

.contact-btn:hover {
  background-color: rgba(100, 255, 218, 0.1);
  transform: translateY(-2px);
}

.social-links {
  display: flex;
  gap: clamp(1rem, 3vw, 2rem);
  flex-wrap: wrap;
}

.social-links a {
  color: var(--text-secondary);
  text-decoration: none;
  transition: all 0.3s ease;
  font-size: clamp(0.9rem, 1.5vw, 1rem);
  position: relative;
}

.social-links a:hover {
  color: var(--primary-color);
}

.social-links a::after {
  content: '';
  position: absolute;
  width: 0;
  height: 2px;
  bottom: -4px;
  left: 0;
  background-color: var(--primary-color);
  transition: width 0.3s ease;
}

.social-links a:hover::after {
  width: 100%;
}

/* Responsive Design */
@media (max-width: 900px) {
  .content {
    gap: 2rem;
  }
}

@media (max-width: 768px) {
  .content {
    flex-direction: column;
    text-align: center;
    gap: 2rem;
    padding: 1.5rem;
  }

  .description {
    margin-left: auto;
    margin-right: auto;
  }

  .skill-tags {
    justify-content: center;
  }

  .social-links {
    justify-content: center;
  }
}

@media (max-width: 480px) {
  .container {
    padding: 1rem;
  }

  .content {
    padding: 1.2rem;
    gap: 1.5rem;
  }

  .profile-image img {
    width: 150px;
    height: 150px;
  }

  .skill-tags {
    gap: 0.5rem;
  }

  .skill-tags span {
    padding: 0.4rem 0.8rem;
  }
}

/* Dark mode optimization */
@media (prefers-color-scheme: dark) {
  .content {
    box-shadow: 0 0 30px rgba(0, 0, 0, 0.3);
  }
}
</style>
<script setup lang="ts"></script>
