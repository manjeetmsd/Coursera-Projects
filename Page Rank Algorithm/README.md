# Page-Rank-Algorithm

The importance of a website is calculated on the basis of two things -- Number of incoming links to the website and number of outgoing links from the website.

We imagine a user who randomly visits websites in a micro-internet by clicking on the links present on the current website. The page rank is simply the ranking of websites most visited by the user.

First we make a rank matrix by assuming the ranks for all the pages then to calculate next iteration by multiplying the previous rank matrix by Link Matrix which contains the probability of going to next page from the current page.

We stop the process when rank matrix does not update any further by multiplication with link matrix i.e. we get the eigen value equation for the Link matrix with eigen value(lambda) equal to 1.

So basically we just have to calculate eigen vectors of Link matrix to get the value of rank matrix and then set the rank to principal eigen vector.

But what if we have a website that does not have a link or has a circular link. To counter this we introduce a damping factor which is the probabilty that to go to a new website user types the address of the new website rather clicking on the links on the website.
