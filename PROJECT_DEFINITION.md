# Search Engagement Opportunity Scoring System

## 2. Define the Actual Decision

### Question
Which pages should the SEO team review first because they may have room to improve their search engagement?

### Decision
Decide the order in which pages are reviewed. The team can only review a limited number of pages per week (for example, about 20), so the ranking decides where their time goes.

### What "opportunity" means here
A page has possible opportunity when it gets many impressions but a lower click-through rate (CTR) than similar pages, for example pages at a similar average position. This is a working definition and I may refine it after looking at the data.

### Action
The SEO team reviews the top-ranked pages and considers possible changes to titles, descriptions, content, or search-intent alignment.

### Cost of a Wrong Call

False alarm: the team reviews a page with little real opportunity and wastes limited review time.
Missed opportunity: a page with real opportunity is ranked too low and never reviewed, so clicks may be lost.

## My lane and why
Lane: Search Engagement Opportunity Scoring System

I picked this lane because the starter data has impressions, clicks, and position for many pages, and the SEO team can't manually review all of them. A ranked list could help them decide where to look first. I can confirm or change this lane until the end of Week 4.

### Unit of analysis and output

Unit of analysis: one row = one page. (If the data is page + query, I will say so after I check the columns.)

Output: an opportunity score for each page, used to make a ranked list. A higher score means "review this page sooner." It does not mean "this page has a problem."

### Why data or ML can help
There are too many pages to check by hand, so the team needs a way to choose where to start.
A single rule like "low CTR = bad" is misleading. CTR naturally depends on position (a page at position 1 gets far more clicks than one at position 8), so a fair comparison has to account for that.
A model can learn what CTR to expect for a page at a given position, and the gap between expected and actual CTR is a sensible starting point for the score.
This is more than "train a model." The main work is defining opportunity, choosing what to compare against, and checking whether the ranking is useful to the team.
