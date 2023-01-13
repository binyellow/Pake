### 1. Fork this project

[Fork this project](https://github.com/tw93/Pake/fork)

### 2. Go to the actions page to enable GitHub actions
- Enter the project settings, Actions, Genneral, Workflow permissions, and check "Read and write permissions" and "Allow GitHub Actions to create and approve pull requests", you can use url `https://github.com/[YourUserName]/Pake/settings/actions` to quickly enter the settings.
![image](https://user-images.githubusercontent.com/28218658/211955296-b734f7bb-78e4-4cb4-9dc0-824850344e2b.png)

### 3. Modify the app.csv file

![image-20221205230432205](https://gw.alipayobjects.com/zos/k/pake/assets/image-20221205230432205.png)

Modify the app.csv file and replace the content after the second line with custom content

![image-20221205230553980](https://gw.alipayobjects.com/zos/k/pake/assets/image-20221205230553980.png)

The format is: `Linux application name, Mac and Windows application name, Chinese character name, URL`, pay attention to use English commas to separate, and `the linux package name must be in lowercase or lowercase-lowercase format`.

### 4. Upload icon
- Recommend https://icon-icons.com/ to generate .icns,.ico,.png icons.
- Upload the .icns file to the `/src-tauri/icons` directory.
- Upload the .ico and .png files to the `/src-tauri/png` directory.

**Note: Two .ico files and one .png file are required, refer to the table below, If not, the default will be used.**

| File Name   | Description                        |
| ----------- | ---------------------------------- |
| app_32.ico  | A ico file with a size of 32\*32   |
| app_256.ico | A ico file with a size of 256\*256 |
| app_512.png | A png file with a size of 512\*512 |

### 5. Advanced configuration
You can find the file `src-tauri/tauri.conf.json`, these three fields can be modified.
1. transparent：If your page does not have the top title bar adaptation, it is recommended to change it to `false`, which will be normal.
2. width：The width of the window is too long and too narrow, which can be modified.
3. height：The height of the window is too long and too narrow, which can be modified.

### 5. Publish to start running automatic compilation

- Click to go to the Releases page

![image-20221205233722029](https://cdn.fliggy.com/upic/rkxpzA.png)

- Click **Create a new release**

![image-20221205233806355](https://gw.alipayobjects.com/zos/k/pake/assets/image-20221205233806355.png)

- Click **Choose a tag** and enter `V0.1.0` (the version number can be customized, but **must start with a capital V**)

![image-20221205233956978](https://gw.alipayobjects.com/zos/k/pake/assets/image-20221205233956978.png)

- Click the **Create new tag** button below

![image-20221205234436283](https://gw.alipayobjects.com/zos/k/pake/assets/image-20221205234436283.png)

- Fill in title and content (optional)
- If you are not modifying in the `master` branch, you need to select the corresponding branch in the target drop-down bar
- Click **Publish release**
- At this point, go to the actions page and make sure the new workflows appear

![image-20221205234306770](https://gw.alipayobjects.com/zos/k/pake/assets/image-20221205234306770.png)

After the compilation is completed, you can see the files generated after the compilation is completed on the release page (compilation takes about 10-30 minutes)