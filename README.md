# go-normal
go标准库学习

[TOC]

# 标准库简介

## 输入输出
- bufio             bufio包实现了带缓存的I/O操作.
- io                io包提供了基本输入输出功能，大多数是围绕系统功能的封装。
    - ioutil            ioutil实现了一些I/O的工具函数。
- flag	            flag 包实现命令行标签解析.
- fmt	            fmt 包实现了格式化I/O函数，类似于C的 printf 和 scanf.
## 文本
- bytes             bytes 包实现了操作[]byte的常用函数.
- reflect	        reflect包实现了运行时反射，允许程序操作任意类型的对象.
- errors	        error 包实现了用于错误处理的函数.
- context           context 包上下文定义了上下文类型，它在 API 边界和进程之间携带截止日期、取消信号和其他请求范围的值。
- time	    	    time包提供了时间的显示和测量用的函数.
- unsafe	        unsafe 包含有关于Go程序类型安全的所有操作.
- expvar	        expvar包提供了公共变量的标准接口，如服务的操作计数器.
- html	            html包提供了用于转义和解转义HTML文本的函数.
    - template	        template包（html/template）实现了数据驱动的模板，用于生成可对抗代码注入的安全HTML输出.
- sort	    	    sort 包为切片及用户定义的集合的排序操作提供了原语.
- strconv	        strconv包实现了基本数据类型和其字符串表示的相互转换.
- strings	        strings包实现了用于操作字符的简单函数.
- sync	    	    sync 包提供了互斥锁这类的基本的同步原语.
    - atomic	        atomic 包提供了底层的原子性内存原语，这对于同步算法的实现很有用.
## 数据结构与算法
- container
    - heap          heap包提供了对任意类型（实现了heap.Interface接口）的堆操作.
    - list          list包实现了双向链表.
    - ring          ring实现了环形链表的操作.
- index	    	
    - suffixarray	    suffixarrayb包通过使用内存中的后缀树实现了对数级时间消耗的子字符串搜索.
- regexp	    	regexp包实现了正则表达式搜索.
    - syntax	        syntax包将正则表达式解析为解析树并将解析树编译为程序。
## 数学计算
- hash	    	    hash包提供hash函数的接口. (下面有很多的包)
- math	    	    math 包提供了基本常数和数学函数。
    - big	        	big 包实现了（大数的）高精度运算.
    - cmplx	        	cmplx 包为复数提供了基本的常量和数学函数.
    - rand	        	rand 包实现了伪随机数生成器.
## 文件系统
## 数据持久存储与交换
- crypto            crypto包搜集了常用的密码（算法）常量. (下面有很多的包)
- database	    	
    - sql	            sql 包提供了通用的SQL（或类SQL）数据库接口.
    - driver            driver 包定义了应被数据库驱动实现的接口，这些接口会被sql包使用.
encoding	        encoding包定义了供其它包使用的可以将数据在字节水平和文本表示之间转换的接口.
    - ascii85	        ascii85 包是对 ascii85 的数据编码的实现.
    - asn1	        	asn1包实现了DER编码的ASN.1数据结构的解析，参见ITU-T Rec X.690.
    - base32	        base32包实现了RFC 4648规定的base32编码.
    - base64	        base64实现了RFC 4648规定的base64编码.
    - binary	        binary包实现了简单的数字与字节序列的转换以及变长值的编解码.
    - csv	        	csv读写逗号分隔值（csv）的文件.
    - gob	        	gob包管理gob流——在编码器（发送器）和解码器（接受器）之间交换的binary值.
    - hex	        	hex包实现了16进制字符表示的编解码.
    - json	        	json包实现了json对象的编解码，参见RFC 4627.
    - pem	        	pem包实现了PEM数据编码（源自保密增强邮件协议）.
    - xml	        	xml包 xml 实现了一个简单的 XML 1.0 解析器，它可以理解 XML 名称空间。
## 数据压缩与归档
- compress
    - bzip2	            bzip2包实现bzip2的解压缩.
    - flate	            flate包实现了deflate压缩数据格式，参见RFC 1951.
    - gzip	            gzip包实现了gzip格式压缩文件的读写，参见RFC 1952.
    - lzw	            lzw包实现了Lempel-Ziv-Welch数据压缩格式，
    - zlib	            zlib包实现了对zlib格式压缩数据的读写，参见RFC 1950.
## 测试
- syscall           syscall 包含一个到低级操作系统原语的接口。
- test              test 包测试为 Go 包的自动化测试提供支持。
    - iotest            iotest 包实现了主要用于测试的 Readers 和 Writers。
    - quick             quick 包实现了实用函数来帮助进行黑盒测试。
## 进程、线程与gorotine
## 网络通讯
- net	    	    net包提供了可移植的网络I/O接口，包括TCP/IP、UDP、域名解析和Unix域socket.
    - http	    	    http包提供了HTTP客户端和服务端的实现.
        - cgi	    	    cgi 包实现了RFC3875协议描述的CGI（公共网关接口）.
        - cookiejar		    cookiejar包实现了保管在内存中的符合RFC 6265标准的http.CookieJar接口.
        - fcgi	    	    fcgi 包实现了FastCGI协议.
        - httptest	        httptest 包提供HTTP测试的单元工具.
        - httptrace	        Package httptrace provides mechanisms to trace the events within HTTP client requests.
        - httputil	        httputil包提供了HTTP公用函数，是对net/http包的更常见函数的补充.
        - pprof	    	    pprof 包通过提供HTTP服务返回runtime的统计数据，这个数据是以pprof可视化工具规定的返回格式返回的.
    - mail	    	    mail 包实现了解析邮件消息的功能.
    - rpc	    	    rpc 包提供了一个方法来通过网络或者其他的I/O连接进入对象的外部方法.
        - jsonrpc	        jsonrpc 包使用了rpc的包实现了一个JSON-RPC的客户端解码器和服务端的解码器.
    - smtp	    	    smtp包实现了简单邮件传输协议（SMTP），参见RFC 5321.
    - textproto	        	textproto实现了对基于文本的请求/回复协议的一般性支持，包括HTTP、NNTP和SMTP.
    - url	    	    url包解析URL并实现了查询的逸码，参见RFC 3986.
## 应用构建与debug
- builtin           builtin 包为Go的预声明标识符提供了文档.
- debug
    - dwarf             dwarf 包提供对从可执行文件加载的 DWARF 调试信息的访问，如 http://dwarfstd.org/doc/dwarf-2.0.0.pdf 上的 DWARF 2.0 标准中所定义
    - elf               elf 包实现对 ELF 对象文件的访问。
    - gosym             gosym 包实现了对嵌入在由 gc 编译器生成的 Go 二进制文件中的 Go 符号和行号表的访问。
    - macho             macho 包实现对 Mach-O 对象文件的访问。
    - pe                pe 包实现对 PE（Microsoft Windows Portable Executable）文件的访问。
    - plan9obj          plan9obj 包实现对 Plan 9 a.out 对象文件的访问。
- os	            os包提供了操作系统函数的不依赖平台的接口.
    - exec	    	    exec包执行外部命令.
    - signal	        signal包实现了对输入信号的访问.
    - user	    	    user包允许通过名称或ID查询用户帐户.
- path	    	    path实现了对斜杠分隔的路径的实用操作函数.
    - filepath	    	filepath包实现了兼容各操作系统的文件路径的实用操作函数.
- plugin	        Package插件实现了Go插件的加载和符号解析。
- runtime	    	TODO(osc): 需更新 runtime 包含与Go的运行时系统进行交互的操作，例如用于控制Go程的函数.
    - cgo	    	    cgo 包含有 cgo 工具生成的代码的运行时支持.
    - debug	    	    debug 包含有程序在运行时调试其自身的功能.
    - pprof	    	    pprof 包按照可视化工具 pprof 所要求的格式写出运行时分析数据.
    - race	    	    race 包实现了数据竞争检测逻辑.
    - trace	    	    Go execution tracer.

# 参考
 - [go标准库中文文档](https://studygolang.com/pkgdoc)
 - [go语言标准库](https://books.studygolang.com/The-Golang-Standard-Library-by-Example/)
 - [概述](https://studygolang.com/static/pkgdoc/main.html)
