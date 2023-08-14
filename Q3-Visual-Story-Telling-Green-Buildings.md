Q3. Visual story telling part 1: green buildings
================

**The case**

Over the past decade, both investors and the general public have paid
increasingly close attention to the benefits of environmentally
conscious buildings. There are both ethical and economic forces at work
here. In commercial real estate, issues of eco-friendliness are
intimately tied up with ordinary decisions about how to allocate
capital. In this context, the decision to invest in eco-friendly
buildings could pay off in at least four ways.

    Every building has the obvious list of recurring costs: water, climate control, lighting, waste disposal, and so forth. Almost by definition, these costs are lower in green buildings.
    Green buildings are often associated with better indoor environments—the kind that are full of sunlight, natural materials, and various other humane touches. Such environments, in turn, might result in higher employee productivity and lower absenteeism, and might therefore be more coveted by potential tenants. The financial impact of this factor, however, is rather hard to quantify ex ante; you cannot simply ask an engineer in the same way that you could ask a question such as, “How much are these solar panels likely to save on the power bill?”
    Green buildings make for good PR. They send a signal about social responsibility and ecological awareness, and might therefore command a premium from potential tenants who want their customers to associate them with these values. It is widely believed that a good corporate image may enable a firm to charge premium prices, to hire better talent, and to attract socially conscious investors.
    Finally, sustainable buildings might have longer economically valuable lives. For one thing, they are expected to last longer, in a direct physical sense. (One of the core concepts of the green-building movement is “life-cycle analysis,” which accounts for the high front-end environmental impact of ac- quiring materials and constructing a new building in the first place.) Moreover, green buildings may also be less susceptible to market risk—in particular, the risk that energy prices will spike, driving away tenants into the arms of bolder, greener investors.

Of course, much of this is mere conjecture. At the end of the day,
tenants may or may not be willing to pay a premium for rental space in
green buildings. We can only find out by carefully examining data on the
commercial real-estate market.

The file greenbuildings.csv contains data on 7,894 commercial rental
properties from across the United States. Of these, 685 properties have
been awarded either LEED or EnergyStar certification as a green
building. You can easily find out more about these rating systems on the
web, e.g. at www.usgbc.org. The basic idea is that a commercial property
can receive a green certification if its energy efficiency, carbon
footprint, site selection, and building materials meet certain
environmental benchmarks, as certified by outside engineers.

A group of real estate economists constructed the data in the following
way. Of the 1,360 green-certified buildings listed as of December 2007
on the LEED or EnergyStar websites, current information about building
characteristics and monthly rents were available for 685 of them. In
order to provide a control population, each of these 685 buildings was
matched to a cluster of nearby commercial buildings in the CoStar
database. Each small cluster contains one green-certified building, and
all non-rated buildings within a quarter-mile radius of the certified
building. On average, each of the 685 clusters contains roughly 12
buildings, for a total of 7,894 data points.

The columns of the data set are coded as follows:

    CS.PropertyID: the building's unique identifier in the CoStar database.
    cluster: an identifier for the building cluster, with each cluster containing one green-certified building and at least one other non-green-certified building within a quarter-mile radius of the cluster center.
    size: the total square footage of available rental space in the building.
    empl.gr: the year-on-year growth rate in employment in the building's geographic region.
    Rent: the rent charged to tenants in the building, in dollars per square foot per calendar year.
    leasing.rate: a measure of occupancy; the fraction of the building's available space currently under lease.
    stories: the height of the building in stories.
    age: the age of the building in years.
    renovated: whether the building has undergone substantial renovations during its lifetime.
    class.a, class.b: indicators for two classes of building quality (the third is Class C). These are relative classifications within a specific market. Class A buildings are generally the highest-quality properties in a given market. Class B buildings are a notch down, but still of reasonable quality. Class C buildings are the least desirable properties in a given market.
    green.rating: an indicator for whether the building is either LEED- or EnergyStar-certified.
    LEED, Energystar: indicators for the two specific kinds of green certifications.
    net: an indicator as to whether the rent is quoted on a "net contract" basis. Tenants with net-rental contracts pay their own utility costs, which are otherwise included in the quoted rental price.
    amenities: an indicator of whether at least one of the following amenities is available on-site: bank, convenience store, dry cleaner, restaurant, retail shops, fitness center.
    cd.total.07: number of cooling degree days in the building's region in 2007. A degree day is a measure of demand for energy; higher values mean greater demand. Cooling degree days are measured relative to a baseline outdoor temperature, below which a building needs no cooling.
    hd.total07: number of heating degree days in the building's region in 2007. Heating degree days are also measured relative to a baseline outdoor temperature, above which a building needs no heating.
    total.dd.07: the total number of degree days (either heating or cooling) in the building's region in 2007.
    Precipitation: annual precipitation in inches in the building's geographic region.
    Gas.Costs: a measure of how much natural gas costs in the building's geographic region.
    Electricity.Costs: a measure of how much electricity costs in the building's geographic region.
    cluster.rent: a measure of average rent per square-foot per calendar year in the building's local market.

The goal

An Austin real-estate developer is interested in the possible economic
impact of “going green” in her latest project: a new 15-story mixed-use
building on East Cesar Chavez, just across I-35 from downtown. Will
investing in a green building be worth it, from an economic perspective?
The baseline construction costs are \$100 million, with a 5% expected
premium for green certification.

The developer has had someone on her staff, who’s been described to her
as a “total Excel guru from his undergrad statistics course,” run some
numbers on this data set and make a preliminary recommendation. Here’s
how this person described his process.

    I began by cleaning the data a little bit. In particular, I noticed that a handful of the buildings in the data set had very low occupancy rates (less than 10% of available space occupied). I decided to remove these buildings from consideration, on the theory that these buildings might have something weird going on with them, and could potentially distort the analysis. Once I scrubbed these low-occupancy buildings from the data set, I looked at the green buildings and non-green buildings separately. The median market rent in the non-green buildings was $25 per square foot per year, while the median market rent in the green buildings was $27.60 per square foot per year: about $2.60 more per square foot. (I used the median rather than the mean, because there were still some outliers in the data, and the median is a lot more robust to outliers.) Because our building would be 250,000 square feet, this would translate into an additional $250000 x 2.6 = $650000 of extra revenue per year if we build the green building.

    Our expected baseline construction costs are $100 million, with a 5% expected premium for green certification. Thus we should expect to spend an extra $5 million on the green building. Based on the extra revenue we would make, we would recuperate these costs in $5000000/650000 = 7.7 years. Even if our occupancy rate were only 90%, we would still recuperate the costs in a little over 8 years. Thus from year 9 onwards, we would be making an extra $650,000 per year in profit. Since the building will be earning rents for 30 years or more, it seems like a good financial move to build the green building.

The developer listened to this recommendation, understood the analysis,
and still felt unconvinced. She has therefore asked you to revisit the
report, so that she can get a second opinion.

Do you agree with the conclusions of her on-staff stats guru? If so,
point to evidence supporting his case. If not, explain specifically
where and why the analysis goes wrong, and how it can be improved. Do
you see the possibility of confounding variables for the relationship
between rent and green status? If so, provide evidence for confounding,
and see if you can also make a picture that visually shows how we might
“adjust” for such a confounder. Tell your story in pictures, with
appropriate introductory and supporting text.

Note: this is intended as an exercise in visual and numerical
story-telling. Your approach should rely on pictures and/or tables, not
a regression model. Tell a story understandable to a non-technical
audience. Keep it concise.

**Solutions:**

``` r
library(dplyr)
```

    ## 
    ## Attaching package: 'dplyr'

    ## The following objects are masked from 'package:stats':
    ## 
    ##     filter, lag

    ## The following objects are masked from 'package:base':
    ## 
    ##     intersect, setdiff, setequal, union

``` r
library(tidyr)
```

``` r
greenBuildings = read.csv("greenbuildings.csv")
```

``` r
greenBuildings$class = if_else(greenBuildings$class_a == 1, "Class A", if_else(greenBuildings$class_b == 1, "Class B", "Class C"))
```

Only 20% of green buildings are renovated compared with all the 40% of
the buildings that are present. So, it is fair to assume that green
buildings usually doesn’t require renovation

Base table:

``` r
greenBuildings %>% filter(leasing_rate >= 10) %>% 
  group_by(green_rating) %>% 
  summarise(medianRent = median(Rent), Count = n())
```

    ## # A tibble: 2 x 3
    ##   green_rating medianRent Count
    ##          <int>      <dbl> <int>
    ## 1            0       25.0  6995
    ## 2            1       27.6   684

**Although mathematically the stats guru’s analyses are accurate, they
forgot that they were making a lot of generalisation by ignoring various
factors.**

Checking for significance of renovation in green and non-green buildings
Hypothesis: Green buildings do not require renovation

``` r
greenBuildings %>% filter(leasing_rate >= 10) %>% 
  group_by(green_rating, renovated) %>% 
  summarise(Count = n()) %>% spread(key = "renovated", value = "Count") %>% 
  mutate(percentRenovated = `1`*100/(`1` + `0`))
```

    ## `summarise()` has grouped output by 'green_rating'. You can override using the
    ## `.groups` argument.

    ## # A tibble: 2 x 4
    ## # Groups:   green_rating [2]
    ##   green_rating   `0`   `1` percentRenovated
    ##          <int> <int> <int>            <dbl>
    ## 1            0  4212  2783             39.8
    ## 2            1   538   146             21.3

Although the % of renovated green buildings are half the % of non-green
buildings, 20% is still a significant amount. Thus we fail to reject the
hypothesis. We are keeping both renovated and non-renovated houses.

Building is a mixed use facility, thus amenities are assumed to be
present This increased the medianRent of green buildings slightly by
\$0.2 per sq ft.

``` r
greenBuildings %>% filter(leasing_rate >= 10, amenities == 1) %>% 
  group_by(green_rating) %>% 
  summarise(medianRent = median(Rent), Count = n())
```

    ## # A tibble: 2 x 3
    ##   green_rating medianRent Count
    ##          <int>      <dbl> <int>
    ## 1            0       25    3633
    ## 2            1       27.8   498

Checking for influence of classes in the rent of the building
Hypothesis: Higher classes will not have an effect on rent value

``` r
greenBuildings %>% filter(leasing_rate >= 10, amenities == 1) %>% 
  group_by(green_rating, class) %>% 
  summarise(medianRent = median(Rent), Count = n())
```

    ## `summarise()` has grouped output by 'green_rating'. You can override using the
    ## `.groups` argument.

    ## # A tibble: 6 x 4
    ## # Groups:   green_rating [2]
    ##   green_rating class   medianRent Count
    ##          <int> <chr>        <dbl> <int>
    ## 1            0 Class A       27.8  1997
    ## 2            0 Class B       23.9  1404
    ## 3            0 Class C       20     232
    ## 4            1 Class A       28.2   439
    ## 5            1 Class B       24.5    57
    ## 6            1 Class C       29.1     2

Reject hypothesis: Higher classes does have higher rent both in green
and non green buildings There are only 2 class C green buildings with
amenities Thus filtering out Class C from the analysis as it may not
provide us with enough samples

Since the building has 15 stories, let us constrain our analysis to only
15 floors

``` r
greenBuildings %>% filter(leasing_rate >= 10, amenities == 1, class!= "Class C", stories == 15) %>% 
  group_by(green_rating, class) %>% 
  summarise(medianRent = median(Rent), Count = n())
```

    ## `summarise()` has grouped output by 'green_rating'. You can override using the
    ## `.groups` argument.

    ## # A tibble: 4 x 4
    ## # Groups:   green_rating [2]
    ##   green_rating class   medianRent Count
    ##          <int> <chr>        <dbl> <int>
    ## 1            0 Class A       24      66
    ## 2            0 Class B       24.4    48
    ## 3            1 Class A       38.4     7
    ## 4            1 Class B       38.2     1

Although there is a significant increase in the median rent of the green
rated buildings, looking at the number of samples for green buildings
with 15 floors being only 8 records, the sample size is too small, we
will expand the filter to two stories less and more

``` r
greenBuildings %>% filter(leasing_rate >= 10, amenities == 1, class!= "Class C", stories >= 13, stories <= 17) %>% 
  group_by(green_rating, class) %>% 
  summarise(medianRent = median(Rent), Count = n())
```

    ## `summarise()` has grouped output by 'green_rating'. You can override using the
    ## `.groups` argument.

    ## # A tibble: 4 x 4
    ## # Groups:   green_rating [2]
    ##   green_rating class   medianRent Count
    ##          <int> <chr>        <dbl> <int>
    ## 1            0 Class A       28.4   226
    ## 2            0 Class B       23.4   231
    ## 3            1 Class A       28.7    60
    ## 4            1 Class B       19.6     5

We observe that the number of buildings with green rating with class B
is still only 5 Thus we are comparing only the Class A green buildings
with non green buildings in addition to the prior conditions.

``` r
greenBuildings %>% filter(leasing_rate >= 10, amenities == 1, class== "Class A", stories >= 13, stories <= 17) %>% 
  group_by(green_rating, class) %>% 
  summarise(medianRent = median(Rent), Count = n())
```

    ## `summarise()` has grouped output by 'green_rating'. You can override using the
    ## `.groups` argument.

    ## # A tibble: 2 x 4
    ## # Groups:   green_rating [2]
    ##   green_rating class   medianRent Count
    ##          <int> <chr>        <dbl> <int>
    ## 1            0 Class A       28.4   226
    ## 2            1 Class A       28.7    60

We observe that medianRent of green rated building is not significantly
higher than non green building.

Let us now see the rent split of green and non-green buildings given the
area

``` r
greenBuildings %>% filter(leasing_rate >= 10, amenities == 1, class== "Class A", stories >= 13, stories <= 17, size > 200000, size < 300000) %>% 
  group_by(green_rating, class) %>% 
  summarise(medianRent = median(Rent), Count = n())
```

    ## `summarise()` has grouped output by 'green_rating'. You can override using the
    ## `.groups` argument.

    ## # A tibble: 2 x 4
    ## # Groups:   green_rating [2]
    ##   green_rating class   medianRent Count
    ##          <int> <chr>        <dbl> <int>
    ## 1            0 Class A       32     129
    ## 2            1 Class A       30.4    30

We note that there is a -\$1.6 difference between green and non-green
building

Let us understand if the green rated buildings which we currently have,
after applying filters, are actually costlier than the non-green ones.
This can be done only by comparing buildings present within the same
clusters of the forementioned set of green buildings.

``` r
similarGreenBuilding = greenBuildings %>% 
  filter(leasing_rate >= 10, 
         amenities == 1, 
         class== "Class A", 
         stories >= 13, stories <= 17, 
         size > 200000, size < 300000, 
         green_rating ==1)

similarClusters = similarGreenBuilding$cluster

allSimilarBuildings = greenBuildings[greenBuildings$cluster %in% similarClusters,]


allSimilarBuildings %>% filter(leasing_rate >= 10, amenities == 1, class== "Class A", stories >= 13, stories <= 17, size > 200000, size < 300000) %>% 
  group_by(green_rating, class) %>% 
  summarise(medianRent = median(Rent), Count = n(), medianLeasingRate = median(leasing_rate))
```

    ## `summarise()` has grouped output by 'green_rating'. You can override using the
    ## `.groups` argument.

    ## # A tibble: 2 x 5
    ## # Groups:   green_rating [2]
    ##   green_rating class   medianRent Count medianLeasingRate
    ##          <int> <chr>        <dbl> <int>             <dbl>
    ## 1            0 Class A       34.0    10              92.1
    ## 2            1 Class A       30.4    30              92.8

**Conclusion:** Thus based on the above findings, we conclude that rent
of green buildings are actually cheaper by \$3.5 than non-green
buildings. Even the leasing rate is more or less similar. So, the return
of investment will be negative if the real estate developer invests in
the project. There were serveral confounding variables involved such
as: - Amenities - Class of building - Number of stories - Size of floor
