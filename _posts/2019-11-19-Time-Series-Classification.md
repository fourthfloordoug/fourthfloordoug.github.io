## Multi-Level Time Series Marketing

[TEASER: Early and Accurate Time Series Classification](https://arxiv.org/abs/1908.03405)

Authors: P. Schäfer, U. Leser

I've been looking into this a bit with some code in [this project](https://github.com/fourthfloordoug/imagerySandbox), where I'm interested in classifying time series with arbitrary observations as they come in.  The paper looks at a dual mode approach where you both provide classification (they call it the slave) and then determine if your classification is any good (called the master).  This is a nice update to what I produced as you get a second level of information out for the [sic]deciderer and don't act on insufficient information.  I feel like they aren't specifying the classifier used in the slave, which is good, as I think the pattern is transferible to what I've been doing.  They use a one class SVM to do the master level classificaiton, but this is possibly adjustable.  It looks like they're training a new classifier on the results of the slave to determine if useful information is being provided.  Interesting.  They tested on some signal processing data.

[Some code](https://github.com/patrickzib/SFA) that isn't directly this, but still related to time series.
