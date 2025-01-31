<script lang="ts">
  import "./css/tailwind.pcss";
  import Version from "./Components/Version.svelte";
  import InfoElectron from "./Components/InfoElectron.svelte";
  import MainWithTitlebar from "./Components/MainWithTitlebar.svelte";

  export let name: string;
  let file;
  function handleFileSelect(event) {
    const selectedFile = event.target.files[0];
    if (selectedFile) {
      file = selectedFile;
      console.log("Fichier sélectionné :", file.name);
    }
  }
</script>

<svelte:head>
  <title>MEMENTO - Svelte, TailwindCSS, Electron and TypeScript</title>
</svelte:head>

<MainWithTitlebar title="MEMENTO - Svelte + Electron">
  <section class="text-center space-y-6">
    <button onclick="">
      Create a fresh project
    </button>
  </section>
</MainWithTitlebar>

<style>
  button{
    font-weight: bolder;
    font-size: larger;
    background-color: rgb(151, 232, 159);
    border-radius: 10px;
    padding: 10px;
  }
  p {
    @apply m-1;
  }
</style>
