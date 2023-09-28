<h1>Count Not Incrementing</h1>

<h2>Confirm basic setup</h2>

<ol>
  <li>
    Supported URLS - if your URL isn't in one of the below formats, the
    extensions won't work. * means it can be any value.
  </li>
  <ul>
    <li>https://*.teams.microsoft.com</li>
    <li>https://*.teams.microsoft.com.mcas.ms</li>
  </ul>
  <li>
    Confirm your subscription status is set to green within the settings popup.
  </li>
  <li>
    Confirm various settings such as enabled toggle, time window to run
    extension, and set status as check box
  </li>
</ol>

<h2>Reinstall - this will reinitialize all listeners/logic</h2>
<ol>
  <li>In chrome, navigate to: chrome://extensions/</li>
  <li>Click Remove for MS Teams: Always Available</li>
  <li>
    Reinstall from
    <span class="header">
      <a
        id="teams-link"
        href="https://chrome.google.com/webstore/detail/microsoft-teams-always-av/klbhkcdmilipmdaejfmhmphbdfiofoen"
        >Chrome Web Store</a
      >
    </span>
  </li>
  <li>Login again</li>
  <li>Validate count is incrementing</li>
</ol>

<h2>Log out and back in of Teams</h2>
<ol>
  <li>Log out and back in</li>
  <li>Validate count is incrementing</li>
</ol>

<h2>Lastly, investigate using dev tools</h2>
<ol>
  <li>Open Microsoft Teams tab in Chrome</li>
  <li>
    Load devtools using f12 on keyboard. You can also right click, inspect
    element
  </li>
  <li>In dev tools, open Console tab at the top</li>
  <li>Clear the console using the 🚫 icon</li>
  <li>
    Open the left hand nav using square with arrow icon, and select the top
    option to show all messages
  </li>
  <img
    style="width: 20%; margin-bottom: 5px"
    src="img/clearAndOpen.jpg"
    alt="option"
  />
  <li>
    Wait ~30 seconds for a new force availability request to come in. Then, we
    can view it's output. See below pic to view an example working output
  </li>
  <li>
    The logging always begins with 'requestForceAvailability'. If this message
    never appears, try uninstalling and reinstall again. The Teams tab isn't
    running the extensions code.
  </li>
  <li>Next, various settings such as status, startTime, and endTime.</li>
  <li>
    Next, confirm the auth token. Auth tokens are never exported from the
    extension. They are only used within the Teams tab. Make sure the auth
    token, a very long string of characters, is found. If it's not, then request
    to force availability will fail.
  </li>
  <li>
    Lastly, investigate the request for force availability worked. This is the
    last logging. You want to confirm the status is 200 and ok is true. If for
    any reason these are not 200/true, the request to force availability failed.
  </li>
  <li>
    If you are here and still experiencing issues, send an email to me at
    msteamsaa@gmail.com with a screenshot similar to the one below.
  </li>

  <img
    style="width: 100%; margin-bottom: 25px"
    src="img/devtools.jpg"
    alt="option"
  />
</ol>

<style>
</style>
