<script>
// @ts-nocheck
  import Timeline from './components/Timeline.svelte';
</script>

<main>
  <header>
    <h1><a href="/D-CTimeline/">D&C Timeline</a></h1>
  </header>
  <Timeline />
</main>

<footer>
  <p><a href="https://github.com/uplandwave">Created by UplandWave</a> | 2025 | Under open source license
  <p class="right"><a href="https://github.com/uplandwave/D-CTimeline">Repo</a></p>
</footer>

<style>
  main {
    display: block;
    font-family: 'Public Sans', sans-serif;
    text-align: center;
    /* padding: 20px; */
    /* position: relative; */
  }
  header {
    font-family: 'Public Sans', sans-serif;
    position: absolute;
    top: 20px;
    left: 20px;
    /* margin: 5px; */
    padding: 5px;
    background-color: #006184;
    
    h1 {
      margin: 0px;
      font-size: 35px;
      color: #003057;
      color: #f8f0e4;
      color: #b0eefc;
      color: #01b6d1;
      /* padding: 0px; */
    }
      a {
          text-decoration: none;
          color: #01b6d1;
        }
  }
  footer {
    font-family: 'Public Sans', sans-serif;
    color: white;
    align-items: center;
    width: 100%;
    height: 25px;
    font-size: 12px;
    background: #003057;
    display: flex;
    position: fixed;
    bottom: 0;
    left: 0;
    padding: 0 .5rem;

      p {
        margin: 0;
      }
      a {
        text-decoration: none;
        color: white;
      }
      a:hover {
        text-decoration: underline;
      }
      .right {
        position: absolute;
        padding-right: 30px;
        right: -2px;
        color: white;
      }
    }


    
</style>