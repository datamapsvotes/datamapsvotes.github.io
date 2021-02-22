# Projects

## 2018 Victorian Election Results by Polling Booth Map

The 2018 Victorian Election Results by Polling Booth Map can be accessed [here](https://datamapsvotes.github.io/Victorian%20State%20Election%20Polling%20Place%20Map%202018/index.html).

This map was created by creating voronoi cells of polling booths for each district, cutting the voronois by their district shape (as it is fairly useless to know which Mildura polling booth is closest to Mallacoota), then colouring the map with the polling booth results after adjusting for postal votes.

### Note of caution

The map colours the Two-Candidate-Preferred results in each district electing a member to the Legislative Assembly for every polling place on the day. Comparison across districts can be inaccurate for the following reasons:

#### Each district is a different contest

The popularity of local members affects the votes cast in the legislative assembly. Comparing across district lines means you might be looking at one booth which was electing a popular member for their party and another which may have the same political composition, but as their member may be less popular, the map makes it look like these communities are different, when in reality they may vote the same had they been placed in the same district.

Further, many districts are not ALP against LIB. In Melbourne District for example, the figures shown are ALP against GRN, which means that comparing booths in Melbourne to a district that is ALP against LIB might suggest that the political composition of these areas differs markedly when in reality it changes because the two largest parties are different in different districts. An example of these differences can be found between Kensington and Newmarket booths.

As the VEC only collects two-candidate-preffered polling place data for candidates it believes will finish 1st and 2nd, the map will not show the correct contest as the necessary data is not available from the VEC. Werribee and Benambra both have incorrect two-candidate-preferred figures as independent candidates finished second in those districts.

#### Allocation of prepoll, postal, absent and other votes not cast at a polling place

All the votes that were not cast on the day had to be allocated to each of the booths in some way, as these votes are just as valid and in many seats change the outcome. How this was done was by taking the percentage of all of a party's on the day votes in the district that were cast in a particular polling booth and allocating that booth that percentage of the party/candidate's votes that were not cast on the day in the district. i.e. Say 20% of all the ALP votes cast on the day for that district were cast in some polling place, then 20% of the ALP's votes that were recorded as prepoll, absent, postal or declaration votes for that district would be allocated to that polling place.

The effect of this is that if two polling places are in different districts and are coloured differently, one may assume that they are different however because one booth might be the most supportive of its party in its district and the other booth the least supportive of the same party in its district, the two booths might have different allocations of other votes despite being politically similar.

## Senate preference distributions

The (Victorian) Senate Preference Distribution preference animation can be found [here](https://datamapsvotes.github.io/Preference%20Distribution%20Animation/index.html).

The animation attempts to demonstrate how preferences are distributed for senate elections, as well as how these preferences were distributed for the Victorian senate election in 2019.

To adapt this animation for any election, download the `index.html` file and create a csv file with the vote tally at each count for the election you wish to animate that matches the format of the `FullPrefDist.csv` file. You can usually obtain a preference count from the electoral commission that conducted the election, but it will still need to be formatted to match `FullPrefDist.csv`. (Don't worry if the electoral commission takes several counts to eliminate a candidate, the animation will handle that, and the 'ticket' column can be ignored if it isn't provided).

From there, go into `index.html` and edit the `quota` and `preCountColumns` (this one has to be either 3 or 4 depending if a 'ticket' column exists) variables to match your election. Then, scroll to the bottom and change the `FullPrefDist.csv` to the directory that your new csv file is in. Then, simply create a server for the HTML file folder and run it in a web browser.

To customise tickets (parties), simply edit the `customColours` array so the first element of the first element of the array is the ticket name as it appears in the csv file, and the second element is the colour that they should be displayed as. Add another element to the larger array for each ticket you would like to colour.

### Credits
This project was inspired by [Geoff Whale](http://www.grwpub.info/senate/index.html) and thus the svg created is released under the [Creative Commons Attribution 3.0 Australia](https://creativecommons.org/licenses/by/3.0/au/) license. The work has been significantly modified.

## District Statistics Visualisation

The Victorian Legislative Assembly District Statistics Visualisation can be found [here](https://datamapsvotes.github.io/District%20Statistics%20Visualisation/index.html#10/-37.8374/144.9962).

This visualisation demonstrates which of the 2018 Legislative Assembly Districts are above or below the average elector count. This assists in determining which low population districts the Electoral Boundaries Commission will abolish and which high population districts they may provide additional seats to.
