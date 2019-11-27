

```
import windpy as pw

#The following files will be located in the same folder as the code to run.
#crypto.py
#wind_asset_default.py
#windpy.py


seed = "............................"
myAddress = pw.Address(seed=seed)

recipient = "3MGqSoQJHGDvRyZRPU56ytekxJ5Q7D2CayQ"
recipient=pw.Address(address=recipient)

asset = "BfZqyk3gnPUJWsPX8qfa4ZhNXvdsgJ4Mm1aySRW2mJ1z"
asset = pw.wind_asset_default.Asset(assetId=asset)

message = ('Hello WIND')
message = message.encode('utf-8').decode('latin-1')

#Send WIND
myAddress.sendWind(recipient = recipient, amount = 1, attachment=message)

#Send asset
myAddress.sendAsset(recipient = recipient, asset = asset, amount = 10, attachment=message)

#Create alias
alias = "1dsadd433"
myAddress.createAlias(alias=alias)

#Issue asset
myAddress.issueAsset( name = "WEUR", description = "WEUR" , quantity = 100000000000000, decimals = 0 )

#Burn asset
myAddress.burnAsset(Asset=asset, quantity=100)

#lease
myAddress.lease(recipient=recipient, amount=1000000)

# Cancel lease
myAddress.leaseCancel(leaseId="HZSYEiE4XrwY7dEi9sCMpYvNf5UZgm2Xj18Cf8mtpD5U")

# Sponsor asset
myAddress.sponsorAsset(Asset= asset, minimalFeeInAssets = 1)
```
