---
layout: page
title: About
permalink: /
subtitle:
nav: true
nav_order: 1
---

<style>
  .post-header {
    display: none;
  }

  /*
   * Hide the extra "About" that comes from the navbar brand.
   * Do not hide the first nav item here, otherwise the real About link
   * may also disappear.
   */
  nav.navbar .navbar-brand {
    display: none !important;
  }

  /* Make navbar links black */
  nav.navbar .navbar-nav .nav-item .nav-link,
  nav.navbar .navbar-nav .nav-item .nav-link.active,
  nav.navbar .navbar-nav .nav-item.active .nav-link,
  nav.navbar .navbar-nav .nav-link:hover,
  nav.navbar .navbar-nav .nav-link:visited {
    color: #222 !important;
  }

  .home-name {
    margin-top: 1.5rem;
    margin-bottom: 2.5rem;
    font-size: 2.8rem;
  }

  .home-top {
    display: grid;
    grid-template-columns: 330px minmax(0, 1fr);
    column-gap: 8.5rem !important;
    align-items: start;
    margin-top: 1.5rem;
    margin-bottom: 4rem;
  }

  .home-photo-box {
    width: 330px;
  }

  .home-photo {
    width: 330px;
    max-width: 100%;
    border-radius: 6px;
  }

  .home-intro {
    font-size: 1rem;
    line-height: 1.6;
    padding-top: 1rem;
    padding-left: 0 !important;
    max-width: 620px;
  }

  .home-bottom {
    display: grid;
    grid-template-columns: 1fr 1fr;
    column-gap: 8rem;
    margin-top: 2rem;
  }

  .home-section h2 {
    margin-bottom: 1rem;
  }

  @media (max-width: 900px) {
    .home-top {
      display: block;
    }

    .home-photo-box {
      margin-bottom: 2rem;
    }

    .home-intro {
      padding-left: 0 !important;
      max-width: 100%;
    }

    .home-bottom {
      display: block;
    }
  }
</style>

<h1 class="home-name">Jiangcheng You</h1>

<div class="home-top">

  <div class="home-photo-box">
    <img class="home-photo z-depth-1" src="{{ '/assets/img/tiger.jpg' | relative_url }}" alt="tiger">
  </div>

  <div class="home-intro">
    <p>
      I am a Ph.D. student in mathematics at the University of Science and Technology of China.
    </p>

    <p>
      My research focuses on Riemannian geometry and geometric relativity, Yang--Mills theory and gauge theory, and spectral geometry. I am particularly interested in geometric and analytic problems related to metrics and curvature, mathematical aspects of general relativity, and gauge-theoretic objects arising from physics, such as instantons and monopoles.
    </p>
  </div>

</div>

<div class="home-bottom">

  <div class="home-section">
    <h2>Research Interests</h2>

    <ul>
      <li>Riemannian geometry and geometric relativity</li>
      <li>Yang--Mills equation and gauge theory</li>
      <li>Spectral geometry</li>
    </ul>
  </div>

  <div class="home-section">
    <h2>Contact</h2>

    <ul>
      <li>Email: <a href="mailto:yjcmp@mail.ustc.edu.cn">yjcmp@mail.ustc.edu.cn</a>, <a href="mailto:youjiangchengmp@163.com">youjiangchengmp@163.com</a>, <a href="mailto:yjcmp27@gmail.com">yjcmp27@gmail.com</a></li>
      <li>arXiv: <a href="https://arxiv.org/search/?query=Jiangcheng+You&searchtype=author">Jiangcheng You</a></li>
      <li>ResearchGate: <a href="https://www.researchgate.net/profile/Jiangcheng-You">Jiangcheng You</a></li>
      <li>Zhihu: <a href="https://www.zhihu.com/people/you-jiang-cheng">尤江城</a></li>
      <li>Xiaohongshu: <a href="https://www.xiaohongshu.com/user/profile/6636fe6c0000000007004b38">尤江城</a></li>
    </ul>
  </div>

</div>
