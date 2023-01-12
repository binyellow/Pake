### 1.Fork 本项目

[点击这里](https://github.com/tw93/Pake/fork)

### 2.前往 actions 页面启用 GitHub actions
- 进入项目settings,Actions,Genneral,Workflow permissions,勾选"Read and write permissions"与“Allow GitHub Actions to create and approve pull requests”，可以通过链接`https://github.com/[你的用户名]/Pake/settings/actions`快速进入设置。

![image](https://user-images.githubusercontent.com/28218658/211955222-812a8807-1c1d-49ae-a144-e9fe6e6e9fe9.png)

### 3.修改 app.csv 文件

![image-20221205230432205](https://cdn.fliggy.com/upic/yT0k9N.png)

第二行以后的内容替换成自定义内容，格式为：`Linux下应用名称,Mac和Windows下应用名称,中文名称,网址`，注意使用英文逗号分隔

![image-20221205230553980](https://cdn.fliggy.com/upic/lKRei1.png)

### 4.上传图标
- 推荐用 <https://icon-icons.com/zh/> ，生成 .icns、.ico、.png图标
- 上传.icns 文件至`/src-tauri/icons`目录下（必须，打包mac应用）
- 上传.ico 和.png 文件至`/src-tauri/png`目录下（打包windows/linux是需要的）

**注意：需要两个.ico 文件和一个.png 文件，参考下表，命名和自己的小写命名一致即可**

| 文件名称    | 说明                 |
| ----------- | -------------------- |
| app_32.ico  | 32\*32 的 ico 图标   |
| app_256.ico | 256\*256 的 ico 图标 |
| app_512.png | 512\*512 的 png 图片 |

### 5.发布以开始运行自动编译

- 点击前往 Releases 页面

![image-20221205233624044](https://gw.alipayobjects.com/zos/k/pake/assets/image-20221205233624044.png)

![image-20221205233722029](https://gw.alipayobjects.com/zos/k/pake/assets/image-20221205233722029.png)

- 点击**Create a new release**

![image-20221205233806355](https://gw.alipayobjects.com/zos/k/pake/assets/image-20221205233806355.png)

- 点击**Choose a tag**，输入`V0.1.0`（版本号可自定义，但是**必须以大写 V 开头**）

![image-20221205233956978](https://gw.alipayobjects.com/zos/k/pake/assets/image-20221205233956978.png)

- 点击下方的**Create new tag**按钮

![image-20221205234436283](https://gw.alipayobjects.com/zos/k/pake/assets/image-20221205234436283.png)

- 填写标题和内容（可选）
- 如果不是在`master`分支修改，需要在 target 下拉栏选择对应分支
- 点击**Publish release**
- 此时，前往 actions 页面，确保出现新 workflows，此处只需要看 Build App 这个即可

![image-20221205234306770](https://cdn.fliggy.com/upic/uwPGFk.png)

在编译完成后，即可在 release 页面看到编译完成后生成的文件（编译大约需要 10-30 分钟）
