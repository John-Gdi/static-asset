# Static Asset Sharing

## Usage

通过本仓库提交`mp4`、`gif`等多媒体数据，以便通过`azure devops`的地址快速访问。


#### url是什么

例如，当我们在`gif`文件夹下提交了`signal-event.gif`文件，可以通过以下`url`访问：

```
https://dev.azure.com/gdidev/StaticAssets/_apis/git/repositories/StaticAssets/items?path=/gif/signal-event.gif&resolveLfs=true&%24format=octetStream
```

这里需替换`https://dev.azure.com/gdidev/StaticAssets/_apis/git/repositories/StaticAssets/items?path= [/gif/signal-event.gif] &resolveLfs=true&%24format=octetStream` 中的文件路径。

## 确保已安装lfs
本项目已启用`lfs`，请在执行`git add`前确保已经安装`lfs`。如果没有安装，可通过以下命令完成安装：

```
git lfs install
```