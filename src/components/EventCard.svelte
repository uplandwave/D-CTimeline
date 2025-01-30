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
      background: #f9f9f9;
      padding: 10px;
      border-radius: 5px;
      /* margin-top: 20px; */
      padding-left: 20px;
      padding-right: 20px;

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
      }
      h2 {
        margin-top: 3px;
      }
      img {
        max-width: 40%;
      }
    }
</style>