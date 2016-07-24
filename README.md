# `chromepass` - Chrome autofill extension for `pass`

_This is currently a work in progress, check back later ☺._

### Setup

1. Install `chromepass` extension from the [Chrome Web Store](#todo).

2. Install and setup the [password store](https://www.passwordstore.org/).

    ```bash
    # apt-get install pass
    ```

3. Set up native host messaging _(this process will be automated with a bash script later)_.

    a. Visit the [extensions](chrome://extensions) page.

    b. Enable `Developer mode`.

    c. Click `Load unpacked extension...` and browse to the extensions folder.

    d. Create a manifest file to register the host application at `~/.config/chromium/NativeMessagingHosts/com.leoxiong.chromepass.json` with the following contents, where `extension id` is the Chrome extension ID.

    ```json
    {
      "name": "com.leoxiong.chromepass",
      "description": "hi",
      "path": "/home/leoxiong/workspace/chromepass/host/app.py",
      "type": "stdio",
      "allowed_origins": [
        "chrome-extension://extension id/"
      ]
    }
    ```

    e. Make sure `chromepass.py` has execute permissions.

    f. Restart Chrome. If the native messaging host has not been successfully registered, kill all instances of chrome and start with debugging enabled `--enable-logging --v=1`.

### How it works

_Write this later._

### Todo / wishlist

_This is currently a work in progress._

### Bugs and feature requests

If there are any bugs, feel free to submit a pull request or contact me at [hello@leoxiong.com](mailto:hello@leoxiong.com).