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


