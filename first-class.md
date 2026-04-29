
### 1. Introduction to GSAP
* **What is it?** A powerful JavaScript library used to create high-performance animations on the web [[02:10](http://www.youtube.com/watch?v=9C03V1dXxOU&t=130)].
* **Why use it?** It simplifies complex animations that would be difficult or verbose in CSS, offering better control and performance [[03:29](http://www.youtube.com/watch?v=9C03V1dXxOU&t=209)].
* **Key Components covered in the series:** 1. Basics (this video)
    2. ScrollTrigger
    3. SVG Animations
    4. Practical Projects

### 2. Getting Started
To use GSAP, you need to include the library in your project via CDN or NPM. The video demonstrates using a CDN link in the HTML file before your custom script [[04:03](http://www.youtube.com/watch?v=9C03V1dXxOU&t=243)].

### 3. Core GSAP Methods
The "Big Three" methods for starting animations:
* **`gsap.to()`**: Animates an element **from** its current state **to** a new state [[52:26](http://www.youtube.com/watch?v=9C03V1dXxOU&t=3146)].
* **`gsap.from()`**: Animates an element **from** a specified state **to** its original state (defined in CSS). Great for entrance animations [[52:26](http://www.youtube.com/watch?v=9C03V1dXxOU&t=3146)].
* **`gsap.fromTo()`**: Allows you to define both the starting and ending points of the animation.

### 4. Basic Syntax
```javascript
gsap.to(".box", {
    x: 500,        // Move 500px on the X-axis
    duration: 2,   // Animation lasts 2 seconds
    delay: 1,      // Starts after 1 second
    rotate: 360,   // Rotate 360 degrees
    backgroundColor: "blue", // Changes color
    borderRadius: "50%"      // Changes shape
});
```

### 5. Essential Properties
* **`x` / `y`**: Short for `translateX` and `translateY`.
* **`duration`**: How long the animation lasts (in seconds) [[52:44](http://www.youtube.com/watch?v=9C03V1dXxOU&t=3164)].
* **`delay`**: Waiting time before the animation starts.
* **`repeat`**: Number of times the animation repeats (-1 for infinite).
* **`yoyo`**: Makes the animation play in reverse after finishing (back and forth).
* **`stagger`**: Creates a delay between the start of animations for multiple elements with the same class. This is excellent for animating lists or grids [[52:52](http://www.youtube.com/watch?v=9C03V1dXxOU&t=3172)].

### 6. GSAP Timelines
This is one of GSAP's most powerful features.
* **The Problem:** Without timelines, if you want animations to play one after another, you have to calculate delays manually.
* **The Solution:** `gsap.timeline()` allows you to chain animations. They will play in sequence automatically [[52:26](http://www.youtube.com/watch?v=9C03V1dXxOU&t=3146)].
```javascript
var tl = gsap.timeline();
tl.to(".box1", { x: 500, duration: 1 })
  .to(".box2", { y: 200, duration: 1 })
  .to(".box3", { rotate: 180, duration: 1 });
```

### 7. Key Learning Points
* **Object-Oriented:** GSAP uses JavaScript objects to define properties.
* **CamelCase:** CSS properties with hyphens (like `background-color`) become camelCase in GSAP (`backgroundColor`).
* **Ease:** You can add `ease: "power1.out"` or other easing functions to make movements look more natural or stylized [[52:36](http://www.youtube.com/watch?v=9C03V1dXxOU&t=3156)].

