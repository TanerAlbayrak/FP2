# Final Project Assignment 2: Explore One More! (FP2) 
DUE March 30, 2015 Monday (2015-03-30)

This is just like FP1, but where you do a different library. (Full description of FP1 is [on Piazza.][piazza])

During this assignment, you should start looking for teammates. See the project schedule [on Piazza.][schedule]

Write your report right in this file. Instructions are below. You can delete them if you like, or just leave them at the bottom.
You are allowed to change/delete anything in this file to make it into your report. It will be public.

This file is formatted with the [**markdown** language][markdown], so take a glance at how that works.

This file IS your report for the assignment, including code and your story.

Code is super easy in markdown, which you can easily do inline `(require net/url)` or do in whole blocks:
```
#lang racket

(require net/url)
```

### My Library: Images
Write what you did!
Remember that this report must include:
 
 I went through the images library and found some procedures to blue images and manipulate them in many ways.
 I was able to draw a venn diagram with different colors and also manipulate exactly how the image looks, from the brushes thickness to blurring the appearance, just like photoshop.
 
 ```
 #lang racket
(require images/flomap)

(define fm
    (draw-flomap
     (λ (fm-dc)
       (send fm-dc set-alpha 0)
       (send fm-dc set-background "green")
       (send fm-dc clear)
       (send fm-dc set-alpha 1/3)
       (send fm-dc translate 2 2)
       (send fm-dc set-pen "red" 4 'long-dash)
       (send fm-dc set-brush "red" 'solid)
       (send fm-dc draw-ellipse 0 0 192 192)
       (send fm-dc set-brush "green" 'solid)
       (send fm-dc draw-ellipse 64 0 192 192)
       (send fm-dc set-brush "blue" 'solid)
       (send fm-dc draw-ellipse 32 40 200 192))
     260 240))
     
     > (flomap->bitmap fm)
```
 [img]http://i.imgur.com/CmWOZvC.png?1[/img]
 
 
* a narrative of what you did
* the code that you wrote
* output from your code demonstrating what it produced
* any diagrams or figures explaining your work 
 
The narrative itself should be no longer than 350 words. Yes, you can add more files and link or refer to them. This is github, handling files is awesome and easy!

Ask questions publicly in the Piazza group.

### How to Do and Submit this assignment

1. To start, [**fork** this repository][forking].
1. Modify the README.md file and [**commit**][ref-commit] changes to complete your solution.
  2. (This assignment is just one README.md file, so you can edit it right in github without cloning)
  3. (You may need to clone and push if you want to add extra files)
1. [Create a **pull request**][pull-request] on the original repository to turn in the assignment.

<!-- Links -->
[piazza]: https://piazza.com/class/i55is8xqqwhmr?cid=411
[schedule]: https://piazza.com/class/i55is8xqqwhmr?cid=453
[markdown]: https://help.github.com/articles/markdown-basics/
[forking]: https://guides.github.com/activities/forking/
[ref-clone]: http://gitref.org/creating/#clone
[ref-commit]: http://gitref.org/basic/#commit
[ref-push]: http://gitref.org/remotes/#push
[pull-request]: https://help.github.com/articles/creating-a-pull-request

