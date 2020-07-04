# Protocol-8020_Disease_Profiles
Protocol-8020 Disease Profiles

Repository for gathering Disease Profiles and documenting their format and how they interact with Personal Profiles.

A Disease Profile is an XML format file with embedded key-value pairs, Probability Curves(SVG curves), and other necessary info.
For the probability curves; the Horizontal Axis is the independent variable (Age, ...), the Vertical Axis is the Disease Probability.

Personal profile is just the natural person's information in an XML format with key-value pairs to match up against a Disease Profile.

The softare component then does the math and gives us the values.  Ie: percent of risk that we will contract the disease.

--------------------------------
There is a need for an additional key-value pair that relates percentages between other values.  This is necessary because not all curves are fully independent.  Most curves/value-pairs are themselves summations of a combination of factors.  To avoid double adding, we need a way to show this ratio.  Age for example may also have risk values associated with other factors such as lung disease.  If we look at just age or if we also add in the risk of lung disease (then we must subtract the value of lung disease from age risk) so the total is more correct.  By paper this wouldn't be very practical, but the computer doesn't care about the complexity.
