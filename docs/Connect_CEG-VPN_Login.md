# CEG-VPN Login
## Connecting to CEG-VPN

- Right-click the OpenVPN tray icon on your taskbar or click the Tunnelblick icon on your status bar and click Connect. A window will appear with connection messages.
- On the first-time logging in, you will need to provide username/password information.
```
Username = your ovpn file name. eg “danield”
Password = “push”
```
These are instructions for the OpenVPN/Duo system and not an actual username/password.

- Click or Tick to Save the Password.
- Click OK or wait 5 seconds for the client to automatically make the connection.

The connection window will show various messages, including that it is sending PUSH REQUEST messages.
You should receive a Duo notification on your phone. Sometimes this is a bit slow, and you may need to open the app to see the notification. 

- Tap Accept on the notification.

The connection window will take a few more seconds to complete the connection messages and then close or can be closed.
Once connected, the OpenVPN tray icon will show as green or the Tunnelblick icon will be highlighted.

More information can be found:
<https://community.openvpn.net/openvpn/wiki/OpenVPN-GUI>
<https://tunnelblick.net/czQuick.html>

## Disconnect from CEG-VPN
When you have finished using ELDB, disconnect from the server in the software that you are using and then disconnect from the VPN. Disconnecting from the VPN whilst still connected to a resource can cause some programmes to hang for a short while.

- Right-click the OpenVPN tray icon on your taskbar and click Disconnect.
- Or click on Disconnect in the Tunnelblick menu icon and Quit.