<script>
// @ts-nocheck
    import { onMount } from 'svelte';
    import events from '../data/events.js';
    import EventCard from './EventCard.svelte';
    
    let selectedEvent = null;
  
    function selectEvent(event) {
      selectedEvent = event;
    }
  </script>

  <div class="infoBox">
    {#if selectedEvent}
      <EventCard {selectedEvent} />
    {:else}
        <h2>Click a bubble on the timeline!</h2>
    {/if}
  </div>
  <div class="timeline-container">
    <div class="timeline">
      {#each events as event}
        <!-- svelte-ignore a11y_no_static_element_interactions -->
        <!-- svelte-ignore a11y_mouse_events_have_key_events -->
        <div class="timeline-stop" on:mouseover={() => selectEvent(event)}>
          <span class="tooltip">{event.date}</span>
        </div>
      {/each}
    </div>
  </div>
  
  <style>
    .timeline-container {
      position: absolute;
      bottom: 35px;
      left: 50%;
      transform: translateX(-50%);
      display: flex;
      flex-direction: column;
      align-items: center;
    }
    .timeline {
      display: flex;
      gap: 30px;
      background: white;
      padding: 10px;
      border-radius: 5px;
      margin-top: 20px;
    }
    .timeline-stop {
      cursor: pointer;
      width: 10px;
      height: 10px;
      padding: 1px;
      background: #ddd;
      border-radius: 50%;
      position: relative;
    }
    .timeline-stop:hover .tooltip {
      display: block;
    }
    .timeline-stop:hover {
      background: #faa61a;
    }
    .tooltip {
      display: none;
      position: absolute;
      bottom: 20px;
      background: #006184;
      color: #01b6d1;
      color: #faa61a;
      padding: 5px;
      border-radius: 3px;
      white-space: nowrap;
    }
    h2 {
      color: #003057;
    }
  </style>