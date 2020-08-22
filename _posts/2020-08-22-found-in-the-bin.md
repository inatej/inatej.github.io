# 「垃圾桶里捡来的」
作为 blog 的第一篇博文，以”Hello World!”为标题可能被误以为是程序自动生成的 placeholder，所以思来想去，还是打算写一下这个 blog 的搭建过程作为第一篇博文；而标题「垃圾桶里捡来的」这句话则是在 PRC 严重缺乏性教育的背景下，常常被父母们用来搪塞孩子们对自己诞生方式的询问。

此 blog 是借助 GitHub 提供的 [GitHub Pages](https://pages.github.com/) 功能实现的，搭建的主要过程参考了发表于少数派的[一篇文章](https://sspai.com/post/54608)。

出于各方面的考量，我注册了专门用于管理这个 blog 的 GitHub 账号。登入账号后，首先[创建一个新的 repository](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/creating-a-new-repository)，只需将 Repository name 更改为 `your-account.github.io`，其他选项保持默认，然后创建新的 repository。

页面会自动跳转到你所创建的 repository，进入 Settings，找到 Theme Chooser 进入选择主题的界面。在默认的几个主题中随意选择一个（因为在后面我们会用其他工具来控制主题），选好后在自动跳转的界面点选 Commit changes。之后使用 repository name 里所填写的网址即可访问你的主页。

下面需要安装 [GitHub Desktop](https://desktop.github.com/) 从而更方便地管理网站。在连接 GitHub 账号等操作后对之前创建的 repository 进行 Clone 的操作，Clone 到本地的路径需要记好，之后会用到。

以 macOS为例，接着使用 Terminal 依次安装 Ruby 和 Jekyll：

`brew install ruby` （这里使用了包管理器 [Homebrew](https://brew.sh/) 进行安装）

`sudo gem install Jekyll bundler`

然后进入 repository 的本地路径，一般是：

`cd ~/Documents/GitHub/your-account.github.io`

接着执行：

`jekyll new . --force` 

这会创建一系列新的文件，此时可以执行 `bundle exec Jekyll serve` 来预览创建好了的网页，访问地址为：`http://127.0.0.1:4000`

你可以在 `your-account.github.io` 这个文件夹中找到 `_config.yml` 文件，通过编辑相应条目，可调整网页中的各个元素，详细内容见 [Jekyll 的官方文档](https://jekyllrb.com/docs/configuration/)。当然你还可以自由[变更网页的主题](https://jekyllrb.com/docs/themes/)。

在完成这些操作后，你可以在 GitHub Desktop 中将这些文件的变动同步到云端：软件会自动发现你变更的文件，你只需要编辑 Summary，再点选 Commit to master，然后点选 Fetch origin。一般需要等待几分钟，你就会在 your-account.github.io 上看到更新后的页面。

以上是通过 GitHub Pages 和 Jekyll 架设一个简单的 blog 的过程，下面便是最重要的一步：发布博文。

推荐使用 Markdown 编辑器来编辑博文，如 [Typora](https://typora.io/)、[MWeb](https://www.mweb.im/)，但不推荐使用 [Bear](https://bear.app)，因为它所导出的 `.md` 文件并非「所见即所得」，如果您是 Bear 的用户，可以尝试一下。另外需要注意以下几点：

1. 文件需要以 `yyyy-MM-dd-yourTitle.markdown` 或 `yyyy-MM-dd-yourTitle.md` 的形式保存。
2. 文件需保存于 `your-account.github.io` 文件夹下的 `_posts` 文件夹中。

- - - -


我在几年之前也尝试过用类似的工具搭建个人 blog，可惜当时只是为了尝试其中的「技术」（可能用「操作」更准确），在搭建好后也没有写多少东西。而这次尝试使用了尽量简单的方式、配合更加简单的主题，希望在此之后能有真正的产出。

