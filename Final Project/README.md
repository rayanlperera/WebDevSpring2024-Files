# Final Project Documentation

## Process
My process throughout this project was to focus on working each page for the website. My goal for the website was to create an experience where the user was able to sift through different vinyls as if they were walking into a vinyl shop and looking though a basket of vinyls. To further the experience I wanted to add my own personal reviews and experiences on listening to each of the album.

## Source Code
Here in the source code you'll find 3 pages for the website. Each of the pages have the same code for the navbar across all of the websites and using the same style sheet throughout.

There's a homepage that contains a carousel with different images of albums and a small description at the bottom of the website. In the about page here you'll see a headshot image of me and paragraph of text describing who I am and why I created the site. Finally in the contact page there is a form that the user can fill out. 

Here's the some code that I felt really happy with throughout developing the project:

This code adds a gradient to make the text visible in the carousel:


```
{
    /* Adds the gradients in between the text and images */
    #vinylCarousel .carousel-item:before{
    content: "";
    background-image: 
    linear-gradient(
        to bottom,
        transparent, rgba(196, 235, 196, 0.7)
    );

    display:block;
    position:absolute;
    top: 0;
    width: 100vw;
    height: 100vh;
}

}


```
This code is to create the rotating vinyl image behind the contact form. 

```
{

     document.addEventListener('DOMContentLoaded', () =>{
    //make content fade in on load
    gsap.from('body', 1, {opacity: 0})

    //make vinyl slowly come out
    gsap.from('#hi-there', 1, {left:0, delay: 0.5 })

    gsap.to('#hi-there', 5,  {rotation:1440, repeat: -1, yoyo: true})

    
   

  })
  // makes sure the animation fits on mobile screens
  let mm = gsap.matchMedia();

  mm.add("(max-width: 767px)", () => {

    gsap.from('#hi-there', 1, {left:0, delay: 0.5 })

    gsap.to('#hi-there', 5,  {rotation:1440, repeat: -1, yoyo: true})

  })


}

```

## Issues That I Encountered

Throughout the project I encountered throughout the project was really trying to work out how to navigate the bootstrap grid. For the about page I really had trouble with positioning items around the page. It was really difficult to position for both the mobile and desktop versions, but I managed to find a way. 

On top of that what else was difficult was positioning the vinyl animation on the contact page with the javascript functions. But also finding the match media function helped out a lot with animation.


## What I Learned

Throughout the project I learned bootstrap such as the navbars, carousel, using forms, and using the grid. On top of that I learned how to use Greensock and how to animate certain objects on the website.

## Next Steps

For next steps I would want to connect the contact pages to Formspree. On top of that I would like to add 3D models through three.js to mimic the user playing around with the vinyls. Finally I would like to add a list of the songs in each album which would direct to either a music video or play the song through a video player.
