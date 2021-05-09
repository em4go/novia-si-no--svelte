<script>
  export let isYes = true
  export let btnT = '400px'
  export let btnL = '400px'
  let isAbsolute = false

    function handleHover(){
        if(!isYes){
          isAbsolute = true
          const posL = Math.floor((Math.random() * (window.innerWidth - 200)))
          const posT = Math.floor(Math.random() * (window.innerHeight - 200))
          btnT = `${posT}px`
          btnL = `${posL}px`
          }}
</script>

<style>

  .isNo {
    top: var(--btn-t);
    left: var(--btn-l);
  }
</style>

<div style="--btn-t: {btnT}; --btn-l: {btnL}"
     on:mouseover={() => handleHover()}
     on:click
     class="Button hover:scale-105 border-2  rounded-lg w-36 transform {isAbsolute ? 'absolute' : ''} {!isYes ? ' isNo border-red-800 bg-red-200' : 'mb-10 bg-green-200 border-green-800 cursor-pointer mt-44'}">
  <p class="text-lg select-none">{isYes ? 'Sí' : 'No'}</p>
</div>
