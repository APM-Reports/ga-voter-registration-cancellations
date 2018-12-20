# Georgia Voter Registration Cancellations

## Estimating Cancellations Triggered by Not Voting in Georgia

In this [project](https://www.apmreports.org/story/2018/10/19/georgia-voter-purge), reporters for APM Reports wanted to find out roughly how many people in Georgia were removed from the state’s voter registration list in 2017, the last time the state performed large-scale list maintenance. More specifically, how many of those cancellations were triggered by people’s decision not to vote in previous elections? While the state keeps records on many aspects of voter registration, trying to answer this question required using multiple data sources to generate an estimate.
 
Removing ineligible voters from the rolls is a standard practice for state and local election officials. The [National Voter Registration Act](https://www.congress.gov/bill/103rd-congress/house-bill/2/text) (NVRA) of 1993 requires states to make a "reasonable effort" to remove ineligible voters from their voter registration lists. [Georgia election law](https://advance.lexis.com/documentpage/?pdmfid=1000516&crid=6a059d99-4235-457f-9448-89f9fe9924f4&nodeid=AAVAADAAHABE&nodepath=%2FROOT%2FAAV%2FAAVAAD%2FAAVAADAAH%2FAAVAADAAHABE&level=4&haschildren=&populated=false&title=%C2%A7+21-2-233.+Comparison+of+change+of+address+information+supplied+by+United+States+Postal+Service+with+electors+list%3B+removal+from+list+of+electors%3B+notice+to+electors&config=00JAA1MDBlYzczZi1lYjFlLTQxMTgtYWE3OS02YTgyOGM2NWJlMDYKAFBvZENhdGFsb2feed0oM9qoQOMCSJFX5qkd&pddocfullpath=%2Fshared%2Fdocument%2Fstatutes-legislation%2Furn%3AcontentItem%3A5STN-94M0-004D-8268-00008-00&ecomp=-kL8kkk&prid=966f9cfb-4588-4716-a582-0fe89acb8da1) requires a process similar to the one suggested by the NVRA in which the voter file is compared with change of address data from the U.S. Postal Service. If there is a match, indicating that a registered voter has moved, then local elections officials send a notice to the old address to confirm the move. If the registered voter does not respond to the notice within 30 days, that person’s registration is designated as inactive. If the person doesn't vote or make other contact with elections officials for two more federal general elections, then that person’s registration is cancelled.

However, Georgia goes beyond what’s suggested in the NVRA. The state also uses not voting as a trigger for the removal process. Election officials send notices to registered voters who haven't voted or made contact with them in the previous three years. As with the notices sent for change of address matches, if the registered voter does not respond to the notice within 30 days, then that person’s registration is placed on the inactive list. The law states that these notices should be sent in the first six months of each odd-numbered year. If the voter doesn’t vote in two more federal elections — and doesn’t make contact — then that person is removed from the voter rolls.

### APM Reports received records of registration cancellations through a public records request

From a public records request to the Georgia Secretary of State, we received records of all cancelled registrations since the 2014 general election. The reason for cancellation for each record is specified as one of these reasons:

* No Activity For 2 General Election Cycles
* Deceased
* Duplicate
* Felon
* Moved Out of State
* Voter Requested
* Hearing
* Not Verified
* Moved Out of County
* Error
* Mentally Incompetent

APM Reports focussed on the registrations that were cancelled after the 2016 general election for "No Activity For 2 General Election Cycles." The vast majority of these records showed the registration being cancelled in July 2017. Unfortunately, this data does not include a field that describes the reason why these voters were made inactive. These cancellations could have been triggered either by a match with change of address data, or by not voting. Because the Secretary of State doesn’t make this distinction in the records, we attempted to calculate roughly how many people had their cancellations triggered by not voting.

### Inactivity and eventually cancellation follows a timeline

To get an estimate of the number of people whose registration was cancelled solely for not voting or making contact, we used migration data to estimate the number of registered voters who moved out of the county. We then subtracted this number from the total number of people removed for inactivity to get an estimate of the number of the voters whose removal was triggered by simply not voting.

To determine the time ranges for data to use for this estimate, we had to consider the list maintenance timeline. Following the protocols laid out in Georgia's election law, people who had their registrations cancelled in 2017 would have had their registration set to inactive in 2013 and then skipped the general elections in 2014 and 2016.

### Turnout statistics provide a count of registered voters in 2012

Following this timeline, the last general election in which these voters would have been active would have been the 2012 general election. APM Reports used [turnout by demographics](http://sos.ga.gov/elections/TurnoutByDemographics/2012_1106/376_cfv_by_county_nov_2012.pdf) statistics for that election, which has a count of active registered voters broken down by county, race and gender. Similar statistics for other elections is also [available on the Secretary of State's website](http://sos.ga.gov/index.php/Elections/voter_turn_out_by_demographics). The totals for each county were the base of registered voters from which we calculated an estimate of the number of registrants who moved.

### Calculating a migration rate from the American Community Survey

To estimate the number of registrants who moved, we used a [table](https://censusreporter.org/tables/B07401/) from the U.S. Census Bureau's American Community Survey (ACS) that provides estimates of those living in an area one year ago and whether they stayed at their current address, moved within the county, moved within the state or moved out of state. This table also breaks out estimates by age range. We retabulated the estimates to get a total estimate for voting-aged residents of each county.

The ACS, as the name suggests, is a survey. The Census Bureau surveys a sample of residents and then uses statistical methods to generate estimates based on the sample. We had to use the five-year estimates because small geographies, like counties, do not have a large enough sample size to generate yearly estimates. This means that the migration data reflects how people surveyed moved across five years of surveys. That means that the estimates will be less accurate if a county experienced inconsistent migration across the five years. Small sample size is also the reason why we cannot calculate separate migration rates by race, even though the cancellation data has information about the registered voters' race. APM Reports used five-year estimates from 2012, the year of the last election before the list maintenance that set the registrants to inactive.

Like any survey, the ACS provides margins of error for its estimates. To make the most conservative estimate of the percentage of people who moved out of a county, we maximized the rate of movers by applying the margin of errors to calculate a rate from the largest estimate of people who moved out of the county and the smallest estimate of people living in the county one year ago. We calculated the rate of out-of-county movers because Georgia election law states that people who move within a county can’t be removed from the voter rolls. Election officials must simply update the registration records of in-county movers detected through a match with the postal service change of address database rather than initiate the verification process used for out-of-county movers. In other words, people who move within the county shouldn’t be purged from the voter list. 

APM Reports applied this out-of-county migration rate for each county to the 2012 number of active registered voters in each county to get an estimate of the number of registrants who moved. This estimate is the number of cancellations that we can attribute to moving rather than simply not voting. Complexities of migration estimates aside, this number should over-count the number of cancellations for moving, and therefore under-count the final estimate of people whose cancellation was triggered by not voting. Some of the registrants who moved will have changed their address with the postal service and responded to the subsequent notices so that their registration is transferred rather than cancelled.

The ACS is not the only source of migration data. The IRS also releases [data on migration](https://www.irs.gov/statistics/soi-tax-stats-migration-data) that provides actual counts, rather than estimates, of the number of returns and personal exemptions claimed, which approximates the number of people in a household. These numbers have the advantage of not being estimates, but only reflect those who file tax returns. We used the ACS data because we already had code to process the data and because it allowed us go get an explicit estimate for voting age people. Others may also want to try to generate estimates using the IRS migration data.

### The final estimate

APM Reports subtracted the estimate of voters who moved from the number of cancellations for inactivity in each county in 2017. That gave us an estimate of the number of people in each county whose cancellations from the rolls were triggered by not voting. 

## About the data

The registration cancellation data comes from a public records request to the Georgia Secretary of State for records of all cancelled registrations since the 2014 general election. These records include many of the same fields as the state's voter file including registration number, first and last names, county, address, race and gender. While some of the personal information is publicly available, APM reports decided to aggregate the data by county, race and reason for removal. This aggregation does not include information about individual voters, but has counts of removed registrations that we used to calculate many of the numbers published in the story. The published data also only reflects counts of cancelled registrations since the 2016 general election.
