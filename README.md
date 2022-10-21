# How to config Kmail to use office 365 which forces OAUTH2

***This is only a work around which I don't even know why it works, but it works***

***If there is any possiblity, plz stay against these non-standard proprietary protocols. However, I admit sometimes life sucks and leaves no choice***

(I only tested KMail 5.19.2 (21.12.2))

- Create an empty identity for this, don't add email address or anything
- Open Kmail configure - Accounts - Receiving
- Add custorm account - EWS
- Input EMail, unclick domain if your office 365 uses default domain (outlook.office365.com)
- Input Username and Password (yes it will fail because OAuth2 is forced)
- Uncheck Server Autodiscovery and manually input EWS URL (if your provider doesn't change it, the default is https://outlook.office365.com/EWS/Exchange.asmx)
- Press OK (it will ask you it is not working and whether you want to save it, click yes)
- Reopen it to modify it
- Check OAuth2 (Office 365)
- Click Try connect, the OAuth2 prompt will show up
- Finish it and the incoming account is set
- Go to Sending and click Add...
- Chosse EWS, the account you just verified will show up, chose it and outgoing account is set
- Now edit the empty identity you added at beginning, and everything is done.
