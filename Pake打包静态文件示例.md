1. 找一个静态目录，比如[AriaNG](https://github.com/mayswind/AriaNg/releases/download/1.3.6/AriaNg-1.3.6.zip),将其解压。

2. 确保已安装`pake-cli >= 2.3.3`，不确定自己是什么版本可以用`pake --version`确定。

3. 执行下面的命令打包静态文件，启动文件一般是index.html，当然也可能是其它的，看前端咯。
```bash
pake ./AriaNg-1.3.6/index.html  --name html-test --iter-copy-file
```
- `--name`是设置包名，一般来说有一定的规范，简单来说就是尽量用英文，或者`-`，不要空格，Linux也不要用大写。

- `--iter-copy-file`是递归拷贝，会拷贝index.html的同级文件和子目录文件

4. 然后就会打包了，打包成功后将会在当前目录生成最终文件。

5. 如果还需要其他设置，比如图标等，可以参考[bin/README_CN.md](https://github.com/tw93/Pake/blob/master/bin/README_CN.md)。
