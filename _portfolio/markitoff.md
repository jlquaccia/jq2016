---
layout: post
title: Markitoff
thumbnail-path: "img/blocitoff.png"
short-description: A self-destructing to-do list application.

---

{:.center}
![]({{ site.baseurl }}/img/blocitoff-2.png)

<div class="text-center cl-effect-1">
  <a href="https://jason-quaccia-blocitoff.herokuapp.com" class="page-link">View Project</a>
</div>

## Summary

Markitoff is an app I built for school while enrolled in Bloc Inc.'s full-stack web developer track.  Not only designed to help out with your daily tasks, it acts as a motivation enhancer and a way to diminish procrastination.  Upon submitting a task to complete, 7 days are given to accomplish what you said that you were going to do.  If you don't complete a task within one week then that task will be removed from your list.  It may not have been as important to you as you thought.

{% highlight ruby %}
namespace :todo do
  desc "Delete items older than seven days"
  task delete_items: :environment do
    Item.where("created_at <= ?", Time.now - 7.days).destroy_all
  end
end
{% endhighlight %}
> <div class="small">Rake task automated to count the remaining days left for a task.</div>

## Explanation

Markitoff was the first real hands-on project that I built from scratch that revolved around Rails full-stack web development.  I learned how to automate rake tasks and utilize Ajax within a Rails application.  Markitoff is 100% responsive and all of the styling was done by me.

## Problem

Ever say you are going to do something but don't?  Do you try to stay organized but end up reverting back to your old ways in the end?  Procrastination is a serious problem now and has been for generations.

## Solution

With Markitoff you can get your tasks done and stay motivated knowing that each task has a limited amount of time to be completed.  This makes checking things off your todo list fun and ultimately makes you a better person.

## Results

The results were quite positive.  Although Markitoff is a very simple web application it was received well by the users that tested it.

## Conclusion

Markitoff works because it helps to motivate you and organize your daily routine.  I feel the rake automation greatly enhances the experience and prompts the user to try harder.  This project has taught me a lot about Rails and has strengthened my fundamental knowledge as a web developer.  I will surely carry forward this knowledge with me in the future.