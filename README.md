# integrated_project_1
Practicum Integrated Project 1 - Video Game Sales

Raw Data: see moved_games.csv

**Project description**
You work for the online store Ice, which sells video games all over the world. User and expert reviews, genres, platforms (e.g. Xbox or PlayStation), and historical data on game sales are available from open sources. You need to identify patterns that determine whether a game succeeds or not. This will allow you to spot potential big winners and plan advertising campaigns.
In front of you is data going back to 2016. Let’s imagine that it’s December 2016 and you’re planning a campaign for 2017.
(The important thing is to get experience working with data. It doesn't really matter whether you're forecasting 2017 sales based on data from 2016 or 2017 sales based on data from 2016.)
The dataset contains the abbreviation ESRB. The Entertainment Software Rating Board evaluates a game's content and assigns an age rating such as Teen or Mature.

**Data Cleaning**
- What to do with NaNs? Decided to keep them rather than average, due to bias from averaging across categories
- Slimmed down to post 2000 games in post_2000_df for most analyses 
- Didn't fill in missing year_of_release, not much sales impact
- Some minor edits (i.e. game with wrong year)

**Initial Observations:**
- There are many missing critic and user scores, figure out what to do with them
- Many missing ratings as well
- Some missing years, can change data type though it's not essential

**Features:**
- Create a total sales column, regional make-up of sales
- Create an average user / critic score column
- Create separate grouped tables (by console, genre, rating) and aggregate there

**Analysis:**
- Examine impact on sales from possible factors: platform, genre, scores, rating
- Examine regional differences (are some games a hit in specific regions?)
- Determine the factors that impact sales

**Observations for Regional User Profiles**
- Japanese gamers are different in their genre preferences. While other regions the same order for top genres, RPGs rank highest in Japan and sports are less popular
- PS series were very popular everywhere (1-2 more so than 3)
- XBox 360 did not gain traction in Japan, but the DS was way more popular than in other regions
- Wii and PS3 did decently everywhere
- Racing as a genre was only in the top 5 in Europe
- Platform was only in the top 5 in Japan
- NA has the most impact on global, as it comprises the biggest portion of sales

**Actionable Insights**
- Looks like Critic Score is a very useful determinant of the success of a game, we should promote games in proportion to their Critic ratings
- Promote games that have high critic scores, let's say above the 75% percentile
Focus on the western markets:
- The Japanese market is unique in its taste of genres (favors RPGs) and platforms (low XBox series, much higher Nintendo)
- Popular Japanese games tend to not do as much in sales as popular NA and global games
- Western markets have the largest impact on sales, with North America the largest and Europe growing
