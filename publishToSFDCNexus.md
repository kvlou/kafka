###Publishing custome secure version of kafka to SFDC Nexus:

Update gradle.properties with following properties or copy gradle.sfdc.properties.

```
version=0.8.2.0-sfdc-0.2-SNAPSHOT
mavenUrl=https://nexus.soma.salesforce.com/nexus/content/repositories/thirdparty-snapshots
mavenUsername=+XcZR4PQ
mavenPassword=u55T3x40oGiY2OxBV5Ykv9hEO+lFxbg+TzY68D39BEJp
signing.keyId=13DBFFE4
signing.password=kafka_security
signing.secretKeyRingFile=/Users/relango/.gnupg/secring.gpg
```

You need to create keys for signing jar and update it appropriately. I did following steps to create keys

1. Install [gpgtools](http://www.gpgtools.org/)
2. Run `gpg --gen-key`
3. Run `gpg --list-secret-keys` to find the keyId and secretKeyRingFile (first line of output)

