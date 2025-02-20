<script>
    export let selectedEvent;
</script>
  
<div class="event-card">
    <h3 class="eventDate">{selectedEvent.date}</h3>
    <hr>
    <h2>{selectedEvent.title}</h2>
    <p>{selectedEvent.description}</p>
    <img src={selectedEvent.image} alt={selectedEvent.title}>
    <h3>Read more in D&C Sections</h3>
    <ul>
        {#each selectedEvent.sections as section}
        <li>{section}</li>
        {/each}
    </ul>
</div>
  
<style>
    .event-card {
      background: #efefe7;
      background: #f8f0e4;
      padding: 10px;
      border-radius: 5px;
      padding-left: 20px;
      padding-right: 20px;
      color: #003057;

      h3 {
        text-align: left;
        margin-bottom: 0px;
        margin-top: 3px;
      }
      ul {
        text-align: left;
        margin-top: 5px;
      }
      .eventDate {
        text-align: center;
        font-size: 36px;
      }
      h2 {
        margin-top: 3px;
      }
      img {
        max-width: 500px;
      }
      hr {
        height: 1px;
        background-color: #01b6d1;
        border:none
      }
    }
</style>