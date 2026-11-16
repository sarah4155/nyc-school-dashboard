# nyc-school-dashboard
Power BI dashboard analyzing NYC school progress reports from 2010-2011

# NYC School Performance Dashboard
A one-page Power BI dashboard that helps district leaders see where school
performance is weakest and whether it's fair to judge schools on score alone.

## The question
Where is NYC school performance weakest, and is it fair to judge schools on score alone?

## Key findings
- The districts with the lowest scores are 5,32,13,23, 19, and 9, with average scores between 36-39 (against the 45.72 Citywide average) 
- Excluding citywide districts 75 and 84, Bronx and Staten Island both have average scores below the Citywide average (45.72), with Bronx's average score being a 41.29 and Staten Island's being a 42.37. Queens has the highest average score (49.34)
- Student need doesn't exactly determine a school's score. As we see on the scatter, the trend only slightly slopes downward, and schools that have similar needs land all over the plot rather than being clustered together
- Of the 1,123 schools which were graded in both 2009-10 and 2010-11, 11 of the schools fell 3 letter grades and 3 schools rose three grades; it's important to consider these grades could be curved based, and is not necessarily indicative that a school's performance improved/declined. These would be important schools to investigate further
- There were some high-need schools that had a high performance, and are worth looking more into

## What's on the dashboard
- KPI cards: school count, average score, % graded A/B, % graded D/F
- District comparison against the citywide average
- Scatter plot of student need vs. overall score, with trend line
- Schools to watch table: schools that dropped letter grades
- Borough map and school scorecard lookup

## How I built it
- Cleaned and modeled data in Power Query (trimmed text, removed ungraded schools, derived borough from the school ID)
- Wrote DAX measures and calculated columns
- Handled the peer index, which is on different scales for middle vs. elementary schools

## Data
NYC Department of Education, 2010–11 School Progress Reports, via NYC Open Data
([link to the dataset page]).

## Limitations
This is an old dataset from 16 years ago and does not reflect the performance of NYC schools today and only presents data over the span of a year. It shows which schools are struggling the most, but not why they're struggling
Peer index is one measure of student need. This is an independent project/analysis and is not affiliated with/endorsed by NYC DOE (Department of Education).

## Is it fair to judge schools based on scores alone? 
Yes, I believe it's crucial to identify which schools need more attention. On my scatter plot, student need (DOE’s peer index) shows a gentle downward trend against overall score, and schools with similar needs fall all over the score range. Many high-need schools beat the trend. Thus, a low score isn’t just a reflection of a hard student population. But peer index is one rough measure, the data covers a single year, and a letter grade can flip on a small score change, so a low score can be used as a prompt to investigate, but not as a definitive conclusion. 

## How to open it
Open `nyc-school-dashboard.pbix` in Power BI Desktop (Windows).
