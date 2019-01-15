This project/page is simply a test harness to listen to messages sent from a parent page when this page is enbedded in an iframe. It was originally created to test message passing in a [VS code extension](https://github.com/ytechie/armviz-vscode-extension).

## Sending Messages from the Parent

If you have this project embedded in an iframe like this:

    <iframe id="armvizFrame" src="https://windowmessages.azurewebsites.net/index.html"></iframe>

You can use this code to send messages to the child frame:

    const webFrame = document.getElementById('myframe');
    webFrame.contentWindow.postMessage({ foo: 'bar' }, '*');