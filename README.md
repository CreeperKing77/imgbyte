# imgbyte
Python module for interaction and actions with the imgflip website using a combination of selenium and requests.

# Documentation
## Setup
createWindow()
> Creates a new window and bot instance.<br/>
> Usage:
``` driver = createWindow() ```<br/>
> The driver object will then be used for all future imgbyte functions.<br/>

img_url(driver, page_path)
> Sets the driver window to the input url. Useful if you want to do some custom things with the page html on a specific page. <br/>
> Many of the functions in this module require it, so be aware that use of them will change the window location. <br/>
> imgbyte functions that require this will be notated with a ``` * ```<br/>
> Usage: ``` img_url(driver, 'user/Imgflip') ```<br/>

login(driver, username/email, password)
> Logs into the specified account. <br/>
> Makes use of the get_token function to add the session token to the driver, as ``` driver.token ```. <br/>
> Most functions require being logged into a user account. Ones that do will be notated with a ``` ~ ```. <br/>
> Usage: ``` login(driver, username, password) ```

get_token(driver)
> Returns the current session token as a string. Requires being logged in.
> Optionally, use ```driver.token``` instead.

## Comments
comment_vote(dtiver, vote_type, comment_id) ~
> Add or Remove and upvote or downvote from a comment.<br/>
> vote_type must be 1 to upvote, 0 to downvote, and -1 to remove your current vote.<br/>
> Usage: ```comment_vote(driver, 1, 1234)``` *Upvotes the comment with id of 1234*

get_comments(driver, post_id) *
> Returns a list of comment objects on the post with the given post id.<br/>
> Comment objects have the attributes ```identifier, user, content, postid, user_perm, image```<br/>
> identifier: the comment id<br/>
> user: username of the user who made the comment<br/>
> content: the text of the comment<br/>
> postid: the id of the post the comment is on<br/>
> user_perm: the permission level of the user. includes ```global-mod, site-mod, stream-mod, normal-user```<br/>
> image: if the comment contains an image, this will be a base64 encoded string of said image<br/>



