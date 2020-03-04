# Median hourly nominal wage growth in the CPS-ORG

```stata tab="Stata"
* load the data
load_epiextracts, begin(1979m1) end(2019m9) sample(org) keep(wage)

* keep only wage earners
keep if wage > 0 & wage != .

* create a quarterly time variable
gen quarterdate = qofd(dofm(ym(year,month)))
format %tq quarterdate

* calculate smoothed (and classical medians)
binipolate wage [pw=orgwgt], by(quarterdate) collapsefun(gcollapse) binsize(0.25)

* create 4-quarter changes and graph the results
tsset quarterdate
gen Dwage_binned = p50_binned / L4.p50_binned - 1
scatter Dwage_binned quarterdate, connect(l) mfcolor(none)
graph export qwagegrowth.pdf, replace

```

```r tab="R"
# sample r code
mydata %>% filter(mpg <= 100)

```

