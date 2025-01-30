<script>
// @ts-nocheck
  import Timeline from './components/Timeline.svelte';
</script>

<main>
  <header>
    <h1>D&C Timeline</h1>
  </header>
  <Timeline />
</main>

<footer>
  <p>Created by <a href="https://github.com/uplandwave">UplandWave</a> | 2025 | Under open source license
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
    top: 10px;
    left: 10px;
    
    h1 {
      margin: 0px;
      font-size: 30px;
      /* padding: 0px; */
    }
  }
  footer {
    font-family: 'Public Sans', sans-serif;
    color: white;
    align-items: center;
    width: 100%;
    height: 25px;
    font-size: 12px;
    background: #595959;
    display: flex;
    position: fixed;
    bottom: 0;
    left: 0;
    padding: 0 1rem;

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
        right: 15px;
        color: white;
      }
    }


    
</style>