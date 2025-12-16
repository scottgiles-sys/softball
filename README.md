<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HAWKS Softball Player Journal</title>
    <style>
        body { font-family: Arial, sans-serif; background-color: #ffffff; color: #000000; margin: 0; padding: 20px; }
        h1 { color: #000000; text-align: center; }
        h2 { color: #000000; border-bottom: 2px solid #9bddff; }
        .logo { text-align: center; margin-bottom: 20px; }
        .logo img { max-width: 250px; height: auto; }
        .quote-section { background: #9bddff; color: #000000; padding: 15px; border-radius: 8px; text-align: center; font-style: italic; margin-bottom: 30px; font-size: 1.1em; }
        section { margin-bottom: 30px; border: 1px solid #9bddff; padding: 15px; border-radius: 8px; background: #ffffff; }
        input, textarea, select { width: 100%; padding: 8px; margin: 5px 0; box-sizing: border-box; border: 1px solid #000000; border-radius: 4px; }
        button { background: #9bddff; color: #000000; padding: 10px; border: 2px solid #000000; border-radius: 4px; cursor: pointer; width: 100%; margin-top: 10px; font-weight: bold; }
        button:hover { background: #8ac9f0; }
        table { width: 100%; border-collapse: collapse; margin-top: 10px; }
        th, td { border: 1px solid #000000; padding: 8px; text-align: left; }
        th { background: #9bddff; color: #000000; }
        p { color: #000000; }
        @media (max-width: 600px) { body { padding: 10px; } section { padding: 10px; } .logo img { max-width: 180px; } }
    </style>
</head>
<body>
    <div class="logo">
        <img src="https://cdn.grok.com/xai/1736345678901234567890/edited_image_2.png" alt="HAWKS Softball Logo">
    </div>
    <h1>HAWKS Softball Player Journal</h1>
    
    <div class="quote-section" id="motivational-quote">
        Loading quote...
    </div>
    
    <p>Welcome, Hawks! Track your goals, practices, workouts, and drills. Everything saves on your device.</p>
    
    <!-- Section 1: Personal Performance Goals -->
    <section id="performance">
        <h2>1. Personal Performance Goals</h2>
        <p>Set and track your game stats like batting average or fielding errors.</p>
        <form id="performance-form">
            <label>Goal Description:</label><input type="text" id="perf-goal" placeholder="e.g., Improve batting average">
            <label>Baseline:</label><input type="text" id="perf-baseline" placeholder="e.g., .250">
            <label>Target:</label><input type="text" id="perf-target" placeholder="e.g., .300 by mid-season">
            <label>Progress:</label><textarea id="perf-progress" placeholder="e.g., Week 1: .275"></textarea>
            <label>Notes:</label><textarea id="perf-notes" placeholder="Reflections..."></textarea>
            <button type="button" onclick="addToTable('perf-table', ['perf-goal', 'perf-baseline', 'perf-target', 'perf-progress', 'perf-notes'])">Add Goal</button>
        </form>
        <table id="perf-table">
            <tr><th>Goal</th><th>Baseline</th><th>Target</th><th>Progress</th><th>Notes</th></tr>
        </table>
    </section>
    
    <!-- Section 2: Practice Routines -->
    <section id="routines">
        <h2>2. Practice Routines</h2>
        <p>Log your weekly drills and routines.</p>
        <form id="routines-form">
            <label>Date:</label><input type="date" id="routine-date">
            <label>Routine:</label><input type="text" id="routine-followed" placeholder="e.g., Hitting Focus">
            <label>Drills:</label><textarea id="routine-drills" placeholder="e.g., Tee work, soft toss"></textarea>
            <label>Challenges:</label><textarea id="routine-challenges" placeholder="e.g., Timing off"></textarea>
            <label>Adjustments:</label><textarea id="routine-adjustments" placeholder="e.g., Add more swings"></textarea>
            <button type="button" onclick="addToTable('routine-table', ['routine-date', 'routine-followed', 'routine-drills', 'routine-challenges', 'routine-adjustments'])">Add Entry</button>
        </form>
        <table id="routine-table">
            <tr><th>Date</th><th>Routine</th><th>Drills</th><th>Challenges</th><th>Adjustments</th></tr>
        </table>
    </section>
    
    <!-- Section 3: Workout Goals -->
    <section id="workouts">
        <h2>3. Workout Goals</h2>
        <p>Track strength, agility, and more tailored to softball.</p>
        <form id="workouts-form">
            <label>Type:</label><input type="text" id="workout-type" placeholder="e.g., Strength">
            <label>Goal:</label><input type="text" id="workout-goal" placeholder="e.g., Squat 150lbs">
            <label>Baseline:</label><input type="text" id="workout-baseline" placeholder="e.g., 100lbs">
            <label>Progress:</label><textarea id="workout-progress" placeholder="e.g., Week 1: 110lbs"></textarea>
            <label>Notes:</label><textarea id="workout-notes" placeholder="Reflections..."></textarea>
            <button type="button" onclick="addToTable('workout-table', ['workout-type', 'workout-goal', 'workout-baseline', 'workout-progress', 'workout-notes'])">Add Goal</button>
        </form>
        <table id="workout-table">
            <tr><th>Type</th><th>Goal</th><th>Baseline</th><th>Progress</th><th>Notes</th></tr>
        </table>
    </section>
    
    <!-- NEW Section 4: Softball-Specific Drills -->
    <section id="drills">
        <h2>4. Softball-Specific Drills</h2>
        <p>Log reps and feedback for key softball drills.</p>
        <form id="drills-form">
            <label>Date:</label><input type="date" id="drill-date">
            <label>Drill Category:</label>
            <select id="drill-category">
                <option value="Hitting">Hitting</option>
                <option value="Fielding">Fielding</option>
                <option value="Throwing">Throwing</option>
                <option value="Pitching">Pitching</option>
                <option value="Base Running">Base Running</option>
                <option value="Other">Other</option>
            </select>
            <label>Drill Name:</label><input type="text" id="drill-name" placeholder="e.g., Tee Work, Front Toss, Ground Balls">
            <label>Reps/Sets:</label><input type="text" id="drill-reps" placeholder="e.g., 50 swings, 3 sets of 10">
            <label>Focus/Notes:</label><textarea id="drill-notes" placeholder="e.g., Worked on inside pitch, footwork felt better"></textarea>
            <button type="button" onclick="addToTable('drill-table', ['drill-date', 'drill-category', 'drill-name', 'drill-reps', 'drill-notes'])">Add Drill Entry</button>
        </form>
        <table id="drill-table">
            <tr><th>Date</th><th>Category</th><th>Drill Name</th><th>Reps/Sets</th><th>Focus/Notes</th></tr>
        </table>
    </section>
    
    <button onclick="exportData()">Export Journal as JSON</button>
    <button onclick="clearData()">Clear All Data</button>

    <script>
        // Motivational Quotes Array
        const quotes = [
            "“Try not to get lost in comparing yourself to others. Discover your gifts and let them shine!” – Jennie Finch",
            "“Passion creates work ethic. Work ethic creates possibilities. Possibilities create happiness.” – Amanda Scarborough",
            "“The off-season separates the good from the great.” – Cat Osterman",
            "“Softball: Where good girls steal.” – Unknown",
            "“Play like you're in first, train like you're in second.” – Unknown",
            "“It's not about perfect. It's about effort.” – Jillian Michaels",
            "“Dream big and work hard.” – Monica Abbott",
            "“Championships are won by teams, not individuals.” – Unknown"
        ];

        // Display random quote and load data
        window.onload = function() {
            const quoteElement = document.getElementById('motivational-quote');
            const randomQuote = quotes[Math.floor(Math.random() * quotes.length)];
            quoteElement.textContent = randomQuote;
            
            loadTable('perf-table', 'performanceData');
            loadTable('routine-table', 'routinesData');
            loadTable('workout-table', 'workoutsData');
            loadTable('drill-table', 'drillsData');  // New drills data
        };

        function addToTable(tableId, inputIds) {
            const table = document.getElementById(tableId);
            const row = table.insertRow(-1);
            const data = [];
            inputIds.forEach(id => {
                const input = document.getElementById(id);
                const cell = row.insertCell();
                cell.textContent = input.value;
                data.push(input.value);
                input.value = ''; // Clear most inputs
            });
            // Don't clear the select dropdown
            document.getElementById('drill-category').selectedIndex = 0;
            saveData(tableId.replace('-table', 'Data'), data, true);
        }

        function saveData(key, newData, append = false) {
            let data = JSON.parse(localStorage.getItem(key)) || [];
            if (append) data.push(newData);
            localStorage.setItem(key, JSON.stringify(data));
        }

        function loadTable(tableId, key) {
            const table = document.getElementById(tableId);
            const data = JSON.parse(localStorage.getItem(key)) || [];
            data.forEach(rowData => {
                const row = table.insertRow(-1);
                rowData.forEach(cellData => {
                    const cell = row.insertCell();
                    cell.textContent = cellData;
                });
            });
        }

        function exportData() {
            const allData = {
                performance: JSON.parse(localStorage.getItem('performanceData')) || [],
                routines: JSON.parse(localStorage.getItem('routinesData')) || [],
                workouts: JSON.parse(localStorage.getItem('workoutsData')) || [],
                drills: JSON.parse(localStorage.getItem('drillsData')) || []  // Include drills
            };
            const blob = new Blob([JSON.stringify(allData, null, 2)], { type: 'application/json' });
            const url = URL.createObjectURL(blob);
            const a = document.createElement('a');
            a.href = url;
            a.download = 'HAWKSsoftball-journal.json';
            a.click();
        }

        function clearData() {
            if (confirm('Clear all journal data?')) {
                localStorage.clear();
                location.reload();
            }
        }
    </script>
</body>
</html>
