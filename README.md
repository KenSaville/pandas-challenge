# pandas-challenge

## Heroes of Pymoli

## Introduction

This project was an assignment for MSU Bootcamp. The purpose was to explore some features of the pandas library in Python.
We were given a data set consisiting of players of a game (Heroes of Pymoli) and various stats for each player.  The stats were mainly the types and
amounts of purchases made in the game - of weapons, and other odd game items.  We analyzed these stats in various ways:  Total player count, Overall purchase analysis (number of items purchased, avg price, etc), and purchasing analysis by gender and by age.  We then calculated, sorted and displayed results for top spenders, most popular items, and most profitable items.

The basic process in most analyses was to group the data by the category of interest (gender, age) using the gropby method, perform calculations on various subsets of the data (avg price, total count, etc), and display these results by category and / or sort them. 

This was all done using jupyter notebook via jupyter lab in Anaconda.
## player counts
used .value_counts() on the names column (SN) to liste all names and number of times each was used
used len() of this to get the number of unique players (576)

## Purchasing Analysis

Here I used groupby, count(), and len(value_counts) to calculate number of unique items, avg price per item, ttotal revenue, total numer of purchases

## Gender Demographics

First removed duplicate names by sorting and using remove_duplicates
grouped unique data frame by gender
calculated avg price, count, total purchased.  All by gender

for example

gender_count = gby_gender_uniq['SN'].count()

Gender
Female                    81
Male                     484
Other / Non-Disclosed     11
Name: SN, dtype: int64

then to access specific values I used subscripts (gender_count[0] for female value, etc.)

## Gender Purchasing Analysis

Generally the same as above, but selected and analyzed data based on purchase price

## Age demographics

Here - made uniq dataframe again by sorting and removing duplicates.  Could have used the same one as a bobe, but this made it more explicit.

I then 'binned' the data based on age ranges.  To do this I used the cut function, and labeled accordingly.

Then grouped by age ranges and calculated values based on columns in the group by object.

## Purchasing Analysis by Age

Same as above, but focused on price

## Top spenders

grouped by name ('SN') didn't make it unique, as I wanted to add up all purchases for each name.
The group by function grouped the data by name, then various quantities were calculated on the appropriate column (e.g. grouped_by_name \['Price'].mean()
added values to new data frame
sorted based on total purchases

## Popular items and profitable items
 Grouped by item ID
 calculated counts and total purchases
 Made new data frame
 sorted based on counts (for popular) and total purchases (for profitable)
 
## Trends

Pymoli Trends

The three clearest trends gleaned from the pymoli data were
1.  Gender:  There was a clear gender preference, with a significant majority of players being male( 84% male, 14 % female and 2% Other/non-disclosing).
2.  Age:  A significant majority of players were between the ages of 15 and 29, with 76.74% of players falling in this range.  The single highest range was 20-24, with 44.79% in this age range.
3. Within the game, the 'Final critic' was the most purchased item (13) followed closely by 'Oathbreaker, Last hope of the Breaking storm' (12).  This was surprising, because clearly the fiery glass crusader is a much more powerful weapon.  Those depending on the Final Critic or Oathbreaker are doomed to banishment in the Icy Underworld of Pain and Suffering.







 
