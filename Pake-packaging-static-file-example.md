1. Find a static directory, such as [AriaNG](https://github.com/mayswind/AriaNg/releases/download/1.3.6/AriaNg-1.3.6.zip), and unzip it.

2. Make sure that `pake-cli >= 2.3.3` is installed. If you are not sure what version you have, you can use `pake --version` to determine it.

3. Execute the following command to package the static files. The startup file is usually index.html. Of course, it may be other files. It depends on the front end.
    ```bash
    pake ./AriaNg-1.3.6/index.html --name html-test --iter-copy-file
    ```
    - `--name` is to set the package name. Generally speaking, there are certain standards. To put it simply, try to use English, or `-`, without spaces, and do not use capital letters in Linux.

    - `--iter-copy-file` is a recursive copy, which will copy files at the same level and subdirectories of index.html

4. Then it will be packaged. After successful packaging, the final file will be generated in the current directory.

5. If you need other settings, such as icons, etc., you can refer to [bin/README.md](https://github.com/tw93/Pake/blob/master/bin/README.md).