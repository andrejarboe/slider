# React Testimonial Slider

This is a React component that displays a testimonial slider. It uses the React Hooks API to display a testimonial slider with a text quote, image, and name of the person who provided the testimonial. It also has a built-in auto-slide feature and navigation buttons to manually move the slider.



## App.js

- `people`: is a data state array. Each `index` contains keys of: `id, image, name, title, quote`
- `index`: is a state value that hold the current index value in the people array
- `useEffect` for buttons: contains 2 conditions that check for the `index` to be with in the `people` array.
    - the first checks that `setIndex(index + 1)` does not pass the last index of the  `people` array in the positive direction and returns 0
    - the second checks that `setIndex(index - 1)` does not pass the last index of the  `people` array in the negative direction and returns array length - 1
- `prev` button: triggers `setIndex(index - 1)` 
- `next` button: triggers `setIndex(index + 1)` 
- `useEffect` for auto sliding: creates a variable `slider` that adds 1 to `index` via `setIndex(index + 1)`. It has a delay of 3 seconds. it then returns `clearInterval(slider)`. his resets the time to 0 and only changes the `index` state value when the time gets to 3 seconds.

