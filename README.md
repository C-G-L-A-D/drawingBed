# drawingBed - 文章图床仓库（Picgo + Github）
  图片上传 Github 后，可以通过 github 地址进行线上访问查看。![Picgo](https://picgo.app/) 支持多平台一键上传图片，并自动复制图片地址等高效操作。

## 一、创建 Github 仓库
  首先新建一个 Github 仓库用于存储图片文件。仓库名称、描述、开源许可证自定义。但是一定要选择 **公开可见性（Choose visibility: Public** ，这样任何外网才能正常访问图片。
![创建图床仓库](https://gitee.com/roada/drawingBed/raw/main/blog/20260421214945.png)

## 二、下载安装 Picgo
  直接打开 ![Picgo 的 Github](https://github.com/Molunerfinn/PicGo) 链接进行下载，也可以通过镜像站进行下载。
  ![下载方式](https://gitee.com/roada/drawingBed/raw/main/blog/202604212200447.png)

  这里我选择通过 Github 进行下载，根据自己电脑的版本进行下载即可。
  ![Picgo安装版本](https://gitee.com/roada/drawingBed/raw/main/blog/202604212204025.png)

  mac 系统下载 dmg 安装包完成后，打开安装包，将应用拖到文件夹进行安装。
  ![安装Picgo](https://gitee.com/roada/drawingBed/raw/main/blog/202604212205889.png)

  首次打开 Picgo 需要同意打开互联网下载的应用。打开后右上角有个 Picgo 的图标，需要右键点击打开主面板（Open Main Window)。
  ![Picgo 主界面](https://gitee.com/roada/drawingBed/raw/main/blog/Picgo主界面.png)
    
  打开主界面后可以在左边菜单栏点击 Picgo Setting 设置汉化。
  ![Picgo 汉化设置](https://gitee.com/roada/drawingBed/raw/main/blog/20260421221746769.png)

## 三、配置 Picgo 图床
  我们使用 Github 作为图床，需要创建 token 允许 Pigco 进行上传、删除等操作。因此，先打开 Github ，点击右上角自己的头像打开用户导航菜单，进入 Setting 设置界面。
  ![Github 用户导航菜单](https://gitee.com/roada/drawingBed/raw/main/blog/20260421223111061.png)

  然后从左边菜单中，找到 Developer Setting 项，点击进入。 
  ![用户设置页菜单栏](https://gitee.com/roada/drawingBed/raw/main/blog/20260421223427548.png)

  接着点击左侧菜单栏的 Personal access tokens 项，在展开的二级菜单中点击 Tokens (classic) 项新建 Token 访问令牌。这里我们选择创建通用 Token 即可。
  （Personal access tokens -> Tokens (classic) -> Generate new toen -> Generate new toen(classic)）
  ![个人访问令牌页面](https://gitee.com/roada/drawingBed/raw/main/blog/20260421224139959.png)

  创建新 Token，建议备注 Token 用途，这样以后管理方便一些。Token 使用期限可以选择永不过期，但是建议还是选择一个有效期。因为这个 Token 只用于图床操作，所以访问权限选择仓库管理就可以了，避免权限过高引发其他问题。
  ![新建 Token 页面](https://gitee.com/roada/drawingBed/raw/main/blog/创建新token.png)

  创建成功后，需要 **立即复制 Token 进行保存** ，否则退出目前页面将无法再看到该 Token 的值。
  [![Token 创建成功页面](https://gitee.com/roada/drawingBed/raw/main/blog/Github新建Token成功.png)

  打开 Picgo 主面板，在菜单栏中找到图床设置 -> Github 新建一个配置。
  ![Picgo 配置 Github](https://gitee.com/roada/drawingBed/raw/main/blog/Picgo配置Github图床.png)

  **图床配置名。** 可以任意填写，主要用于 Picgo 显示区分；
  **设定仓库名。** 要填写图床指定仓库，即步骤一新建的仓库。填写格式为：Github用户名/仓库名称，这样才能区分上传的仓库。可以打开自己的 Github 图床仓库，从浏览器输入框的路径中复制；
  **设定分支名。** 通常填写默认的 main 分支即可，如有需要自行填写待存储的分支；
  **设定存储路径。** 可不填写。如果需要区分图片用途或使用位置，可以将不同类型图片保存在不同路径。例如博客图片，可以填写 `blog/` ,这样使用该图床配置上传的图片，都会上传到图床仓库下的 blog 目录里。
  ![Picgo 图床配置](https://gitee.com/roada/drawingBed/raw/main/blog/20260422001133622.png)

  保存配置后，可以将该配置设置为默认图床。


## 四、Picgo 的其余便捷配置
  在 Picgo 设置 中可以选择开机自启动、自定义图片链接格式、上传前重命名、时间戳重命名、上传后自动复制链接、通过内置剪贴板自动上传等功能。

### Typora 内置 Picgo
  Typora 可以内置 Picgo 插件，只要在文档编辑时贴上图片，就可以将图片自动上传图床，并将图片链接自动替换。
  打开 Typora 设置界面，点击图片菜单项，在上传服务中选择 Picgo.app 项。
  （设置 -> 图片 -> 上传服务 -> Picgo.app）
  ![Typora配置Picgo](https://gitee.com/roada/drawingBed/raw/main/blog/Typora配置Picgo.png)

  可以通过验证图片上传按钮测试能否正常使用。测试成功将会显示以下弹窗：
  ![Typora图床上传验证成功](https://gitee.com/roada/drawingBed/raw/main/blog/Typora图床上传验证成功.png)


