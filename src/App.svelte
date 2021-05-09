<script>
  import TailwindCSS from './components/TailwindCSS.svelte'
  import Button from './components/Button.svelte'
  import Modal from './components/Modal.svelte'

  let saidYes = false


</script>

<TailwindCSS />

<div class="w-full min-h-screen p-8 text-center {saidYes ? 'bg-green-300' : 'bg-blue-200'} ">
  {#if saidYes}
    <div class="flex items-center justify-center h-80">
    <Modal />
    </div>
  {:else}
  <h1 class="mt-32 text-4xl font-bold">¿Quieres ser mi novia?</h1>
    <div class="flex flex-col-reverse items-center justify-center h-full justify-self-center">
      <Button isYes={false} btnL={'125px'} btnT={'480px'} />
      <Button on:click={() => saidYes = true} isYes={true} />
    </div>
  {/if}
</div>
