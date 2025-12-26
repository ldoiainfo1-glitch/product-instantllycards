# Android App Links Setup - Digital Asset Links

## What is this?
This file verifies that the Instantlly Cards Android app is authorized to open links from instantllycards.com

## File Location
`.well-known/assetlinks.json`

## How to verify it's working:

1. **After deployment, check the file is accessible:**
   ```
   https://instantllycards.com/.well-known/assetlinks.json
   ```

2. **Use Google's Testing Tool:**
   https://developers.google.com/digital-asset-links/tools/generator

3. **Verify in Statement List Generator:**
   - Site domain: instantllycards.com
   - Package name: com.instantllycards.www.twa
   - SHA256 fingerprint: 5B:8E:A0:6F:65:E0:38:F7:22:EF:38:E1:0E:D7:B3:0D:FD:7D:60:7F:EA:26:2E:B7:4B:2B:55:3D:D9:65:C9:9A

## Requirements:
✅ File must be served over HTTPS
✅ Content-Type must be `application/json`
✅ No redirects allowed
✅ File must be publicly accessible

## Troubleshooting:
If verification fails, check:
1. File is accessible at the exact URL above
2. Returns HTTP 200 status
3. Has correct Content-Type header
4. Domain doesn't redirect (www vs non-www)
5. HTTPS certificate is valid
