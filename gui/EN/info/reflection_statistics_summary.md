# Reflection-Statistics-Summary-help
# Reflection Statistics Summary
This table collects in one place the most important indicators of the quality of the diffraction data used for refinement. These parameters are independent of any structure model or refinement process.

## TotalReflections
Total number of reflections recorded during the diffraction experiment.

## UniqueReflections
Total number of unique reflections (unrelated by symmetry) recorded during the diffraction experiment.

## DataCount
Usually equal to the number of unique reflections.

## FriedelOppositesMerged
Number of Friedel reflection pairs (*h*, *k*, *l*) and (-*h*, -*k*, -*l*) that have been merged in the data. Such merging is very uncommon, so this number is usually zero.

## InconsistentEquivalents
Number of pairs of equivalent reflections in the data that are dissimilar.

## SystematicAbsencesRemoved


## MinD
Minimum resolution of the data set, in &Aring;.

## MaxD
Maximum resolution of the data set, in &Aring;.

## LimDmin
Minimum possible resolution (theoretical limit based on the unit cell dimensions), in &Aring;. This value may be higher than the theoretical limit due to OMIT commands applied to the data.

## LimDmax
Maximum possible resolution, in &Aring;. This value may be affected by OMIT commands applied to the data.

## FilteredOff
Number of reflections removed from the data by ranged commands such as "OMIT -3 50" or "SHEL 15 0.8".

## OmittedByUser
Number of reflections omitted from the data by specific OMIT commands such as "OMIT 1 0 0".

## OmittedReflections


## IntensityTransformed


## Rint
A measure of the precision with which individual reflections were measured in the diffraction experiment. If Rint is about two to three times bigger than Rsigma (see below), there may be a problem with the data set.

## Rsigma
A measure of the signal-to-noise ratio in the diffraction experiment.

## MeanIOverSigma
Average value of I/&sigma;(I) over the entire data set; a measure of the signal-to-noise ratio in the diffraction experiment.

## Completeness
Point group completeness of the data set out to the maximum 2&theta; recorded in the diffraction experiment.

## MaxIndices
Maximum values of the indices *h*, *k*, and *l* in the data set used for refinement (i.e., after OMIT statements have been applied).

## MinIndices
Minimum values of the indices *h*, *k*, and *l* in the data set used for refinement (i.e., after OMIT statements have been applied).

## FileMaxIndices
Maximum values of the indices *h*, *k*, and *l* in the data set, as originally recorded in the diffraction experiment.

## FileMinIndices
Minimum values of the indices *h*, *k*, and *l* in the data set, as originally recorded in the diffraction experiment.

## ReflectionAPotMax


## FriedelPairCount
Number of Friedel pairs (*h*, *k*, *l*) and (-*h*, -*k*, -*l*) in the data set.

## Redundancy
In the set of numbers (*n*<sub>1</sub>, *n*<sub>2</sub>, *n*<sub>3</sub>, ...) listed here, *n*<sub>1</sub> is the number of reflections in the data set measured once, *n*<sub>2</sub> is the number of reflections measured twice, *n*<sub>3</sub> is the number measured three times, etc.

## IsCentrosymmetric
This number is 1 if the structure is centrosymmetric and 0 if it is non-centrosymmetric.

## Completeness\_laue\_full
Laue group completeness of the data set, calculated out to the IUCr-recommended resolution limit sin(&theta;)/&lambda; &ge; 0.6 (e.g., 2&theta; = 50.5&deg; for Mo K&alpha; radiation).

## Completeness\_point\_full
Point group completeness of the data set, calculated out to the IUCr-recommended resolution limit sin(&theta;)/&lambda; &ge; 0.6 (e.g., 2&theta; = 50.5&deg; for Mo K&alpha; radiation).

## Completeness\_laue\_max
Laue group completeness of the data set, calculated out to the maximum 2&theta; recorded in the diffraction experiment.

## Completeness\_point\_max
Point group completeness of the data set, calculated out to the maximum 2&theta; recorded in the diffraction experiment.