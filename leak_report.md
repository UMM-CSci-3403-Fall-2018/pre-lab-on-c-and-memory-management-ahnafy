# Leak report

We make sure memory is allocate to result so that each character is kept track of. In the strip function at `line 42` memory leaks, and also at `line 62` of the main function. As characters are passed along function, nothing is freed at any step what so ever.

## To fix the memory leak

We need to free memory in the function is_clean. After the string comaparison is made, we check if the cleaned string is null. If not, we make sure the memory is free. However, for a null string that cannot be made to happed. 
