# lab8TriviaQuestion
placing code to link for post requesting assistance

TLDR: Browsers make it so you can't change the background color of the autofill using !important 
  https://developer.mozilla.org/en-US/docs/Web/CSS/:autofill


I was attempting to change the background color of the input field for part 2 of this lab.
I was finding that if I left the field empty, and submitted, it would work. However if I entered in something into the input field it didn't work.
The part that shows "correct" or "incorrect" was working, so I knew the if/else was working properly.

Unfortunately while trying to figure out what was going on I neglected to remember one of the most basic troubleshooting techniques, try it in another environment
or in this casse another browser.

When I did so I entered in a name and it worked.
It was then that I realized that I had been using the autofill to select things I had previously typed into the input to make things quicker/easier.
It never ocurred to me that the autofill might be a different situation than entering in something manually.

That's when I found the above linked documentation about :autofill and how most browsers don't allow you to change background-color.
Within the context of this lab where normally people wouldn't enter the same thing over and over again the simplest solution was to change a line in the index.html file
  From:<input type="text" placeholder="Dresden" id="wizbox"/>
  To: <input type="text" placeholder="Dresden" id="wizbox" autocomplete="off"/>
  
It's not very satisifying to just turn it off, and over all I think it's better usability to have it on, but for this page it works.
While trying to find that MDN page again today to update this repo I saw some links to what looked like they were probably better work arounds for this situation. 
I haven't investigated them at this time but it's something to consider for next time if the context calls for a better solution.
