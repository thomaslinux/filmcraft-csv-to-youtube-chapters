# filmcraft-csv-to-youtube-chapters
Convert FilmCraft csv markers to YouTube Chapters

# Why ?
Because I wanted to convert the exported csv markers from FilmCraft into YouTube Chapters.

Because I wanted to show what you can do with small prompts to free llms on duck.ai

# Credits
FilmCraft team (tested v0.16, very usable)

GPT-6 Luna for the logic

Gemma 4 31B for the styling

Me for some small tweaks to the final code

# Prompts
To GPT-6 Luna
```
a html page that convert this into youtube timecodes for chapters :

Sequence,Marker ID,Name,Comment,Kind,Color,Start Timecode,End Timecode,Duration Frames,Start Ticks,Duration Ticks,Frame Rate,Author,URL
"Sequence 01","414","intro","","Chapter","Ambience","00:00:00:00","00:00:00:00","0","0","0","60/1","",""
"Sequence 01","415","Create a new Instance","","Chapter","Ambience","00:00:07:25","00:00:07:25","0","1883952000000","0","60/1","",""
[...]
```

To Gemma 4 31B ended inside ``<style class="css-file-picker"></style>``
```
  <div class="file-picker">
    <label for="csvFile">Import CSV file:
    <input id="csvFile" type="file" accept=".csv,text/csv">
	</label>
  </div>

simple css code for modern styling
```

To Gemma 4 31B ended inside ``<style class="modern"></style>``
```
<h1>FilmCraft csv markers to YouTube Chapter</h1>
  <p>Import a CSV file or paste CSV content below. The converter uses the following columns</p>
    <code>Name ; Start Timecode ; Frame Rate</code>

  <div class="file-picker">
    <label for="csvFile">Import CSV file:
    <input id="csvFile" type="file" accept=".csv,text/csv">
	</label>
  </div>

  <label for="input">Or paste CSV content:</label>
  <textarea id="input" placeholder="Paste your CSV content here"></textarea>

  <button id="convert">Convert to YouTube chapters</button>
  <button id="copy" type="button">Copy output</button>
  <span id="status" role="status"></span>

  <label for="output">YouTube chapters:</label>
  <textarea id="output" readonly placeholder="Converted chapters will appear here"></textarea>
simple css code for modern styling
```
