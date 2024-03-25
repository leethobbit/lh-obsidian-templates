---
aliases: []
tags:
date: 2023-01-03
---
## P&L Dashboard

### Rules
- No trading after 10am
- Size Cap: 200 shares
- Stop losses MUST be set before entering a trade

### P&L - Last 7 Days
```tracker
searchType: frontmatter
searchTarget: daily_profits
folder: 00 Meta/03 Periodic/01 Daily
startDate: -1w
endDate: 0d
accum: true
line:
	title: P&L - This Week
	yAxisLabel: USD
	showPoint: false
```

### P&L - Last 30 Days
```tracker
searchType: frontmatter
searchTarget: daily_profits
folder: 00 Meta/03 Periodic/01 Daily
startDate: -1M
endDate: 0d
accum: true
line:
	title: P&L - Last 30 Days
	yAxisLabel: USD
	showPoint: false
```

### P&L - Last 90 Days
```tracker
searchType: frontmatter
searchTarget: daily_profits
folder: 00 Meta/03 Periodic/01 Daily
startDate: -3M
endDate: 0d
accum: true
line:
	title: P&L - Last 90 Days
	yAxisLabel: USD
	showPoint: false
```

### P&L - Last 365 Days
```tracker
searchType: frontmatter
searchTarget: daily_profits
folder: 00 Meta/03 Periodic/01 Daily
startDate: -1y
endDate: 0d
accum: true
line:
	title: P&L - Past Year
	yAxisLabel: USD
	showPoint: false
```


```tracker
searchType: frontmatter
searchTarget: profit_loss
folder: 00 Meta/03 Periodic/01 Daily
datasetName: P&L
month:
	startWeekOn: 'Sun'
	threshold: 1
	color: green
	dimNotInMonth: false
	headerMonthColor: green
	selectedRingColor: lightblue
	showSelectedValue: true
	circleColorByValue: false
```
### Trading - 2024
```dataviewjs
dv.span("Greener is Better!")

const hue1 = 13 //red
const hue2 = 132 //green

const calendarData = {
	intensityScaleStart: -50,
	intensityScaleEnd: 50,
	colors: {
	    red2green: [
	        `hsl(${hue1}, 100%, 37%)`,     // 1 - darkest red
	        `hsl(${hue1}, 100%, 50%)`,     // 2 - 
	        `hsl(${hue1}, 100%, 60%)`,     // 3 - 
	        `hsl(${hue1}, 100%, 77%)`,     // 4 - lightest red
	        `hsl(0, 0%, 80%)`,             // 5 - neutral gray
	        `hsl(${hue2*0.7}, 70%, 72%)`,  // 6 - lightest green
	        `hsl(${hue2*0.85}, 43%, 56%)`, // 7 - 
	        `hsl(${hue2}, 49%, 36%)`,      // 8 - 
            `hsl(${hue2}, 59%, 24%)`,      // 9 - darkest green
        ],
	},
	entries: []
}

for (let page of dv.pages("#daily-note").where(p => p['daily_profits'])){

	calendarData.entries.push({
	date: page.file.name,
	intensity: page['daily_profits'],
	content: await dv.span(`[[${page['daily_profits']}| ]]`),
	})
}

renderHeatmapCalendar(this.container, calendarData)
```


## Total Profit/Loss
```dataviewjs
dv.paragraph("### $" + dv.pages("#daily-note")
	.daily_profits.array().reduce((acc, val) => acc + val, 0).toFixed(2))
```

## Testing PNL
```dataviewjs
dv.paragraph("### $" + dv.pages("#daily-note")
	.profit_loss.array().reduce((acc, val) => acc + val).toFixed(2))
```
## Trade Journal - Last 10 Days
```dataview
TABLE
daily_profits AS "P&L",
trade_notes AS "Trading Notes"
FROM "00 Meta/03 Periodic/01 Daily"
sort file.name desc
limit 10
```

## Journal Idea
![[Pasted image 20230301100458.png]]