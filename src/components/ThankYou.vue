<template>
  <section class="thankyou">
    <img src="../assets/img/illustration-thank-you.svg" alt="thank you">

    <span>You selected 1 out of 5</span>

    <div class="text">
      <h2>Thank you!</h2>
      <p>We appreciate you taking the time to give a rating. If you ever need more support, 
      don't hesitate to get in touch!</p>
    </div>

    <div class="attribution">
      <p>Challenge by <a href="https://www.frontendmentor.io?ref=challenge" target="_blank">Frontend Mentor</a>. 
      Coded by <a href="#">Pedro Hercules</a>.</p>
    </div>
  </section>
</template>

<style>
  .thankyou{
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 20px;
  }

  .thankyou img {
    height: 100px;
    width: 150px;
  }

  span{
    color: hsl(25, 97%, 53%);
    background: hsl(214, 18%, 25%);
    padding: 5px 20px;
    border-radius: 2rem;
    margin-bottom: 3%;
  }

  .text{
    text-align: center;
  }

  .attribution {
    text-align: center;
  }

  .attribution a{
    font-weight: 700;
    color: hsl(216, 12%, 54%);
  }
</style>