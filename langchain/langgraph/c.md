** 我想做一个项目：

GitHub Sentinel 是一款开源工具类 AI Agent，专为开发者和项目管理人员设计，能够定期（每日/每周）自动获取并汇总订阅的 GitHub 仓库最新动态。

** 我需要实现的功能：

1. 订阅管理：用户可以订阅感兴趣的 GitHub 仓库，设置更新频率，如每日或每周。
2. 更新获取：GitHub Sentinel 能够定期获取订阅仓库的最新动态，包括新提交、问题、Pull Request 等。
3. 通知系统：当有新的更新时，GitHub Sentinel 会通过邮件、Slack 等方式通知用户。
4. 报告生成：GitHub Sentinel 会调用大模型生成详细的报告，包括新增的 Pull Request、问题、提交等信息。其中大模型可选择不同的大模型。



** 非功能性需求
1.进行初始化配置，使得GItHubSentinel项目能真正运行；
2.以https://github.com/langchain-ai/langchain/ 为例， 获取其最新版本的信息，并调用open-ai gpt4-o汇总成一个报告；
3、需要有良好的LOG, LOG日志采用loguru
4、系统执行支持三种方式，
  a、命令行模式 ,受动态输入的指令，类似 git 的命令行模式，如增加或减少订阅；
  b、scheduler定时执行模式, Scheduler 在后台运行，不阻塞工具 I/O 
  b、基于gradio的图形界面模式。