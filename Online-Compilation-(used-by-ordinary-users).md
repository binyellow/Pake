### 1. Fork this project

[Click here](https://github.com/tw93/Pake/fork)

### 2. Go to Actions
- Click to go to the Actions interface, select `Build App with Pake-Cli`, fill in the form information, and click `Run Workflow`.
- The form parameters and filling requirements are basically consistent with the parameters of the pake-cli. For details, please refer to the pake-cli documentation [link](https://github.com/tw93/Pake/blob/master/bin/README.md#usage).
![image](https://user-images.githubusercontent.com/28218658/224034379-40d623ed-df91-4006-835d-ee852fcb55d4.png)

### 3. Download the attachment
- If the small green icon appears, it means that the packaging is successful. You can click `Build App with Pake-Cli` to view the packaging details and attachments.
![image](https://user-images.githubusercontent.com/28218658/224034726-6d17f899-cc2e-46d9-ac5b-68a8b28f231c.png)
- You can see that there is a 1 in `Artfacts` here, which means that there is an attachment available for download.
![image](https://user-images.githubusercontent.com/28218658/224035345-1acc86c3-8dcd-414e-aa88-ddd96a183876.png)
- Click `Artfacts`, it will automatically jump to the bottom, you can see the final attachment information, click the attachment name to download it officially.
![image](https://user-images.githubusercontent.com/28218658/223757788-08f9ce71-d2ae-49f8-b2a5-debbb9214bc2.png)


### 4. About running time (simple understanding is enough)
- The first run will be relatively slow, about 10-15 minutes, after the subsequent cache, it will be much faster.
- Try to ensure that the first run is complete, so that the generated cache can save a lot of time. If the run fails, the generated cache is incomplete, and the subsequent acceleration cannot be achieved.
- You can view the cache on the page in the lower left corner of Actions, generally named `[Package Platform]-cargo-xxxx`, generally between 400M-600M, if the cache is small, only tens of M, you can click the delete button on the right Delete the cache, then the next build will automatically generate a new cache instead.
![image](https://user-images.githubusercontent.com/28218658/224035969-39d331b4-f9aa-4104-b05a-36525b1b01d4.png)
