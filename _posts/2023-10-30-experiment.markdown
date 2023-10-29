---
layout: news
title:  "New Title"
date:   2023-10-30 11:45:44 +0000
categories: jekyll update
---

<form id="simpleCalculator">
    <label for="duration">Duration of meeting (minutes):</label>
    <input type="number" id="duration" placeholder="Enter duration">
    
    <label for="attendees">Number of attendees:</label>
    <input type="number" id="attendees" placeholder="Enter number of attendees">
    
    <label for="salary">Average hourly salary (per attendee):</label>
    <input type="number" id="salary" placeholder="Enter average hourly salary">
    
    <button type="button" onclick="calculateCost()">Calculate</button>
</form>

<p id="result"></p>

<script>
    function calculateCost() {
        var duration = parseFloat(document.getElementById("duration").value);
        var attendees = parseFloat(document.getElementById("attendees").value);
        var salary = parseFloat(document.getElementById("salary").value);
        
        // Assuming 60 minutes in an hour
        var cost = (salary / 60) * duration * attendees;
        
        document.getElementById("result").textContent = "Total meeting cost: $" + cost.toFixed(2);
    }
</script>
