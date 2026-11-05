# SafeGuard Android starter

This is the first buildable Android starter for SafeGuard.

## Included in this starter
- Dark navy SafeGuard screen
- Local PIN setup/change and PIN verification
- Android BiometricPrompt integration
- GitHub Actions workflow to build a debug APK in the cloud

## Important limitations
This is not yet a complete app locker. It does not intercept launches of other apps, configure a pattern lock, or take intruder photos. Those require additional Android components and clear user-granted permissions. Intruder alerts should be opt-in and privacy-conscious.

The sample PIN hash is a starter implementation, not production-grade credential storage. Before public release, replace it with a salted, slow password hash and Android Keystore-backed protection, add rate limiting, and complete security testing.

## Build from a phone using GitHub
1. Create a GitHub account and a new empty repository named `SafeGuard`.
2. Upload the contents of this folder to the repository (not the parent folder).
3. Open the repository's Actions tab.
4. Select **Build SafeGuard APK** and tap **Run workflow**, or push to `main`.
5. When the run finishes, open it and download the `SafeGuard-debug-apk` artifact.
6. Extract the ZIP and install `app-debug.apk` on your Android phone. Android may ask you to allow installation from the browser or file manager you used.

For a real app-locking release, test only on devices you own or have permission to manage.
