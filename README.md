# three-element-role-application
A prototype of role-application with focus handling, in order to create a mobile SR fallback for [data navigator](https://dig.cmu.edu/data-navigator/), without intercepting swipe gestures in javascript.

## Notes
Using a desktop screen reader, this works fine. Using a touch-based screen reader (ipad), there is a little bit of an echo because the swipe focuses and then the focus is moved with javascript.

The lifecycle works like this while inside the structure:
- user swipes (forward or backward)
- new element receives focus
- we render the middle element with desired info and focus that element
- after focusing, we render the pre and post elements with new attributes based on the user's new location in the structure

All in all, this experience isn't ideal. Plus, a structure with many, many elements will become tedious (but data navigator would allow a user to skip them all).
