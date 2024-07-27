# MusicBridge

A user-friendly application designed to seamlessly transfer music tracks and playlists from Spotify to other popular music streaming platforms. This tool addresses the common challenge faced by music enthusiasts who want to switch services or maintain their music libraries across multiple platforms.

### Environment Configuration

The .env file contains sensitive configuration values and API keys necessary for the app to interact with Spotify and Apple Music services. These values should be kept confidential and never committed to version control.

How to obtain the values:

**SPOTIFY_CLIENT_ID and SPOTIFY_CLIENT_SECRET:**

- Go to the Spotify Developer Dashboard (<https://developer.spotify.com/dashboard/>)
- Log in or create a Spotify Developer account
- Create a new application
- Once created, you'll see the Client ID on the app's dashboard
- Click "Show Client Secret" to reveal the Client Secret

**APPLE_KEY_ID, APPLE_TEAM_ID, APPLE_PRIVATE_KEY:**

Sign in to your Apple Developer account (<https://developer.apple.com/>)

- Go to "Certificates, Identifiers & Profiles"
- Navigate to "Keys" and create a new key for MusicKit
- The Key ID will be displayed when you create the key
- Download the private key file (.p8) - this is your APPLE_PRIVATE_KEY
- Find your Team ID in the membership details of your account

**APPLE_JWT_TOKEN:**

- This is a JSON Web Token you need to generate using your Apple Developer credentials
- Use a JWT library in your preferred programming language to create this token
- It should be signed with your private key and include your Team ID and Key ID

**APPLE_USER_TOKEN:**

- This token is obtained when a user authenticates with your app using their Apple ID
- You'll need to implement Apple Music user authentication in your app to get this token
- The process involves using Apple's MusicKit JS or native SDKs
  Remember to keep your .env file secure and never share these values publicly. When deploying your application, use environment variables provided by your hosting platform instead of a .env file for added security.

## Useful Links

- <https://developer.spotify.com/documentation/web-api/reference/get-a-list-of-current-users-playlists>
- <https://developer.apple.com/documentation/applemusicapi/playlists>
