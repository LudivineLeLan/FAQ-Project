<script>
  export let title;
  export let answer;

  let isOpen = false;

  function toggle() {
    isOpen = !isOpen;
  }

  function handleKey(event){
    if (event.key === "Enter"){
        event.preventDefault();
        toggle();
    }
  }
</script>

<div class="question" tabindex="0" onclick={toggle} onkeydown={handleKey}>
  <div class="question-header">
    <h2>{title}</h2>
    <img src={isOpen ? "/icon-minus.svg" : "/icon-plus.svg"} alt="toggle icon" />
  </div>

  {#if isOpen}
    <div class="answer">
      {answer}
    </div>
  {/if}
</div>

<style>

.question-header{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
}

h2:hover{
cursor: pointer;
}
</style>