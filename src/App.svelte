<script>
  const notes = ['C', 'C#', 'D', 'D#', 'E', 'F', 'F#', 'G', 'G#', 'A', 'A#', 'B'];
  const intervals = ['unison', 'minor second', 'major second', 'minor third', 'major third', 'perfect fourth', 'augmented fourth', 'perfect fifth', 'minor sixth', 'major sixth', 'minor seventh', 'major seventh', 'octave'];
  let randomNote = '';
  let randomInterval = '';

  function generateRandomNoteAndInterval() {
    randomNote = notes[Math.floor(Math.random() * notes.length)];
    randomInterval = intervals[Math.floor(Math.random() * intervals.length)];
  }
</script>

<style>
  button {
    padding: 10px;
    font-size: 16px;
    background-color: #007aff;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }
</style>

<div>
  <button on:click={generateRandomNoteAndInterval}>Generate random note and interval</button>
  {#if randomNote && randomInterval}
    <h1>The random note is: {randomNote}</h1>
    <h2>The random interval is: {randomInterval}</h2>
  {/if}
</div>

