
---

| Title | Type | Duration | Name | City |
| --- | --- | --- | --- | --- |
| Activity Lifecycle | Lab | "1:00" | James Davis | NYC |

---  
# Activity Lifecycle Lab

## Introduction

Below, you will find three scenarios, and questions following each one.

To the best of your ability, answer the questions **in english**, not in code.

Below the scenarios, you will find a few questions. Answer those however you'd like.

Answer the questions by editing this readme, pushing your changes to your forked repo, and making a pull request.

## Exercise  


####Scenario 1:

Let’s say you made a To Do list app, where you can add things to a list and cross them off. You decide to cross some items off the list and mark them as complete.

When you rotate the device, the things you marked as complete are no longer crossed off.

**Question**: Why did this happen?
<br />Answer: - the activity is destroyed and a new activity is started.

**Question**: How do you fix this issue?
<br />Answer: We can save the instance state and share the saved instance and load that saved instance state whenever the activity is recreated.


####Scenario 2:

The Amazon Kindle Android app allows you to open and read eBooks. You discovered a bug! You opened a book, and read it from the beginning up to page 68. Then, you left the app and closed it completely so you can do other things.

When you opened the app again, and opened the book, it started from page 1 (and not page 68 where you left off)!

**Question**: How would you fix this issue?
<br />**Answer**: We would use Shared Preferences to save the current page number and needs to be updated in the onPause method. That data should be made available in the onResume method so the user can get back to the page. put on the Main Activity and get on the Second Activity


####Scenario 3:

Facebook for Android added a feature last year where, if you started writing a comment on someone’s post and decided not to do so, the app would save a draft of it just in case you changed your mind.

Take this scenario. On a post on Facebook, you click the “comment” button (which opens a new CommentActivity). You start writing a comment, and then change your mind by pressing the back key (which closes the CommentActivity). You click on the “comment” button again, and in the newly-opened CommentActivity, the comment you were writing is still there.

**Question**: How would you implement this feature? Be specific; what lifecycle methods would you use in CommentActivity, and what techniques would you use? 
<br />**Answer**:You would use the onPause and onResume methods, and also the Shareprefernces method and check if(sharedpreferences !=null); to save the method.



In your own words…
==================

**Question**: What are the methods of the Activity Lifecycle?
<br />**Answer**: onCreate
                  onStart
                  onResume
                  onPause
                  onStop
                  onDestroy

**Question**: What order are the methods called?
<br />**Answer**: The methods are called in order of 
                  onCreate
                  onStart
                  onResume
                  onPause
                  onStop
                  onDestroy

**Question**: What is a bundle?
<br />**Answer**: a bundle is a set of data that you can send in a Intent.

**Question**: How do you get the Shared Preferences of an app?
<br />**Answer**: SharedPreferencnes sharedpref= getSharedPreferences(Context.MODE_PRIVATE);
to save- sharedpref.put(data type) 
to get- sharedpref.get(data type);
