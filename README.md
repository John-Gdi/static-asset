# Static Asset CDN Sharing

## Usage

通过本仓库提交`mp4`、`gif`等多媒体数据，以便通过`github`的CDN快速访问。


#### url是什么
如果在这个仓库里提交了文件，`pipeline`会自动同步文件至`github`。如上传了`gif/default-vr-itr.gif`文件，那么提交完成后，可以通过以下路径访问该资源：

```
https://media.githubusercontent.com/media/John-Gdi/static-asset/main/gif/default-vr-itr.gif
```

每次我们只需要替换`main`后面的相对路径即可。

## 注意事项

本项目已启用`lfs`，请在执行`git add`前确保已经安装`lfs`。如果没有安装，可通过以下命令完成安装：

```
git lfs install
```