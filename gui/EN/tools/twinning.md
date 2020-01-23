# Twinning-help

# Twinning
These tools provide a quick way to assess whether twinning is present in your structure.

## Search for Twin Laws
This will search for all metrically possible twin laws, and list them along with an approximate R-factor reduction. You can then test them to decide if you believe there is a twin law. Each twin law will generate a hklf5 format file.

## Cumulative Intensities
This will generate a graph of the cumulative intensities. If you data follows the bottom line, then your crystal is almost certainly twinned.

## Detailed Options

### Extended
This runs more cycles of the twinning procedure, and can find more complex twin laws. It takes a noticibly longer time than the basic version.

### Personal
These values are stored internally in your user profile and will persist between structures. 
You can raise the maximum index to search more axes. Doubling this value increases the time taken eightfold.

 You can raise the rotation fraction to search in smaller increments. Doubling this value doubles the time taken.

 You can raise the proximity threshold to allow for wider margins on 'overlapping' diffraction peaks. This will store and test more twin laws, but should not have much impact on the time taken.
 
 ### Search
 Executes a search with your personal options rather than the iterated standard search.




