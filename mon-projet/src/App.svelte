<script>
import Question from './Question.svelte';

  let faqs = [
    {
      title: "What is Frontend Mentor, and how will it help me?",
      answer: "Frontend Mentor offers realistic coding challenges to help developers improve their frontend coding skills with projects in HTML, CSS, and JavaScript. It's suitable for all levels and ideal for portfolio building."
    },
    {
      title: "Is Frontend Mentor free?",
      answer: "Yes, Frontend Mentor offers both free and premium coding challenges, with the free option providing access to a range of projects suitable for all skill levels."
    },
    {
      title: "Can I use the projects in my portfolio?",
      answer: "Yes, you can use projects completed on Frontend Mentor in your portfolio. It's an excellent way to showcase your skills to potential employers!"
    },

    {
      title: "How can I get help if I'm stuck on a Frontend Mentor challenge?",
      answer: "The best place to get help is inside Frontend Mentor's Discord community. There's a help channel where you can ask questions and seek support from other community members."
    }
  ];

</script>


<div class="header-container"><img src="/background-pattern-desktop.svg" alt="header" class="header"></div>
  <div class="FAQ">
    <div class="title">
     <img src="/icon-star.svg" alt=""/> <h1>FAQs</h1>
    </div>
    <div class="faq-container">
  {#each faqs as question}
    <Question title={question.title} answer={question.answer} />
  {/each}
</div>
  </div>

  
  <div class="attribution">
    Challenge by <a href="https://www.frontendmentor.io?ref=challenge" target="_blank">Frontend Mentor</a>. 
    Coded by <a href="">Ludivine</a>.
  </div>


<style>

.header-container {
  position: relative; 
  width: 100%;
  height: 200px;
}

.header {
  width: 100%;
  height: 100%;
  object-fit: cover; 
  display: block; 
}

.FAQ {
    margin-top: 0;
    transform: translateY(-60px);
    background-color: white;
    display: flex;
    flex-direction: column;
    margin : auto;
    gap: 2rem;
    max-width: 700px;
    padding: 2rem;
    border-radius: 30px;
}

.title{
    display: flex;
    flex-direction: row;
    gap: 1rem;
}

h1{
    font-weight: bolder;
}


.attribution {
  align-self: flex-end;
    text-align: center;
    color:#AD28EB;
}

.attribution a{
  text-decoration: none;
  color: #AD28EB;
  font-weight: bold;
}

</style>