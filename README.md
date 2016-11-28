# tweet-bot
A Twitter Bot that retweets, favorites, on the basis of hashtags and replies to other users if they follow it.

<h1>1- What you need?</h1>
<ul>
  <li>You must have <a target="_blank" href="https://nodejs.org/en/">Node.js</a> installed on your system.</li>
  <li>A Twitter Account.</li>
  <li>Your bot will be using <a target="_blank" href="https://www.npmjs.com/package/twit">twit</a> which is an npm module to manipulate tweets and streams, and to communicate with the 
  <a target="_blank" href="https://dev.twitter.com/docs">Twitter API.</a></li>
</ul>

<h1>2- Configuring and granting permissions from Twitter API</h1>
<p>
After logging to to your Twitter account, follow to this link: https://apps.twitter.com/app/new to create a new application. Fill out the necessary fields in the form click on the button Create Your Twitter Application. After creating the application, look for ‘Keys and Access Tokens’ under the nav-panes and click on ‘Generate Token Actions` and then copy:
</p>
<ul>
  <li>Consumer Key</li>
  <li>Consumer Secret</li>
  <li>Access Token</li>
  <li>Access Token Secret</li>
</ul>
<p>Open the <pre>config.js</pre> file and paste all four values inside it. Expose those values using <pre>module.export</pre></p>
<pre>
  //config.js
  /** TWITTER APP CONFIGURATION
  * consumer_key
  * consumer_secret
  * access_token
  * access_token_secret
  */
  module.exports = {
    consumer_key: '',  
    consumer_secret: '',
    access_token: '',  
    access_token_secret: ''
  }
</pre>

<h1>3- Change the hashtags values</h1>
<pre>
var params = {
  q: '#HELLOTREE,#nodejs',  // REQUIRED
  result_type: 'recent',
  lang: 'en'
}
</pre>

<h1>4- Building the bot</h1>
<ol>
  <li>git clone https://github.com/tareksmoubarak/tweet-bot.git</li>
  <li>Navigate into bot directory and run: <b>npm install</b> </li>
  <li>Run the following command: <b>node bot.js</b>
</ol>
