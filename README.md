# Bilibili Comment Downloader

主要基于`requests`库，通过Bilibili的评论api爬取视频评论、点赞数以及评论回复

## 使用方法

- 首先需要在`fetch_bilibili_comments.py`脚本开头定义的`HEADERS`变量中添加自己的Cookie
- 然后运行脚本，控制台会出现提示：“Please input the title or the link of the video: ”，输入视频**标题**或者**链接**后，控制台会打印出搜索到的视频标题，确认无误后输入“y”继续；如果搜索到的视频有误，输入“n”退出
- 确认视频标题后自动爬取该视频所有的评论及评论回复，并在**脚本所在目录**下保存csv格式的结果，文件名为`视频标题_comments.csv`
- 如果出现`CookieError`，可能是Cookie有误或过期，需要重新配置Cookie

该脚本使用到的Python非标准库有：

- `pandas`
- `requests`
- `lxml`

## 结果示例

输出结果包含5列，分别为`用户名称`、`用户性别`、`评论内容`、`点赞数`和`评论回复`

![example](https://github.com/lvlh2/BilibiliCommentFetcher/blob/main/example.png)
