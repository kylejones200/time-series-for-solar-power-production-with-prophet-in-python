# Time series for solar power production with Prophet in Python

This simple project takes cumulative power production data from solar panels and predicts future generation. I use a tool from Facebook...

### Time series for solar power production with Prophet in Python
This simple project takes cumulative power production data from solar panels and predicts future generation. I use a tool from Facebook called Prophet which is a Bayesian time series approach.

We start by importing the modules and data.


I am using a simple way of plotting because the data is simple. If the data has more columns then `df.plot()` is probably not the right answer.


We see that production increases over time and has seasonal "waves" based on the intensity of the solar.


Adding the forecast (blue line) and range of uncertainty gives us a feel for what to expect.

Now let's add seasonality.


Another approach. We move from cumulative production to daily production using \`df\['y'\].diff()\`. `tssmoothie` is a module that lets us do exponential smoothing.


This graph shows actual values (dots), forecasted values (dark blue), and probable range (light blue). This graph makes the seasonality very clear. Production is higher in the summer than in the winter.
