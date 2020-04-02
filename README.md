# Google Drive Player Proxy Generator + JW Player 8 + WordPress Plugin + Anti Limit
Grab google drive streaming links (redirector.googlevideo.com/videoplayback?..)

![](https://i.imgur.com/pkAyfgr.png)

## Usage API

Use directly here : <a href="http://streamapi.net/" rel="dofollow">http://streamapi.net/

API : http://streamapi.net/get.php?url=https://drive.google.com/file/d/[ID]/view&poster={url}&logo={url}

Live Demo : http://streamapi.net/embed.php?id=352214&poster=https://i.imgur.com/AYx7p2r.png&logo=http://streamapi.net/template/images/logo.png

## Usage WordPress Plugin

Download : http://streamapi.net/wp_streamapi_v1.zip

## How to use:
 
 1. #### Download and install the plugin
 2. #### Go to setting > StreamAPI
 3. #### How to use
 
### Place This Code Under Your Post Content:
 
Code:
[api link="your_video_link" poster="poster_link" logo="logo_link"]

### Example #1:
 
Code:
[api link="https://drive.google.com/file/d/13bmEX-hj1vj1p03KdUb41Wc1gA4IXBoj/view" poster="http://streamapi.net/poster/1.jpg" logo="http://streamapi.net/template/images/logo.png"]

### Example #2:
 
Code:
[api link="https://drive.google.com/file/d/13bmEX-hj1vj1p03KdUb41Wc1gA4IXBoj/view"]


## Usage PHP Code
## How to use

### PHP Code:

	$streamAPIContent = file_get_contents('http://streamapi.net/get.php?url={url-drive-google}&poster={poster-url}&logo={logo-url}');
	$datastreamAPI = json_decode($streamAPIContent, TRUE);
	if($datastreamAPI['status_video']=='Ready') {
		$streamAPISLUG = $datastreamAPI['iframe'];
		$statusVideo = 1;
	}
	

### In which
1. #### {url-drive-google} : File path from google drive. Note: Always grant public rights.
2. #### {poster-url} : Image path
3. #### {logo-url} : Logo path
4. #### $streamAPISLUG : Path to attach to iframe tag
5. #### $statusVideo : Video status. 1 ready. 0 errors
