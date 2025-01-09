# Troubleshooting

## OpenVPN works but I can’t connect to the ELDB Server

## “server not found” / “can not find specified endpoint” etc

- Check that you’ve entered the server name correctly:
  - _eldb.qmul-ceg.net_
- It can help some applications to specify that the connection uses TCP, either in a select dropdown or as a prefix:
  - _tcp:eldb.qmul-ceg.net_
- If the server name still doesn’t work, try using the endpoint name:
  - _tcp:ceg-mssql-02.czd1trqfl4br.eu-west-2.rds.amazonaws.com_)
- If that doesn’t work, try using the server’s IP address. This can change when the server is rebooted or updated, which is why it is recommend to use the server name or endpoint, if possible. The current server IP address is:
  - _tcp:192.168.5.130_

## OpenVPN login doesn’t work

- Check that you are putting the correct information into the OpenVPN login. It doesn’t’ use a username or password. In the credentials popup put:
  - Username = your ovpn file name. eg “danield”, if your file is danield.ovpn
  - Password = “PUSH”. This is command to push authentication to the Duo app.
- If you’ve recently been sent a new ovpn file, make sure you have installed it.
- Check the OpenVPN log
  - Right click on the tray icon and click View Log.
  - Errors will be flagged as ERROR and may help point you in the right direction
- Still not sure – save a copy of the log and attach in an email to CEG.

## Contacting CEG

Send queries to [m.a.sharp@qmul.ac.uk](mailto:m.a.sharp@qmul.ac.uk), who will assess and pass them on as required. We will respond within 48 hours.

| Date | Version | Information |
| --- | --- | --- |
| 19/06/2023 | 1   | Document Created |
| 01/09/2023 | 2   | Added information on Azure Data Studio<br><br>Added information on Power Query<br><br>Added Password section<br><br>Revised the Overview section<br><br>Removed the Table of Contents, as too difficult to maintain<br><br>Various formatting and typo corrections |
| 31/10/2023 | 3   | Added connecting to SQL server through R |
| 01/08/2024 | 4   | Updated and improved the Overview<br><br>Amended Setting Up an ODBC User DSN to emphasise that DSNs can be reused for different databases on the server.<br><br>Expanded the Troubleshooting section |