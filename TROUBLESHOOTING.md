# Troubleshooting

This guide is for troubleshooting software on Linux platforms.

## Fail to launch the software

- Since **AppImage** requires FUSE to work properly, you might see `dlopen(): error loading libfuse.so.2` where some distributions does not come with [`FUSE`](https://packages.debian.org/bookworm/libfuse2) library by default.  For **Ubuntu**, **Debian** and their derivatives, here is the solution to make it works smoothly.

    - Ubuntu (pre-22.04), Debian and their derivatives

        Be sure to check `fuse3` does not exist. Manually install `fuse2` by using the following command

        ```
            sudo apt-get install fuse libfuse2
        ```

    - Ubuntu (>=22.04), Debian and their derivatives

        This is only valid with distributions having `fuse3`. Manually install `fuse2` by using the following command

        ```
            sudo apt install libfuse2
        ```

        **_NOTE:_** Do not by any chance remove or purge `fuse3` library which comes with the system. Many immportant packages depends on it, so you may end up completely crash your system.

    For more information, check the following references:

    - Troubleshooting with AppImage: https://docs.appimage.org/user-guide/troubleshooting/fuse.html
