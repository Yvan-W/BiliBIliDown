Description:
  BBDown是一个免费且便捷高效的哔哩哔哩下载/解析软件.

Usage:
  BBDown <url> [command] [options]

Arguments:
  <url>  视频地址 或 av|bv|BV|ep|ss

Options:
  -tv, --use-tv-api                              使用TV端解析模式
  -app, --use-app-api                            使用APP端解析模式
  -intl, --use-intl-api                          使用国际版解析模式
  --use-mp4box                                   使用MP4Box来混流
  --encoding-priority <encoding-priority>        视频编码的选择优先级, 用逗号分割 例: "hevc,av1,avc"
  --dfn-priority <dfn-priority>                  画质优先级,用逗号分隔 例: "8K 超高清, 1080P 高码率, HDR 真彩, 杜比视界"
  -info, --only-show-info                        仅解析而不进行下载
  --show-all                                     展示所有分P标题
  --use-aria2c                                   调用aria2c进行下载(你需要自行准备好二进制可执行文件)
  -ia, --interactive                             交互式选择清晰度
  -hs, --hide-streams                            不要显示所有可用音视频流
  -mt, --multi-thread                            使用多线程下载(默认开启)
  --video-only                                   仅下载视频
  --audio-only                                   仅下载音频
  --sub-only                                     仅下载字幕
  --debug                                        输出调试日志
  --skip-mux                                     跳过混流步骤
  --skip-subtitle                                跳过字幕下载
  --skip-cover                                   跳过封面下载
  --force-http                                   下载音视频时强制使用HTTP协议替换HTTPS(默认开启)
  -dd, --download-danmaku                        下载弹幕
  --skip-ai                                      跳过AI字幕下载
  --bandwith-ascending                           比特率升序(最小体积优先)
  -F, --file-pattern <file-pattern>              使用内置变量自定义单P存储文件名:

                                                 <videoTitle>: 视频主标题
                                                 <pageNumber>: 视频分P序号
                                                 <pageNumberWithZero>: 视频分P序号(前缀补零)
                                                 <pageTitle>: 视频分P标题
                                                 <aid>: 视频aid
                                                 <cid>: 视频cid
                                                 <dfn>: 视频清晰度
                                                 <res>: 视频分辨率
                                                 <fps>: 视频帧率
                                                 <videoCodecs>: 视频编码
                                                 <videoBandwidth>: 视频码率
                                                 <audioCodecs>: 音频编码
                                                 <audioBandwidth>: 音频码率
                                                 <ownerName>: 上传者名称
                                                 <ownerMid>: 上传者mid

                                                 默认为: <videoTitle>
  -M, --multi-file-pattern <multi-file-pattern>  使用内置变量自定义多P存储文件名:

                                                 默认为: <videoTitle>/[P<pageNumberWithZero>]<pageTitle>
  -p, --select-page <select-page>                选择指定分p或分p范围: (-p 8 或 -p 1,2 或 -p 3-5 或 -p ALL 或 -p LAST)
  --language <language>                          设置混流的音频语言(代码), 如chi, jpn等
  -c, --cookie <cookie>                          设置字符串cookie用以下载网页接口的会员内容
  -token, --access-token <access-token>          设置access_token用以下载TV/APP接口的会员内容
  --aria2c-args <aria2c-args>                    调用aria2c的附加参数(默认参数包含"-x16 -s16 -j16 -k 5M", 使用时注意字符串转义)
  --work-dir <work-dir>                          设置程序的工作目录
  --ffmpeg-path <ffmpeg-path>                    设置ffmpeg的路径
  --mp4box-path <mp4box-path>                    设置mp4box的路径
  --aria2c-path <aria2c-path>                    设置aria2c的路径
  --delay-per-page <delay-per-page>              设置下载合集分P之间的下载间隔时间(单位: 秒, 默认无间隔)
  --host <host>                                  指定BiliPlus host(解析服务器能够获取你账号的大部分权限!)
  --ep-host <ep-host>                            指定BiliPlus EP host
  --area <area>                                  指定BiliPlus area 例: hk(使用BiliPlus需要access_token, 不需要cookie)
  --config-file <config-file>                    读取指定的BBDown本地配置文件(默认为: BBDown.config)
  --version                                      Show version information
  -?, -h, --help                                 Show help and usage information


Commands:
  login    通过APP扫描二维码以登录您的WEB账号
  logintv  通过APP扫描二维码以登录您的TV账号
