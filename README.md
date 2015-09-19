# cordova-ios-security
`cordova plugin add https://github.com/sorned/cordova-ios-security.git`

It will add the following part to the `*-Info.plist` file during build process:

    <key>NSAppTransportSecurity</key> 
    <dict>
      <key>NSExceptionDomains</key>
      <dict>
        <key>amazonaws.com</key>
        <dict>
          <key>NSIncludesSubdomains</key>
          <true/>
          <key>NSTemporaryExceptionAllowsInsecureHTTPLoads</key>
          <true/>
          <key>NSTemporaryExceptionMinimumTLSVersion</key>
          <string>TLSv1.1</string>
        </dict>
      </dict>
    </dict>
