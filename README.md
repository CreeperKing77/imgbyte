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
> Usage: ``` img_url(driver, 'user/Imgflip') ```
