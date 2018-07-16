python 资源大全中文版 我想很多程序员应该记得 github 上有一个 awesome xxx 系列的资源整理。awesome python 是 vinta 发起维护的 python 资源列表，内容包括：web 框架、网络爬虫、网络内容提取、模板引擎、数据库、数据可视化、图片处理、文本处理、自然语言处理、机器学习、日志、代码分析等。由伯乐在线持续更新。 awesome 系列虽然挺全，但基本只对收录的资源做了极为简要的介绍，如果有更详细的中文介绍，对相应开发者的帮助会更大。这也是我们发起这个开源项目的初衷。 关于项目 我们要做什么？ 基于 awesome python 列表，我们将对其中的各个资源项进行编译整理。此外还将从其他来源补充好资源。 整理后的内容，将收录在伯乐在线资源频道。可参考已整理的内容： 《scrapy：python 的爬虫框架》 《flask：一个使用 python 编写的轻量级 web 应用框架》 如何为列表贡献新资源？ 欢迎大家为列表贡献高质量的新资源，提交 pr 时请参照以下要求： 请确保推荐的资源自己使用过 提交 pr 时请注明推荐理由 资源列表管理收到 pr 请求后，会定期（每周）在微博转发本周提交的 pr 列表，并在微博上面听取使用过这些资源的意见。确认通过后，会加入资源大全。 感谢您的贡献！ 本项目的参与者 维护者： 贡献者：艾凌风、namco、daetalus、黄利民、atupal、rainbow、木头lbj、beyondwu、cissoid、李广胜、polyval、冰斌、赵叶宇、л stalgic、硕恩、strongit、yuukilp、chenjiandongx、autopenguin、visonforcoding、super赛亚人、since future、knktc 注：名单不分排名，不定期补充更新 资源列表 环境管理 管理 python 版本和环境的工具 p：非常简单的交互式 python 版本管理工具。官网 pyenv：简单的 python 版本管理工具。官网 vex：可以在虚拟环境中执行命令。官网 virtualenv：创建独立 python 环境的工具。官网 virtualenvwrapper：virtualenv 的一组扩展。官网 包管理 管理包和依赖的工具。 pip：python 包和依赖关系管理工具。官网 pip tools：保证 python 包依赖关系更新的一组工具。官网 pipenv：pyhton 官方推荐的新一代包管理工具。官网 conda：跨平台，python 二进制包管理工具。官网 curdling：管理 python 包的命令行工具。官网 wheel：python 分发的新标准，意在取代 eggs。官网 包仓库 本地 pypi 仓库服务和代理。 warehouse：下一代 pypi。官网 bandersnatch：pypa 提供的 pypi 镜像工具。官网 devpi：pypi 服务和打包 测试 分发工具。官网 localshop：本地 pypi 服务（自定义包并且自动对 pypi 镜像）。官网 分发 打包为可执行文件以便分发。 pyinstaller：将 python 程序转换成独立的执行文件（跨平台）。官网 dh virtualenv：构建并将 virtualenv 虚拟环境作为一个 debian 包来发布。官网 nuitka：将脚本、模块、包编译成可执行文件或扩展模块。官网 py2app：将 python 脚本变为独立软件包（mac os x）。官网 py2exe：将 python 脚本变为独立软件包（windows）。官网 pynsist：一个用来创建 windows 安装程序的工具，可以在安装程序中打包 python 本身。官网 构建工具 将源码编译成软件。 buildout：一个构建系统，从多个组件来创建，组装和部署应用。官网 bitbake：针对嵌入式 linux 的类似 make 的构建工具。官网 fabricate：对任何语言自动找到依赖关系的构建工具。官网 platformio：多平台命令行构建工具。官网 pybuilder：纯 python 实现的持续化构建工具。官网 scons：软件构建工具。官网 交互式解析器 交互式 python 解析器。 ipython：功能丰富的工具，非常有效的使用交互式 python。官网 bpython：界面丰富的 python 解析器。官网 ptpython：高级交互式 python 解析器， 构建于 python prompt toolkit 之上。官网 文件 文件管理和 mime（多用途的网际邮件扩充协议）类型检测。 aiofiles：基于 asyncio，提供文件异步操作。官网 imghdr：（python 标准库）检测图片类型。官网 mimetypes：（python 标准库）将文件名映射为 mime 类型。官网 path py：对 os path 进行封装的模块。官网 pathlib：（python3 4 标准库）跨平台的、面向对象的路径操作库。官网 python magic：文件类型检测的第三方库 libmagic 的 python 接口。官网 unipath：用面向对象的方式操作文件和目录。官网 watchdog：管理文件系统事件的 api 和 shell 工具。官网 日期和时间 操作日期和时间的类库。 arrow：更好的 python 日期时间操作类库。官网 chronyk：python 3 的类库，用于解析手写格式的时间和日期。官网 dateutil：python datetime 模块的扩展。官网 delorean：解决 python 中有关日期处理的棘手问题的库。官网 maya：人性化的时间处理库。官网 moment：一个用来处理时间和日期的 python 库。灵感来自于 moment js。官网 pendulum：一个比 arrow 更具有明确的，可预测的行为的时间操作库。官网 pytime：一个简单易用的 python 模块，用于通过字符串来操作日期 时间。官网 pytz：现代以及历史版本的世界时区定义。将时区数据库引入 python。官网 when py：提供用户友好的函数来帮助用户进行常用的日期和时间操作。官网 文本处理 用于解析和操作文本的库。 通用 chardet：字符编码检测器，兼容 python2 和 python3。官网 difflib： python 标准库 帮助我们进行差异化比较。官网 ftfy：让 unicode 文本更完整更连贯。官网 fuzzywuzzy：模糊字符串匹配。官网 levenshtein：快速计算编辑距离以及字符串的相似度。官网 pangu py：在中日韩语字符和数字字母之间添加空格。官网 pypinyin：汉字拼音转换工具 python 版。官网 shortuuid：一个生成器库，用以生成简洁的，明白的，url 安全的 uuid。官网 simplejson：python 的 json 编码、解码器。官网 unidecode：unicode 文本的 ascii 转换形式 。官网 uniout：打印可读的字符，而不是转义的字符串。官网 xpinyin：一个用于把汉字转换为拼音的库。官网 yfiglet figlet：pyfiglet figlet 的 python 实现。 flashtext 一个高效的文本查找替换库。官网 slug 化 awesome slugify：一个 python slug 化库，可以保持 unicode。官网 python slugify：python slug 化库，可以把 unicode 转化为 ascii。官网 unicode slugify：一个 slug 工具，可以生成 unicode slugs 需要依赖 django 。官网 解析器 phonenumbers：解析，格式化，储存，验证电话号码。官网 ply：lex 和 yacc 解析工具的 python 实现。官网 pygments：通用语法高亮工具。官网 pyparsing：生成通用解析器的框架。官网 python nameparser：把一个人名分解为几个独立的部分。官网 python user agents：浏览器 user agent 解析器。官网 sqlparse：一个无验证的 sql 解析器。官网 特殊文本格式处理 一些用来解析和操作特殊文本格式的库。 通用 tablib：一个用来处理中表格数据的模块。官网 office marmir：把输入的 python 数据结构转换为电子表单。官网 openpyxl：一个用来读写 excel 2010 xlsx xlsm xltx xltm 文件的库。官网 pyexcel：一个提供统一 api，用来读写，操作 excel 文件的库。官网 python docx：读取，查询以及修改 microsoft word 2007 2008 docx 文件。官网 relatorio：模板化 opendocument 文件。官网 unoconv：在 libreoffice openoffice 支持的任意文件格式之间进行转换。官网 xlsxwriter：一个用于创建 excel xlsx 文件的 python 模块。官网 xlwings：一个使得在 excel 中方便调用 python 的库（反之亦然），基于 bsd 协议。官网 xlwt：读写 excel 文件的数据和格式信息。官网 xlrd pdf pdfminer：一个用于从 pdf 文档中抽取信息的工具。官网 pypdf2：一个可以分割，合并和转换 pdf 页面的库。官网 reportlab：快速创建富文本 pdf 文档。官网 markdown mistune：快速并且功能齐全的纯 python 实现的 markdown 解析器。官网 python markdown：john grubers markdown 的 python 版实现。官网 python markdown2：纯 python 实现的 markdown 解析器，比 python markdown 更快，更准确，可扩展。官网 yaml pyyaml：python 版本的 yaml 解析器。官网 csv csvkit：用于转换和操作 csv 的工具。官网 archive unp：一个用来方便解包归档文件的命令行工具。官网 自然语言处理 用来处理人类语言的库。 nltk：一个先进的平台，用以构建处理人类语言数据的 python 程序。官网 jieba：中文分词工具。官网 langid py：独立的语言识别系统。官网 pattern：python 网络信息挖掘模块。官网 snownlp：一个用来处理中文文本的库。官网 textblob：为进行普通自然语言处理任务提供一致的 api。官网 textgrocery：一简单高效的短文本分类工具，基于 liblinear 和 jieba。官网 thulac 清华大学自然语言处理与社会人文计算实验室研制推出的一套中文词法分析工具包官网 文档 用以生成项目文档的库。 sphinx：python 文档生成器。官网 awesome sphinxdoc：官网 mkdocs：对 markdown 友好的文档生成器。官网 pdoc：一个可以替换 epydoc 的库，可以自动生成 python 库的 api 文档。官网 pycco：文学编程（literate programming）风格的文档生成器。官网 readthedocs：一个基于 sphinx mkdocs 的在线文档托管系统，对开源项目免费开放使用。官网 配置 用来保存和解析配置的库。 config：logging 模块作者写的分级配置模块。官网 configobj：ini 文件解析器，带验证功能。官网 configparser： python 标准库 ini 文件解析器。官网 profig：通过多种格式进行配置，具有数值转换功能。官网 python decouple：将设置和代码完全隔离。官网 命令行工具 用于创建命令行程序的库。 命令行程序开发 asciimatics：跨平台，全屏终端包（即鼠标 键盘输入和彩色，定位文本输出），完整的复杂动画和特殊效果的高级 api。官网 cement：python 的命令行程序框架。官网 click：一个通过组合的方式来创建精美命令行界面的包。官网 cliff：一个用于创建命令行程序的框架，可以创建具有多层命令的命令行程序。官网 clint：python 命令行程序工具。官网 colorama：跨平台彩色终端文本。官网 docopt：python 风格的命令行参数解析器。官网 gooey：一条命令，将命令行程序变成一个 gui 程序。官网 python prompt toolkit：一个用于构建强大的交互式命令行程序的库。官网 python fire：google 出品的一个基于 python 类的构建命令行界面的库。官网 pythonpy：在命令行中直接执行任何 python 指令。官网 生产力工具 aws cli：amazon web services 的通用命令行界面。官网 bashplotlib：在终端中进行基本绘图。官网 caniusepython3：判断是哪个项目妨碍你你移植到 python3。官网 cookiecutter：从 cookiecutters（项目模板）创建项目的一个命令行工具。官网 doitlive：一个用来在终端中进行现场演示的工具。官网 pyftpdlib：一个速度极快和可扩展的 python ftp 服务库。官网 howdoi：通过命令行获取即时的编程问题解答。官网 httpie：一个命令行 http 客户端，curl 的替代品，易用性更好。官网 pathpicker：从 bash 输出中选出文件。官网 percol：向 unix shell 传统管道概念中加入交互式选择功能。官网 saws：一个加强版的 aws 命令行。官网 thefuck：修正你之前的命令行指令。官网 mycli：一个 mysql 命令行客户端，具有自动补全和语法高亮功能。官网 pgcli：postgres 命令行工具，具有自动补全和语法高亮功能。官网 try：一个从来没有更简单的命令行工具，用来试用 python 库。官网 下载器 用来进行下载的库 s3cmd：一个用来管理 amazon s3 和 cloudfront 的命令行工具。官网 s4cmd：超级 s3 命令行工具，性能更加强劲。官网 you get：一个 youtube youku niconico 视频下载器，使用 python3 编写。官网 youtube dl：一个小巧的命令行程序，用来下载 youtube 视频。官网 图像处理 用来操作图像的库 pillow：pillow 是一个更加易用版的 pil。官网 hmap：图像直方图映射。官网 imgseek：一个使用视觉相似性搜索一组图片集合的项目。官网 nude py：裸体检测。官网 pybarcode：不借助 pil 库在 python 程序中生成条形码。官网 pygram：类似 instagram 的图像滤镜。官网 python qrcode：一个纯 python 实现的二维码生成器。官网 quads：基于四叉树的计算机艺术。官网 scikit image：一个用于（科学）图像处理的 python 库。官网 thumbor：一个小型图像服务，具有剪裁，尺寸重设和翻转功能。官网 wand：magickwand的 python 绑定。magickwand 是 imagemagick 的 c api 。官网 face recognition：简单易用的 python 人脸识别库。官网 ocr 光学字符识别库。 pyocr：tesseract 和 cuneiform 的一个封装 wrapper 。官网 pytesseract：google tesseract ocr 的另一个封装 wrapper 。官网 python tesseract：google tesseract ocr 的一个包装类。 音频 用来操作音频的库 audiolazy：python 的数字信号处理包。官网 audioread：交叉库 gstreamer core audio mad ffmpeg 音频解码。官网 beets：一个音乐库管理工具及 musicbrainz 标签添加工具。官网 dejavu：音频指纹提取和识别。官网 django elastic transcoder：django amazon elastic transcoder。官网 eyed3：一个用来操作音频文件的工具，具体来讲就是包含 id3 元信息的 mp3 文件。官网 id3reader：一个用来读取 mp3 元数据的 python 模块。官网 m3u8：一个用来解析 m3u8 文件的模块。官网 mutagen：一个用来处理音频元数据的 python 模块。官网 pydub：通过简单、简洁的高层接口来操作音频文件。官网 pyechonest：echo nest api 的 python 客户端。官网 talkbox：一个用来处理演讲 信号的 python 库。官网 timeside：开源 web 音频处理框架。官网 tinytag：一个用来读取 mp3 ogg flac 以及 wave 文件音乐元数据的库。官网 mingus：一个高级音乐理论和曲谱包，支持 midi 文件和回放功能。官网 video 用来操作视频和 gif 的库。 moviepy：一个用来进行基于脚本的视频编辑模块，适用于多种格式，包括动图 gifs。官网 scikit video：scipy 视频处理常用程序。官网 地理位置 地理编码地址以及用来处理经纬度的库。 geodjango：世界级地理图形 web 框架。官网 geoip：maxmind geoip legacy 数据库的 python api。官网 geojson：geojson 的 python 绑定及工具。官网 geopy：python 地址编码工具箱。官网 pygeoip：纯 python geoip api。官网 django countries：一个 django 应用程序，提供用于表格的国家选择功能，国旗图标静态文件以及模型中的国家字段。官网 http 使用 http 的库。 aiohttp：基于 asyncio 的异步 http 网络库。官网 requests：人性化的 http 请求库。官网 grequests：requests 库 gevent ，用于异步 http 请求 官网 httplib2：全面的 http 客户端库。官网 treq：类似 requests 的 python api 构建于 twisted http 客户端之上。官网 urllib3：一个具有线程安全连接池，支持文件 post，清晰友好的 http 库。官网 数据库 python 实现的数据库。 pickledb：一个简单，轻量级键值储存数据库。官网 pipelinedb：流式 sql 数据库。官网 tinydb：一个微型的，面向文档型数据库。官网 zodb：一个 python 原生对象数据库。一个键值和对象图数据库。官网 数据库驱动 用来连接和操作数据库的库。 mysql：awesome mysql 系列 aiomysql：基于 asyncio 的异步 mysql 数据库操作库。官网 mysql python：python 的 mysql 数据库连接器。官网 ysqlclient：mysql python 分支，支持 python 3。 oursql：一个更好的 mysql 连接器，支持原生预编译指令和 blobs。官网 pymysql：纯 python mysql 驱动，兼容 mysql python。官网 postgresql psycopg2：python 中最流行的 postgresql 适配器。官网 queries：psycopg2 库的封装，用来和 postgresql 进行交互。官网 txpostgres：基于 twisted 的异步 postgresql 驱动。官网 其他关系型数据库 apsw：另一个 python sqlite 封装。官网 dataset：在数据库中存储 python 字典 pymssql：一个简单的 microsoft sql server 数据库接口。官网 nosql 数据库 asyncio redis：基于 asyncio 的 redis 客户端 pep 3156 。官网 cassandra python driver：cassandra 的 python 驱动。官网 happybase：一个为 apache hbase 设计的，对开发者友好的库。官网 plyvel：一个快速且功能丰富的 leveldb 的 python 接口。官网 py2neo：neo4j restful 接口的 python 封装客户端。官网 pycassa：cassandra 的 python thrift 驱动。官网 pymongo：mongodb 的官方 python 客户端。官网 redis py：redis 的 python 客户端。官网 telephus：基于 twisted 的 cassandra 客户端。官网 txredis：基于 twisted 的 redis 客户端。官网 orm 实现对象关系映射或数据映射技术的库。 关系型数据库 django models：django 的一部分。官网 sqlalchemy：python sql 工具以及对象关系映射工具。官网 awesome sqlalchemy 系列 peewee：一个小巧，富有表达力的 orm。官网 ponyorm：提供面向生成器的 sql 接口的 orm。官网 python sql：编写 python 风格的 sql 查询。官网 nosql 数据库 django mongodb engine：django mongodb 后端。官网 pynamodb：amazon dynamodb 的一个 python 风格接口。官网 flywheel：amazon dynamodb 的对象映射工具。官网 mongoengine：一个 python 对象文档映射工具，用于 mongodb。官网 hot redis：为 redis 提供 python 丰富的数据类型。官网 redisco：一个 python 库，提供可以持续存在在 redis 中的简单模型和容器。官网 其他 butterdb：google drive 电子表格的 python orm。官网 web 框架 全栈 web 框架。 django：python 界最流行的 web 框架。官网 awesome django 系列 flask：一个 python 微型框架。官网 awesome flask 系列 pyramid：一个小巧，快速，接地气的开源 python web 框架。 awesome pyramid 系列 bottle：一个快速小巧，轻量级的 wsgi 微型 web 框架。官网 cherrypy：一个极简的 python web 框架，服从 http 1 1 协议且具有 wsgi 线程池。官网 turbogears：一个可以扩展为全栈解决方案的微型框架。官网 web py：一个 python 的 web 框架，既简单，又强大。官网 web2py：一个全栈 web 框架和平台，专注于简单易用。官网 tornado：一个 web 框架和异步网络库。官网 sanic：基于 python3 5 的异步网络框架。官网 权限 允许或拒绝用户访问数据或功能的库。 carteblanche：站在用户和设计者角度开发的一个代码对齐模块，很好地处理了代码导航及权限。官网 django guardian：django 1 2 实现了单个对象权限。官网 django rules：一个小巧但是强大的应用，提供对象级别的权限管理，且不需要使用数据库。官网 cms 内容管理系统 odoo cms 一个开源的，企业级 cms，基于 odoo。官网 django cms：一个开源的，企业级 cms，基于 django。官网 djedi cms：一个轻量级但却非常强大的 django cms ，考虑到了插件，内联编辑以及性能。官网 feincms：基于 django 构建的最先进的内容管理系统之一。官网 kotti：一个高级的，python 范的 web 应用框架，基于 pyramid 构建。官网 mezzanine：一个强大的，持续的，灵活的内容管理平台。官网 opps：一个为杂志，报纸网站以及大流量门户网站设计的 cms 平台，基于 django。官网 plone：一个构建于开源应用服务器 zope 之上的 cms。官网 quokka：灵活，可扩展的小型 cms，基于 flask 和 mongodb。官网 wagtail：一个 django 内容管理系统。官网 widgy：最新的 cms 框架，基于 django。官网 电子商务 用于电子商务以及支付的框架和库。 django oscar：一个用于 django 的开源的电子商务框架。官网 django shop：一个基于 django 的店铺系统。官网 cartridge：一个基于 mezzanine 构建的购物车应用。官网 shoop：一个基于 django 的开源电子商务平台。官网 alipay：非官方的 python 支付宝 api。官网 merchant：一个可以接收来自多种支付平台支付的 django 应用。官网 money：一个货币类库。带有可选的 cldr 后端本地化格式，提供可扩展的货币兑换解决方案。官网 python currencies：显示货币格式以及它的数值。官网 restful api 用来开发 restful apis 的库 django django rest framework：一个强大灵活的工具，用来构建 web api。官网 django tastypie：为 django 应用开发 api。官网 django formapi：为 django 的表单验证，创建 json apis 。官网 flask flask api：为 flask 开发的，可浏览 web apis 。官网 flask restful：为 flask 快速创建 rest apis 。官网 flask restless：为 sqlalchemy 定义的数据库模型创建 restful apis 。官网 flask api utils：为 flask 处理 api 表示和验证。官网 eve：rest api 框架，由 flask mongodb 等驱动。官网 pyramid cornice：一个 pyramid 的 rest 框架 。官网 与框架无关的 falcon：一个用来建立云 api 和 web app 后端的高性能框架。官网 sandman：为现存的数据库驱动系统自动创建 rest apis 。官网 restless：框架无关的 rest 框架 ，基于从 tastypie 学到的知识。官网 ripozo：快速创建 rest hateoas hypermedia apis。官网 验证 实现验证方案的库。 oauth authomatic：简单但是强大的框架，身份验证 授权客户端。官网 django allauth：django 的验证应用。官网 django oauth toolkit：为 django 用户准备的 oauth2。官网 django oauth2 provider：为 django 应用提供 oauth2 接入。官网 flask oauthlib：oauth 1 0 a 2 0 客户端实现，供 flask 使用。官网 oauthlib：一个 oauth 请求 签名逻辑通用、 完整的实现。官网 python oauth2：一个完全测试的抽象接口。用来创建 oauth 客户端和服务端。官网 python social auth：一个设置简单的社会化验证方式。官网 rauth：oauth 1 0 a 2 0 和 ofly 的 python 库。官网 sanction：一个超级简单的 oauth2 客户端实现。官网 其他 jose：javascript 对象签名和加密草案的实现。官网 pyjwt：json web 令牌草案 01。官网 python jws：json web 签名草案 02 的实现。官网 python jwt：一个用来生成和验证 json web 令牌的模块。官网 模板引擎 模板生成和词法解析的库和工具。 jinja2：一个现代的，对设计师友好的模板引擎。官网 chameleon：一个 html xml 模板引擎。 模仿了 zpt（zope page templates） 进行了速度上的优化。官网 genshi：python 模板工具，用以生成 web 感知的结果。官网 mako：python 平台的超高速轻量级模板。官网 队列 处理事件以及任务队列的库。 celery：一个异步任务队列 作业队列，基于分布式消息传递。官网 huey：小型多线程任务队列。官网 mrq：mr queue 一个 python 的分布式 worker 任务队列， 使用 redis 和 gevent。官网 rq：简单的 python 作业队列。官网 simpleq：一个简单的，可无限扩张的，基于亚马逊 sqs 的队列。官网 搜索 对数据进行索引和执行搜索查询的库和软件。 django haystack：django 模块化搜索。官网 elasticsearch py：elasticsearch 的官方底层 python 客户端。官网 elasticsearch dsl py：elasticsearch 的官方高级 python 客户端。官网 solrpy：solr 的 python 客户端。官网 whoosh：一个快速的纯 python 搜索引擎库。官网 动态消息 用来创建用户活动的库。 django activity stream：从你的站点行为中生成通用活动信息流。官网 stream framework：使用 cassandra 和 redis 创建动态消息和通知系统。官网 资源管理 管理、压缩、缩小网站资源的工具。 django compressor：将链接和内联的 javascript 或 css 压缩到一个单独的缓存文件中。官网 django storages：一个针对 django 的自定义存储后端的工具集合。官网 fanstatic：打包、优化，并且把静态文件依赖作为 python 的包来提供。官网 file conveyor：一个后台驻留的程序，用来发现和同步文件到 cdns s3 和 ftp。官网 flask assets：帮你将 web 资源整合到你的 flask app 中。官网 jinja assets compressor：一个 jinja 扩展，用来编译和压缩你的资源。官网 webassets：为你的静态资源打包、优化和管理生成独一无二的缓存 url。官网 缓存 缓存数据的库。 beaker：一个缓存和会话库，可以用在 web 应用和独立 python 脚本和应用上。官网 django cache machine：django 模型的自动缓存和失效。官网 django cacheops：具有自动颗粒化事件驱动失效功能的 orm。官网 django viewlet：渲染模板，同时具有额外的缓存控制功能。官网 dogpile cache：dogpile cache 是 beaker 的下一代替代品，由同一作者开发。官网 hermescache：python 缓存库，具有基于标签的失效和 dogpile effect 保护功能。官网 johnny cache：django 应用缓存框架。官网 pylibmc：libmemcached 接口的 python 封装。官网 电子邮件 用来发送和解析电子邮件的库。 django celery ses：带有 aws ses 和 celery 的 django email 后端。官网 envelopes：供人类使用的电子邮件库。官网 flanker：一个 email 地址和 mime 解析库。官网 imbox：python imap 库。官网 inbox py：python smtp 服务器。官网 inbox：一个开源电子邮件工具箱。官网 lamson：python 风格的 smtp 应用服务器。官网 mailjet：mailjet api 实现，用来提供批量发送邮件，统计等功能。官网 marrow mailer：高性能可扩展邮件分发框架。官网 modoboa：一个邮件托管和管理平台，具有现代的、简约的 web ui。官网 pyzmail：创建，发送和解析电子邮件。官网 talon：mailgun 库，用来抽取信息和签名。官网 国际化 用来进行国际化的库。 babel：一个 python 的国际化库。官网 korean：一个韩语词态库。官网 url 处理 解析 urls 的库 furl：一个让处理 url 更简单小型 python 库。官网 purl：一个简单的，不可变的 url 类，具有简洁的 api 来进行询问和处理。官网 pyshorteners：一个纯 python url 缩短库。官网 shorturl：生成短小 url 和类似 bit ly 短链的 python 实现。官网 webargs：一个解析 http 请求参数的库，内置对流行 web 框架的支持，包括 flask django bottle tornado 和 pyramid。官网 html 处理 处理 html 和 xml 的库。 beautifulsoup：以 python 风格的方式来对 html 或 xml 进行迭代，搜索和修改。官网 bleach：一个基于白名单的 html 清理和文本链接库。官网 cssutils：一个 python 的 css 库。官网 html5lib：一个兼容标准的 html 文档和片段解析及序列化库。官网 lxml：一个非常快速，简单易用，功能齐全的库，用来处理 html 和 xml。官网 markupsafe：为 python 实现 xml html xhtml 标记安全字符串。官网 pyquery：一个解析 html 的库，类似 jquery。官网 requests html：人性化的，pythonic 的 html 解析库。官网 untangle：将 xml 文档转换为 python 对象，使其可以方便的访问。官网 xhtml2pdf：html css 转 pdf 工具。官网 xmltodict：像处理 json 一样处理 xml。官网 爬取网络站点的库 scrapy：一个快速高级的屏幕爬取及网页采集框架。官网 cola：一个分布式爬虫框架。官网 demiurge：基于 pyquery 的爬虫微型框架。官网 feedparser：通用 feed 解析器。官网 grab：站点爬取框架。官网 mechanicalsoup：用于自动和网络站点交互的 python 库。官网 portia：scrapy 可视化爬取。官网 pyspider：一个强大的爬虫系统。官网 robobrowser：一个简单的，python 风格的库，用来浏览网站，而不需要一个独立安装的浏览器。官网 网页内容提取 用于进行网页内容提取的库。 haul：一个可以扩展的图像爬取工具。官网 html2text：将 html 转换为 markdown 格式文本。官网 lassie：人性化的网页内容检索库。官网 micawber：一个小型网页内容提取库，用来从 urls 提取富内容。官网 newspaper：使用 python 进行新闻提取，文章提取以及内容策展。官网 opengraph：一个用来解析开放内容协议 open graph protocol 的 python 模块。官网 python goose：html 内容 文章提取器。官网 python readability：arc90 公司 readability 工具的 python 高速端口。官网 sanitize：为杂乱的数据世界带来调理性。官网 sumy：一个为文本文件和 html 页面进行自动摘要的模块。官网 textract：从任何格式的文档中提取文本，word，powerpoint，pdfs 等等。官网 表单 进行表单操作的库。 deform：python html 表单生成库，受到了 formish 表单生成库的启发。官网 django bootstrap3：集成了 bootstrap 3 的 django。官网 django crispy forms：一个 django 应用，他可以让你以一种非常优雅且 dry（dont repeat yourself） 的方式来创建美观的表单。官网 django remote forms：一个平台独立的 django 表单序列化工具。官网 wtforms：一个灵活的表单验证和呈现库。官网 wtforms json：一个 wtforms 扩展，用来处理 json 数据。官网 数据验证 数据验证库。多用于表单验证。 cerberus：一个映射验证器（mappings validator）。支持多种规则，提供归一化功能，可以方便地定制为 python 风格的 schema 定义。官网 colander：一个用于对从 xml json，html 表单获取的数据或其他同样简单的序列化数据进行验证和反序列化的系统。官网 kmatch：一种用于匹配 验证 筛选 python 字典的语言。官网 schema：一个用于对 python 数据结构进行验证的库。官网 schematics：数据结构验证。官网 valideer：轻量级可扩展的数据验证和适配库。官网 voluptuous：一个 python 数据验证库。主要是为了验证传入 python 的 json，yaml 等数据。官网 jsonschema：json schema的 python 实现，用于 json 数据的验证。官网 反垃圾技术 帮助你和电子垃圾进行战斗的库。 django simple captcha：一个简单、高度可定制的 django 应用，可以为任何 django 表单添加验证码。官网 django simple spam blocker：一个用于 django 的简单的电子垃圾屏蔽工具。官网 标记 用来进行标记的库。 django taggit：简单的 django 标记工具。官网 管理面板 管理界面库。 ajenti：一个你的服务器值得拥有的管理面板。官网 django suit：django 管理界面的一个替代品 仅对于非商业用途是免费的 。官网 django xadmin：django admin 的一个替代品，具有很多不错的功能。官网 flask admin：一个用于 flask 的简单可扩展的管理界面框架。官网 flower：一个对 celery 集群进行实时监控和提供 web 管理界面的工具。官网 grappelli：django 管理界面的一个漂亮的皮肤。官网 wooey：一个 django 应用，可以为 python 脚本创建 web 用户界面。官网 静态站点生成器 静态站点生成器是一个软件，它把文本和模板作为输入，然后输出 html 文件。 pelican：使用 markdown 或 rest 来处理内容， jinja 2 来制作主题。支持 dvcs disqus 。agpl 许可。官网 cactus：为设计师设计的静态站点生成器。官网 hyde：基于 jinja2 的静态站点生成器。官网 nikola：一个静态网站和博客生成器。官网 tinkerer：tinkerer 是一个博客引擎 静态站点生成器，由 sphinx 驱动。官网 lektor：一个简单易用的静态 cms 和博客引擎。官网 进程 操作系统进程启动及通信库。 envoy：比 python subprocess 模块更人性化。官网 sarge：另一 种 subprocess 模块的封装。官网 sh：一个完备的 subprocess 替代库。官网 并发和并行 用以进行并发和并行操作的库。 multiprocessing： python 标准库 基于进程的“线程”接口。官网 threading： python 标准库 更高层的线程接口。官网 eventlet：支持 wsgi 的异步框架。官网 gevent：一个基于协程的 python 网络库，使用 greenlet。官网 tomorrow：用于产生异步代码的神奇的装饰器语法实现。官网 uvloop：在 libuv 之上超快速实现 asyncio 事件循环。官网 网络 用于网络编程的库。 asyncio： python 标准库 异步 i o 事件循环 协程以及任务。官网 twisted：一个事件驱动的网络引擎。官网 pulsar：事件驱动的并发框架。官网 diesel：基于 greenlet 的事件 i o 框架。官网 pyzmq：一个 zeromq 消息库的 python 封装。官网 toapi：一个轻巧，简单，快速的 flask 库，致力于为所有网站提供 api 服务。官网 txzmq：基于 twisted 的 zeromq 消息库的 python 封装。官网 websocket 帮助使用 websocket 的库。 autobahnpython：给 python 、使用的 websocket wamp 基于 twisted 和 asyncio。官网 crossbar：开源统一应用路由 websocket wamp for python on autobahn 。官网 django socketio：给 django 用的 websockets。官网 websocket for python：为 python2 3 以及 pypy 编写的 websocket 客户端和服务器库。官网 wsgi 服务器 兼容 wsgi 的 web 服务器 gunicorn：pre forked 部分是由 c 语言编写的。官网 uwsgi：uwsgi 项目的目的是开发一组全栈工具，用来建立托管服务， 由 c 语言编写。官网 bjoern：异步，非常快速，由 c 语言编写。官网 fapws3：异步 仅对于网络端 ，由 c 语言编写。官网 meinheld：异步，部分是由 c 语言编写的。官网 netius：异步，非常快速。官网 paste：多线程，稳定，久经考验。官网 rocket：多线程。官网 waitress：多线程 是它驱动着 pyramid 框架。官网 werkzeug：一个 wsgi 工具库，驱动着 flask ，而且可以很方便大嵌入到你的项目中去。官网 rpc 服务器 兼容 rpc 的服务器。 simplejsonrpcserver：这个库是 json rpc 规范的一个实现。官网 simplexmlrpcserver： python 标准库 简单的 xml rpc 服务器实现，单线程。官网 zerorpc：zerorpc 是一个灵活的 rpc 实现，基于 zeromq 和 messagepack。官网 密码学 cryptography：这个软件包意在提供密码学基本内容和方法提供给 python 开发者。官网 hashids：在 python 中实现 hashids 。官网 paramiko：sshv2 协议的 python 2 6 3 3 ，提供客户端和服务端的功能。官网 passlib：安全密码存储／哈希库，官网 pycrypto：python 密码学工具箱。官网 pynacl：网络和密码学 nacl 库的 python 绑定。官网 图形用户界面 用来创建图形用户界面程序的库。 curses：内建的 ncurses 封装，用来创建终端图形用户界面。官网 enaml：使用类似 qml 的 declaratic 语法来创建美观的用户界面。官网 kivy：一个用来创建自然用户交互（nui）应用程序的库，可以运行在 windows linux mac os x android 以及 ios 平台上。官网 pyglet：一个 python 的跨平台窗口及多媒体库。官网 pyqt：跨平台用户界面框架 qt 的 python 绑定 ，支持 qt v4 和 qt v5。官网 pyside：跨平台用户界面框架 qt 的 python 绑定 ，支持 qt v4。官网 tkinter：tkinter 是 python gui 的一个事实标准库。官网 toga：一个 python 原生的 操作系统原生的 gui 工具包。官网 urwid：一个用来创建终端 gui 应用的库，支持组件，事件和丰富的色彩等。官网 wxpython：wxpython 是 wxwidgets c 类库和 python 语言混合的产物。官网 pygobject：glib gobject gio gtk gtk 3 的 python 绑定。官网 flexx：flexx 是一个纯 python 语言编写的用来创建 gui 程序的工具集，它使用 web 技术进行界面的展示。官网 游戏开发 超赞的游戏开发库。 cocos2d：cocos2d 是一个用来开发 2d 游戏， 示例和其他图形 交互应用的框架。基于 pyglet。官网 panda3d：由迪士尼开发的 3d 游戏引擎，并由卡内基梅陇娱乐技术中心负责维护。使用 c 编写 针对 python 进行了完全的封装。官网 pygame：pygame 是一组 python 模块，用来编写游戏。官网 pyogre：ogre 3d 渲染引擎的 python 绑定，可以用来开发游戏和仿真程序等任何 3d 应用。官网 pyopengl：opengl 的 python 绑定及其相关 apis。官网 pysdl2：sdl2 库的封装，基于 ctypes。官网 renpy：一个视觉小说（visual novel）引擎。官网 日志 用来生成和操作日志的库。 logging： python 标准库 为 python 提供日志功能。官网 logbook：logging 库的替代品。官网 eliot：为复杂的和分布式系统创建日志。官网 raven：sentry 的 python 客户端。官网 sentry：实时记录和收集日志的服务器。官网 测试 进行代码库测试和生成测试数据的库。 测试框架 unittest： python 标准库 单元测试框架。官网 nose：nose 扩展了 unittest 的功能。官网 contexts：一个 python 3 3 的 bdd 框架。受到 c – machine specifications 的启发。官网 hypothesis：hypothesis 是一个基于先进的 quickcheck 风格特性的测试库。官网 mamba：python 的终极测试工具， 拥护 bdd。官网 pyautogui：pyautogui 是一个人性化的跨平台 gui 自动测试模块。官网 pyshould：should 风格的断言，基于 pyhamcrest。官网 pytest：一个成熟的全功能 python 测试工具。官网 green：干净，多彩的测试工具。官网 pyvows：bdd 风格的测试工具，受 vows js 的启发。官网 robot framework：一个通用的自动化测试框架。官网 web 测试 selenium：selenium webdriver 的 python 绑定。官网 locust：使用 python 编写的，可扩展的用户加载测试工具。官网 sixpack：一个和语言无关的 a b 测试框架。官网 splinter：开源的 web 应用测试工具。官网 mock 测试 mock： python 标准库 一个用于伪造测试的库。官网 doublex：python 的一个功能强大的 doubles 测试框架。官网 freezegun：通过伪造日期模块来生成不同的时间。官网 httmock：针对 python 2 6 和 3 2 生成 伪造请求的库。官网 httpretty：python 的 http 请求 mock 工具。官网 responses：伪造 python 中的 requests 库的一个通用库。官网 vcr py：在你的测试中记录和重放 http 交互。官网 对象工厂 factoryboy：一个 python 用的测试固件 test fixtures 替代库。官网 mixer：另外一个测试固件 test fixtures 替代库，支持 django flask sqlalchemy peewee 等。官网 modelmommy：为 django 测试创建随机固件。官网 代码覆盖率 coverage：代码覆盖率测量。官网 codecov：一个代码覆盖率测试工具，为开源项目提供免费代码覆盖率测试服务。官网 伪数据 faker：一个 python 库，用来生成伪数据。官网 fake2db：伪数据库生成器。官网 radar：生成随机的日期 时间。官网 错误处理 fuckit py：fuckit py 使用最先进的技术来保证你的 python 代码无论对错都能继续运行。官网 代码分析和 lint 工具 进行代码分析，解析和操作代码库的库和工具。 代码分析 coala：语言独立和易于扩展的代码分析应用程序。官网 code2flow：把你的 python 和 javascript 代码转换为流程图。官网 pycallgraph：这个库可以把你的 python 应用的流程 调用图 进行可视化。官网 pysonar2：python 类型推断和检索工具。官网 lint 工具 flake8：模块化源码检查工具 pep8 pyflakes 以及 co。官网 pylint：一个完全可定制的源码分析器。官网 yapf google 的 python 代码格式化工具。官网 pylama：python 和 javascript 的代码审查工具。官网 代码格式化 autopep8：自动格式化 python 代码，以使其符合 pep8 规范。官网 black：一个坚定的 python 代码格式化工具。官网 调试工具 用来进行代码调试的库。 调试器 ipdb：ipython 启用的 pdb。官网 pudb：全屏，基于控制台的 python 调试器。官网 pyringe：可以在 python 进程中附加和注入代码的调试器。官网 wdb：一个奇异的 web 调试器，通过 websockets 工作。官网 winpdb：一个具有图形用户界面的 python 调试器，可以进行远程调试，基于 rpdb2。官网 django debug toolbar：为 django 显示各种调试信息。官网 django devserver：一个 django 运行服务器的替代品。官网 flask debugtoolbar：django debug toolbar 的 flask 版。官网 性能分析器 lineprofiler：逐行性能分析。官网 memory profiler：监控 python 代码的内存使用。官网、内存 profiling：一个交互式 python 性能分析工具。官网 其他 pyelftools：解析和分析 elf 文件以及 dwarf 调试信息。官网 python statsd：statsd 服务器的 python 客户端。官网 科学计算和数据分析 用来进行科学计算和数据分析的库。 astropy：一个天文学 python 库。官网 bcbio nextgen：这个工具箱为全自动高通量测序分析提供符合最佳实践的处理流程。官网 bccb：生物分析相关代码集合。官网 biopython：biopython 是一组可以免费使用的用来进行生物计算的工具。官网 blaze：numpy 和 pandas 的大数据接口。官网 cclib：一个用来解析和解释计算化学软件包输出结果的库。官网 networkx：一个为复杂网络设计的高性能软件。官网 neupy：执行和测试各种不同的人工神经网络算法。官网 numba：python jit just in time 编译器，针对科学用的 python ，由 cython 和 numpy 的开发者开发。官网 numpy：使用 python 进行科学计算的基础包。官网 open babel：一个化学工具箱，用来描述多种化学数据。官网 open mining：使用 python 挖掘商业情报 bi pandas web 接口 。官网 orange：通过可视化编程或 python 脚本进行数据挖掘，数据可视化，分析和机器学习。官网 pandas：提供高性能，易用的数据结构和数据分析工具。官网 pydy：pydy 是 python dynamics 的缩写，用来为动力学运动建模工作流程提供帮助， 基于 numpy scipy ipython 和 matplotlib。官网 pymc：马尔科夫链蒙特卡洛采样工具。官网 rdkit：化学信息学和机器学习软件。官网 scipy：由一些基于 python ，用于数学，科学和工程的开源软件构成的生态系统。官网 statsmodels：统计建模和计量经济学。官网 sympy：一个用于符号数学的 python 库。官网 zipline：一个 python 算法交易库。官网 bayesian belief networks：优雅的贝叶斯信念网络框架。官网 数据可视化 进行数据可视化的库。 参见 awesome javascript。 matplotlib：一个 python 2d 绘图库。官网 bokeh：用 python 进行交互式 web 绘图。官网 ggplot：ggplot2 给 r 提供的 api 的 python 版本。官网 plotly：协同 python 和 matplotlib 工作的 web 绘图库。官网 pyecharts：基于百度 echarts 的数据可视化库。官网 pygal：一个 python svg 图表创建工具。官网 pygraphviz：graphviz 的 python 接口。官网 pyqtgraph：交互式实时 2d 3d 图像绘制及科学 工程学组件。官网 snakeviz：一个基于浏览器的 pythons cprofile 模块输出结果查看工具。官网 vincent：把 python 转换为 vega 语法的转换工具。官网 vispy：基于 opengl 的高性能科学可视化工具。官网 计算机视觉 计算机视觉库。 opencv：开源计算机视觉库。官网 pyocr：tesseract 和 cuneiform 的包装库。官网 pytesseract：google tesseract ocr 的另一包装库。官网 simplecv：一个用来创建计算机视觉应用的开源框架。官网 机器学习 机器学习库。 参见 awesome machine learning caffe 一个 caffe 的 python 接口。官网 caffe2：一个轻量级的，模块化的，可扩展的深度学习框架。官网 crab：灵活、快速的推荐引擎。官网 gensim：人性化的话题建模库。官网 hebel：gpu 加速的深度学习库。官网 keras 以 tensorflow theano cntk 为后端的深度学习封装库，快速上手神经网络。官网 mxnet：一个高效和灵活的深度学习框架。官网 nupic：智能计算 numenta 平台。官网 pattern：python 网络挖掘模块。官网 pybrain：另一个 python 机器学习库。官网 pydeep：python 深度学习库。官网 pylearn2：一个基于 theano 的机器学习库。官网 python recsys：一个用来实现推荐系统的 python 库。官网 pytorch：一个具有张量和动态神经网络，并有强大 gpu 加速能力的深度学习框架。官网 scikit learn：基于 scipy 构建的机器学习 python 模块。官网 skflow：一个 tensorflow 的简化接口 模仿 scikit learn 。官网 tensorflow：谷歌开源的最受欢迎的深度学习框架。官网 theano：一个快速数值计算库。官网 vowpalporpoise：轻量级 vowpal wabbit 的 python 封装。官网 mapreduce mapreduce 框架和库。 dpark：spark 的 python 克隆版，一个类似 mapreduce 的框架。官网 dumbo：这个 python 模块可以让人轻松的编写和运行 hadoop 程序。官网 luigi：这个模块帮你构建批处理作业的复杂流水线。官网 mrjob：在 hadoop 或 amazon web services 上运行 mapreduce 任务。官网 pyspark：spark 的 python api 。官网 streamparse：运行针对事实数据流的 python 代码。集成了 apache storm。官网 函数式编程 使用 python 进行函数式编程。 cytoolz：toolz 的 cython 实现 高性能函数式工具。官网 fn py：在 python 中进行函数式编程 实现了一些享受函数式编程缺失的功能。官网 funcy：炫酷又实用的函数式工具。官网 toolz：一组用于迭代器，函数和字典的函数式编程工具。官网 第三方 api 用来访问第三方 api 的库。 参见： list of python api wrappers and libraries。 apache libcloud：一个为各种云设计的 python 库。官网 boto：amazon web services 的 python 接口。官网 django wordpress：wordpress models and views for django 官网 facebook sdk：facebook 平台的 python sdk 官网 facepy：facepy 让和 facebooks graph api 的交互变得更容易。官网 gmail：gmail 的 python 接口。官网 google api python client：python 用的 google apis 客户端库。官网 gspread：google 电子表格的 python api 官网 twython：twitter api 的封装。官网 devops 工具 用于 devops 的软件和库。 ansible：一个非常简单的 it 自动化平台。官网 saltstack：基础设施自动化和管理系统。官网 openstack：用于构建私有和公有云的开源软件。官网 docker compose：快速，分离的开发环境，使用 docker。官网 fabric：一个简单的，python 风格的工具，用来进行远程执行和部署。官网 cuisine：为 fabric 提供一系列高级函数。官网 fabtools：一个用来编写超赞的 fabric 文件的工具。官网 gitapi：git 的纯 python api。官网 hgapi：mercurial 的纯 python api。官网 honcho：foreman 的 python 克隆版，用来管理基于 procfile 的应用。官网 pexpect：controlling interactive programs in a pseudo terminal like 在一个伪终端中控制交互程序，就像 gnu expect 一样。官网 psutil：一个跨平台进程和系统工具模块。官网 supervisor：unix 的进程控制系统。官网 任务调度 任务调度库。 apscheduler：轻巧但强大的进程内任务调度，使你可以调度函数。官网 django schedule：一个 django 排程应用。官网 doit：一个任务执行和构建工具。官网 gunnery：分布式系统使用的多用途任务执行工具 ，具有 web 交互界面。官网 joblib：一组为 python 提供轻量级作业流水线的工具。官网 plan：如有神助地编写 crontab 文件。官网 schedule：人性化的 python 任务调度库。官网 spiff：使用纯 python 实现的强大的工作流引擎。官网 taskflow：一个可以让你方便执行任务的 python 库，一致并且可靠。官网 airflow：airflow 是airbnb公司开源的，是一个工作流分配管理系统，通过有向非循环图的方式管理任务流程，设置任务依赖关系和时间调度。官方 外来函数接口 使用外来函数接口的库。 cffi：用来调用 c 代码的外来函数接口。官网 ctypes： python 标准库 用来调用 c 代码的外来函数接口。官网 pycuda：nvidia cuda api 的封装。官网 swig：简化的封装和接口生成器。官网 高性能 让 python 更快的库。 cython：优化的 python 静态编译器。使用类型混合使 python 编译成 c 或 c 模块来获得性能的极大提升。官网 peachpy：嵌入 python 的 x86 64 汇编器。可以被用作 python 内联的汇编器或者是独立的汇编器，用于 windows linux os x native client 或者 go 。官网 pypy：使用 python 实现的 python。解释器使用黑魔法加快 python 运行速度且不需要加入额外的类型信息。官网 pyston：使用 llvm 和现代 jit 技术构建的 python 实现，目标是为了获得很好的性能。官网 stackless python：一个强化版的 python。官网 微软的 windows 平台 在 windows 平台上进行 python 编程。 python x y ：面向科学应用的 python 发行版，基于 qt 和 spyder。官网 pythonlibs：非官方的 windows 平台 python 扩展二进制包。官网 pythonnet：python 与 net 公共语言运行库 clr 的集成。官网 pywin32：针对 windows 的 python 扩展。官网 winpython：windows 7 8 系统下便携式开发环境。官网 网络可视化和 sdn 用来进行网络可视化和 sdn 软件定义网络 的工具和库。 mininet：一款流行的网络模拟器以及用 python 编写的 api。官网 pox：一个针对基于 python 的软件定义网络应用（例如 openflow sdn 控制器）的开源开发平台。官网 pyretic：火热的 sdn 编程语言中的一员，为网络交换机和模拟器提供强大的抽象能力。官网 sdx platform：基于 sdn 的 ixp 实现，影响了 mininet pox 和 pyretic。官网 nru：一个基于组件的软件定义网络框架。官网 硬件 用来对硬件进行编程的库。 ino：操作 arduino 的命令行工具。官网 pyro：python 机器人编程库。官网 pyuserinput：跨平台的，控制鼠标和键盘的模块。官网 scapy：一个非常棒的操作数据包的库。官网 wifi：一个 python 库和命令行工具用来在 linux 平台上操作 wifi。官网 pingo：pingo 为类似 raspberry pi，pcduino， intel galileo 等设备提供统一的 api 用以编程。官网 兼容性 帮助从 python 2 向 python 3 迁移的库。 python future：这就是 python 2 和 python 3 之间丢失的那个兼容性层。官网 python modernize：使 python 代码更加现代化以便最终迁移到 python 3。官网 six：python 2 和 3 的兼容性工具。官网 杂项 不属于上面任何一个类别，但是非常有用的库。 blinker：一个快速的 python 进程内信号 事件分发系统。官网 itsdangerous：一系列辅助工具用来将可信的数据传入不可信的环境。官网 pluginbase：一个简单但是非常灵活的 python 插件系统。官网 pychievements：一个用来创建和追踪成就的 python 框架。官网 tryton：一个通用商务框架。官网 算法和设计模式 python 实现的算法和设计模式。 algorithms：一个 python 算法模块。官网 python patterns：python 设计模式的集合。官网 sortedcontainers：快速，纯 python 实现的 sortedlist，sorteddict 和 sortedset 类型。官网 编辑器插件 编辑器和 ide 的插件 emacs elpy：emacs python 开发环境。官网 sublime text sublimejedi：一个 sublime text 插件，用来使用超赞的自动补全库 jedi。官网 anaconda：anaconda 把你的 sublime text 3 变成一个功能齐全的 python ide。官网 vim youcompleteme：引入基于 jedi 的 python 自动补全引擎。官网 jedi vim：绑定 vim 和 jedi 自动补全库对 python 进行自动补全。官网 python mode：将 vim 变成 python ide 的一款多合一插件。官网 visual studio ptvs：visual studio 的 python 工具。官网 集成开发环境 流行的 python 集成开发环境。 pycharm：商业化的 python ide ，由 jetbrains 开发。也有免费的社区版提供。官网 liclipse：基于 eclipse 的免费多语言 ide 。使用 pydev 来支持 python 。官网 spyder：开源 python ide。官网 自动聊天工具 用于开发聊天机器人的库 errbot：最简单和最流行的聊天机器人用来实现自动聊天工具。官网 服务 在线工具和简化开发的 api 。 金融数据 tushare ：一个可以提供免费股票、基金、期货、港股等金融数据的 python 开源数据。官网 ta lib ：金融数据技术分析库，可以依据原始金融数据计算各种技术指标 计算性能比较优异。官网 持续集成 参见 awesome ciandcd travis ci：一个流行的工具，为你的开源和 私人 项目提供持续集成服务。 仅支持 github 官网 circleci：一个持续集成工具，可以非常快速的进行并行测试。 仅支持 github 官网 vexor ci：一个为私人 app 提供持续集成的工具，支持按分钟付费。官网 wercker：基于 docker 平台，用来构建和部署微服务。官网 代码质量 codacy：自动化代码审查，更加快速的发布高质量代码。对于开源项目是免费的。官网 quantifiedcode：一个数据驱动、自动、持续的代码审查工具。官网 资源 在这里可以找到新的 python 库。 网站 r python coolgithubprojects django packages full stack python python 3 wall of superpowers python hackers python zeef trending python repositories on github today pypi ranking 周刊 import python newsletter pycoders weekly python weekly twitter codetengu getpy planetpython pycoders pypi pythontrending pythonweekly 学习指南 scipy lecture notes：如何用 python 来做学术？官网 sscientific python lectures：python 科学计算的资料。官网 mario level 1：用 python 和 pygame 写的超级马里奥第一关。官网 python koans：python 的交互式学习工具。官网 minecraft：用 python 写的 minecraft 游戏。官网 pycrumbs：python 资源大全。官网 python patterns：使用 python 实现设计模式。官网 projects：python 项目大集合。官网 the hitchhikers guide to python：旅行者的 python 学习指南。官网 code like a pythonista idiomatic python：如何像 python 高手 pythonista 一样编程。官网 知名网站 值得关注的 python 技术站点。 中文站点 伯乐在线 python 频道：分享 python 开发技术、相关的行业动态。官网 英文站点 《值得关注的 10 个 python 英文博客》 微博、微信公众号 python开发者 微博： python开发者 python开发者：人生苦短，我用 python。python 越来越受广大程序员的喜爱。「python开发者」是最受欢迎的、专注分享 python 技术的微信公众号，主要分享 python 相关的技术文章、工具资源和资讯等。