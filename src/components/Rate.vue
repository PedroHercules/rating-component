<template>
    <section class="text">
      <img src="../assets/img/icon-star.svg" alt="star">
      <h2>How did we do?</h2>
      <p>Please let us know how we did with your support request. All feedback is appreciated 
      to help us improve our offering!</p>
    </section>
    
    <div class="votes">
      <span class="score" @click="chooseScore(0)">1</span>
      <span class="score" @click="chooseScore(1)">2</span>
      <span class="score" @click="chooseScore(2)">3</span>
      <span class="score" @click="chooseScore(3)">4</span>
      <span class="score" @click="chooseScore(4)">5</span>
    </div>

    <button>SUBMIT</button>
</template>

<script>
  export default{
    data() {
      return {
        score: 0,
        indexScoreClicked: -1,
        scoreClicked: 0
      }
    }, 
    methods: {
      chooseScore: function (index) {
        const score = document.getElementsByClassName('score')[index];
        score.style.backgroundColor = "hsl(216, 12%, 54%)";
        score.style.color = "#fff";
        if (this.scoreClicked >= 0 && this.scoreClicked != index){
          const beforeScoreClicked = document.getElementsByClassName('score')[this.scoreClicked];
          beforeScoreClicked.style.backgroundColor = "";
          beforeScoreClicked.style.color = "";
        }
        this.scoreClicked = index;
      },

      onSubmit: function () {
        
      }
    }
  }
</script>

<style>
  h2{
    color: #fff;
  }

  .text img{
    margin-bottom: 5%;
    height: 35px;
    width: 35px;
    padding: 10px;
    border-radius: 100%;
    background: hsl(214, 18%, 25%);
  }

  .text h2{
    margin-bottom: 2%; 
  }

  .votes{
    display: flex;
    justify-content: space-between;
    margin-bottom: 2%;
    width: 100%;
    gap: 2px;
  }

  .votes .score{
    background: hsl(214, 18%, 25%);
    display: flex;
    align-items: center;
    justify-content: center;
    height: 45px;
    width: 45px;
    border-radius: 100%;  
    color: hsl(217, 12%, 63%);
    cursor: pointer;
    transition: .3s;
  }

  .votes .score:hover{
    background: hsl(25, 97%, 53%);
    color: #fff;
  }

  button{
    height: 40px;
    width: 100%;
    border-radius: 2rem;
    border: none;
    background: hsl(25, 97%, 53%);
    color: #fff;
    font-weight: 700;
    letter-spacing: 1px;
    cursor: pointer;
    transition: .3s;
  }

  button:hover{
    background: #fff;
    color: hsl(25, 97%, 53%);
  }

  
</style>