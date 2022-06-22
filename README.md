# Static Asset Sharing

## Usage

通过本仓库提交`mp4`、`gif`等多媒体数据，以便通过`github`的CDN快速访问。


#### url是什么
如果在这个仓库里提交了文件，`pipeline`会自动同步文件至`github`。如上传了`gif/default-vr-itr.gif`文件，那么提交完成后，可以通过以下路径访问该资源：

```
https://media.githubusercontent.com/media/John-Gdi/static-asset/main/gif/default-vr-itr.gif
```

每次我们只需要替换`main`后面的相对路径即可。

## 注意事项

#### 使用Azure Repos路径

由于`github`的`lfs`只提供`1GB`的存储空间，当超过的时候会无法使用。可考虑使用`Azure Devops`的路径。

```
https://dev.azure.com/gdidev/StaticAssets/_apis/git/repositories/StaticAssets/items?path=/gif/signal-event.gif&resolveLfs=true&%24format=octetStream
```

这里需替换`https://dev.azure.com/gdidev/StaticAssets/_apis/git/repositories/StaticAssets/items?path= [/gif/signal-event.gif] &resolveLfs=true&%24format=octetStream` 中的文件路径。

#### 确保已安装lfs
本项目已启用`lfs`，请在执行`git add`前确保已经安装`lfs`。如果没有安装，可通过以下命令完成安装：

```
git lfs install
```