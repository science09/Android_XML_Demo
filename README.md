# Android_XML_Demo
Android解析XML格式数据的三种方法

XML在各种开发中都广泛应用，Android也不例外。作为承载数据的一个重要角色，如何读写XML成为Android开发中一项重要的技能。今天就由我向大家介绍一下在Android平台下几种常见的XML解析和创建的方法。

在Android中，常见的XML解析器分别为SAX解析器、DOM解析器和PULL解析器。

### SAX解析器：

SAX(Simple API for XML)解析器是一种基于事件的解析器，它的核心是事件处理模式，主要是围绕着事件源以及事件处理器来工作的。当事件源产生事件后，调用事件处理器相应的处理方法，一个事件就可以得到处理。在事件源调用事件处理器中特定方法的时候，还要传递给事件处理器相应事件的状态信息，这样事件处理器才能够根据提供的事件信息来决定自己的行为。

SAX解析器的优点是解析速度快，占用内存少。非常适合在Android移动设备中使用。

### DOM解析器：

DOM是基于树形结构的的节点或信息片段的集合，允许开发人员使用DOM API遍历XML树、检索所需数据。分析该结构通常需要加载整个文档和构造树形结构，然后才可以检索和更新节点信息。

由于DOM在内存中以树形结构存放，因此检索和更新效率会更高。但是对于特别大的文档，解析和加载整个文档将会很耗资源。

### PULL解析器：

PULL解析器的运行方式和SAX类似，都是基于事件的模式。不同的是，在PULL解析过程中，我们需要自己获取产生的事件然后做相应的操作，而不像SAX那样由处理器触发一种事件的方法，执行我们的代码。PULL解析器小巧轻便，解析速度快，简单易用，非常适合在Android移动设备中使用，Android系统内部在解析各种XML时也是用PULL解析器。

XMLDemo文件下介绍了三种解析器的使用，通过示例可以发现，PULL解析方式更简单易用。
