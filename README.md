# Cesium.HPUZYZ.Demo
This project is some demos of CESIUM. Much of them are from other people's blogs and cesium's official website (https://cesiumjs.org/tutorials/cesium-up-and-running/). Thanks to my good friend MikesWei (https://github.com/MikesWei) for giving me great help.
# 内容
本工程使用VS2013+chrome来编辑和调试，示例代码下载后，可以直接在vs中调试运行，部分示例的测试数据需要另外下载，在对应博客中我已经一一指出了。目前我把cesium学习基础内容整理19个笔记，涵盖环境搭建、影像服务、地形服务、模型加载、鼠标事件、绘制对象、3DTiles加载等几方面。关于其它诸如czml、DataSource、粒子系统等先放一放，随后再学习。现在继续从两个方面写：工具篇、原理篇。工具篇包括在cesium引擎上实现一些常用的工具，原理篇和大家一起尝试查看cesium的源码，试图探究一下cesium底层实现和设计思想。
# 学习计划变更说明：
在看了cesium源码好多天后，发现自己连三维的门都没碰到，以前觉得会调用三维引擎的接口就算三维开发了，现在想想真是感觉自己井底之蛙。看cesium源码这么些天实在看不下去，索性从webgl底层学习。我想花一部分时间先把webgl这块补起来，不求马上就掌握（掌握也不可能，三维博大精深，仅凭看几页教程就说掌握真是天方夜谭），只求再看cesium源码时能看得懂就算达到目的了。先在原理篇前面插个专题：WebGL篇。
</br>
</br>
*[Cesium学习笔记汇总](http://blog.sina.com.cn/s/blog_15e866bbe0102xu2f.html) </br>
### 基础篇
*[Cesium学习笔记1--环境搭建](http://blog.sina.com.cn/s/blog_15e866bbe0102xleh.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483679&idx=1&sn=80cb03643d3a211e382c10f738148272&chksm=fc237c4ccb54f55ab244a7d38489a0568ce1f33c3831b7dad680e4b02296e71f2f9beeb89a28&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记2--官方DEMO和API查看](http://blog.sina.com.cn/s/blog_15e866bbe0102xm9s.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483679&idx=2&sn=35ea99dec0680e04e3801b90c09edc88&chksm=fc237c4ccb54f55a21276f900e3067b650ca0714c5b0365ce604df0ab97c90c5045a3502fbd1&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记3--Cesium影像服务--在线服务](http://blog.sina.com.cn/s/blog_15e866bbe0102xmo5.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483702&idx=1&sn=dbd93a6b696a1cb4b413195106125a37&chksm=fc237c65cb54f5730e1fae37c239cf74dac312ef306702ae12a7d17e90c6059ad07cbd2307bf&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记4--Cesium影像服务--在线服务扩展](http://blog.sina.com.cn/s/blog_15e866bbe0102xmo6.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483702&idx=2&sn=c459d3af574ae08ff721277882c62b61&chksm=fc237c65cb54f573bddfb09536480296be15dd183e023843a723f22c8b3ec177dd390eecaa84&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记5--Cesium影像服务--地图发布](http://blog.sina.com.cn/s/blog_15e866bbe0102xn72.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483702&idx=3&sn=211f3b73a5bc7f6915545be19282db91&chksm=fc237c65cb54f57354726e9906d60df8168f5094dd544fcc1895583d69c8c4252aa11453f603&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记6--Cesium影像服务--图层功能](http://blog.sina.com.cn/s/blog_15e866bbe0102xnmj.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483735&idx=1&sn=ef5006ea77056ea3c4e50add8c0735a9&chksm=fc237c04cb54f5122a70a957fba72cc57482de80ec06f87bb7eaef85caf358c64e5c9a6892a9&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记7--Cesium影像服务--BaseLayerPicker使用](http://blog.sina.com.cn/s/blog_15e866bbe0102xnml.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483735&idx=2&sn=de523b54dd825188851acf5a918f246c&chksm=fc237c04cb54f512400ef05dc5a0597e8042d925a5497beb575d5336357254b5ef24ff6f94ce&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记8--Cesium地形服务--在线地形](http://blog.sina.com.cn/s/blog_15e866bbe0102xoak.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483736&idx=1&sn=2795d14ea00f4d5539c7ec8e94721472&chksm=fc237c0bcb54f51da99041d6488a7c4a6c461f356da995e5d5c5d95e1daffa5ee1c9100be35d&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记9--Cesium地形服务--本地地形数据处理及加载](http://blog.sina.com.cn/s/blog_15e866bbe0102xofa.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483736&idx=2&sn=cbfa390aff7fc14c9764879851bf532b&chksm=fc237c0bcb54f51dc8a00464bb5a537ee41d321d676236631e4e0f3f3ef9d52046575e48a156&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记10--Cesium地形服务--地形数据采样](http://blog.sina.com.cn/s/blog_15e866bbe0102xoo7.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483736&idx=3&sn=bc34f2db26be861e99bf91ef5e797ddd&chksm=fc237c0bcb54f51d5c136e0d9d21c0c834c0275dbf662d02b6c1d5d95e8987001cadb40409ed&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记11--模型加载](http://blog.sina.com.cn/s/blog_15e866bbe0102xpsm.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483798&idx=1&sn=31760ec2922981374e437e02023ffbd3&chksm=fc237cc5cb54f5d301783086f577df31d1ae8665ab36a61c5a1f58cfbbbce792404d33148894&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记12--鼠标事件](http://blog.sina.com.cn/s/blog_15e866bbe0102xq8d.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483798&idx=2&sn=b2f7eda111003971733b93c886c6255e&chksm=fc237cc5cb54f5d3115c4315757cb7a52817f197750d6c6fe1bfb53862975ab65470a2877994&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记13--绘制对象-Entity方式](http://blog.sina.com.cn/s/blog_15e866bbe0102xqsx.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483798&idx=3&sn=b67b900e74885eba31281a85028a33f4&chksm=fc237cc5cb54f5d3a9805aaebbb3de0776d4daa7dee02aadd843235dbee8d1044b535c9df764&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记14--绘制对象-Entity管理](http://blog.sina.com.cn/s/blog_15e866bbe0102xrt2.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483798&idx=4&sn=8eb9808f4a56ee390ee8f2d8686e4cbc&chksm=fc237cc5cb54f5d319c1ff12d5c28e1c2987d0b2e57b6cf16f651a54ede13414087654113a26&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记15--绘制对象-Primitive方式](http://blog.sina.com.cn/s/blog_15e866bbe0102xse8.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483798&idx=5&sn=f46f3d4ca7b348f257dce6f5d5a3eb01&chksm=fc237cc5cb54f5d34bf24c8cb92de9ff22ed117a347da10c682089c7240a232617439287639a&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记16--绘制对象-Primitive管理](http://blog.sina.com.cn/s/blog_15e866bbe0102xseb.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483798&idx=6&sn=0294715d7375365d998f2df9d566c23c&chksm=fc237cc5cb54f5d369221b8a70875bb151650793a9068d85842e9cccd0b43d67aa09fc094537&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记17--绘制对象-Primitive外观](http://blog.sina.com.cn/s/blog_15e866bbe0102xsi8.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483798&idx=7&sn=9ec195e1b636ee9fc7d512132c9bfc9a&chksm=fc237cc5cb54f5d3806133a175644179b21193170b3d7e76d170ba914c53dd2fb333a7f5613a&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记18--绘制对象-效率比较](http://blog.sina.com.cn/s/blog_15e866bbe0102xsj3.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483798&idx=8&sn=4d5c9a8b655018b19bd98bdedeb42f81&chksm=fc237cc5cb54f5d31502f05e607adab030beb055506bde228e257b2693994362e3056a097aae&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记19--3DTiles加载](http://blog.sina.com.cn/s/blog_15e866bbe0102xt9i.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483800&idx=1&sn=ea74ff0529e6a6e48fea5cb1c39f928c&chksm=fc237ccbcb54f5ddd9e7dce8b299cf7b89bc98537f4dc5287357b2b25750c83980d03dd35317&token=1964897234&lang=zh_CN#rd)
### 工具篇
*[Cesium学习笔记-工具篇01-Tooltip-entity方式](http://blog.sina.com.cn/s/blog_15e866bbe0102xv5f.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483808&idx=1&sn=bb11a5c13d6a857ebb3d6833886d312f&chksm=fc237cf3cb54f5e59ed6b5d63cf6e0c28176f93562b22be4f08ab560bec32adbe800b7dc8c16&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记-工具篇02-Tooltip-div方式](http://blog.sina.com.cn/s/blog_15e866bbe0102xv8k.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483815&idx=1&sn=8cbab6c2a66a09f1cf787743dcb3ea5d&chksm=fc237cf4cb54f5e28a6bda6e6fd15fde7268228313cfb21143765addffaf4c1ae24779d8eb92&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记-工具篇03-DrawHelper](http://blog.sina.com.cn/s/blog_15e866bbe0102xvwv.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483828&idx=1&sn=2ffa5ff35dae482f65bdf8ae62e860ea&chksm=fc237ce7cb54f5f1eb3f29486dd97dddd4cc7c1177200f8623fe63c09e060a8eab518bd5609e&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记-工具篇04-ChangeablePrimitive可编辑图形](http://blog.sina.com.cn/s/blog_15e866bbe0102xvwx.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483839&idx=1&sn=b1cee3c34aa6e12db71a1e2a6486a161&chksm=fc237ceccb54f5faa747f4ee09f440990dc95d4a91a6dbdd3fb4a39ab9e5ea4b7bad0094bf17&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记-工具篇05-DynamicDrawTool交互绘制](http://blog.sina.com.cn/s/blog_15e866bbe0102xvx1.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483853&idx=1&sn=544ac3f074689942b9919943381041d7&chksm=fc237c9ecb54f5882eae7d0832bc90e2821f6c98ac503a0295e4294cfefe1bae3b7021a990d2&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记-工具篇06-GroundPush挖地形](http://blog.sina.com.cn/s/blog_15e866bbe0102xwyb.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483862&idx=1&sn=51a7d5f9a96877d7071fb60f93f96213&chksm=fc237c85cb54f59320d0b58c1ac14a9fc35162a48a7797b03923edc2e717c7148ae563270bb8&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记-工具篇07-GroundClipping挖地形](http://blog.sina.com.cn/s/blog_15e866bbe0102xwyd.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483868&idx=1&sn=9e052783c10652049f39a24e9ab32986&chksm=fc237c8fcb54f59905c52f01089225100a9c6163c6d22ff67595fed2fb35fa62b28a11381621&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记-工具篇08-CesiumNavigation导航插件](http://blog.sina.com.cn/s/blog_15e866bbe0102xxcw.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483875&idx=1&sn=96e65792ad6c43a11405592433cddc57&chksm=fc237cb0cb54f5a62e58fe0caa01a7053a2af6b292dbe383779101df53b4f0104f8d53d430e4&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记-工具篇09-CesiumVectorTile矢量瓦片](http://blog.sina.com.cn/s/blog_15e866bbe0102xxd1.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483892&idx=1&sn=60e4cec786a75696bb87d9b0d7c8ea87&chksm=fc237ca7cb54f5b1d3562b3f1b233f32f07286e0ec519793e34b711a261abc5ef43f0463d51b&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记-工具篇10-TileLonlatsImageryProvider经纬度网格瓦片地图服务](http://blog.sina.com.cn/s/blog_15e866bbe0102xxme.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483892&idx=2&sn=aa524545315feef23b088f8abb6db5ee&chksm=fc237ca7cb54f5b15ca0448cf6c06470498fc2674e7cb70839d2140e9475bc3758cade5b8fcf&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记-工具篇11-Mouse-ButtonLanguage鼠标设置、按钮语言设置](http://blog.sina.com.cn/s/blog_15e866bbe0102xyn0.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483899&idx=1&sn=74d3233f7877ede33425451788d36e1a&chksm=fc237ca8cb54f5be1558fe311b771321b44383a447cfda3b7b67f8919095f1f9a1f5782f0c6d&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记-工具篇12-GlobeSet球场景相关设置](http://blog.sina.com.cn/s/blog_15e866bbe0102xyny.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483922&idx=1&sn=62369576424d4277858a1cb7b02dc73d&chksm=fc237f41cb54f65743a4628fc718c93fd2ccebf445acb5468c9a6b75fa1a3f61a3e203e4c4ab&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记-工具篇13-CesiumThreejs引入threejs](http://blog.sina.com.cn/s/blog_15e866bbe0102xz2g.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483933&idx=1&sn=9647d29734100af5a6b6af241f202773&chksm=fc237f4ecb54f6588f529f40e49714b9d8b4921ad2c03aeac115650cdd2561ee4eb18978d17f&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记-工具篇14-PickPosition获取鼠标点击位置方法总结](http://blog.sina.com.cn/s/blog_15e866bbe0102xz32.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483938&idx=1&sn=60d835cc73ebc3d2d3bc67dc9a1882c4&chksm=fc237f71cb54f6673c935934d22d4c5fb84368e829eb21a7825470d951815d8f9ec021098289&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记-工具篇15-Elevation等高线绘制](http://blog.sina.com.cn/s/blog_15e866bbe0102xz6u.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483957&idx=1&sn=225ab5826f96d3e82c0bcef4c289aade&chksm=fc237f66cb54f670fca86192fff9704e270a77634a4cb6e3e6fd2812c6ae7b007e7a5055c8de&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记-工具篇16-DynamicDraw-ClampGround交互绘制-贴地](http://blog.sina.com.cn/s/blog_15e866bbe0102xzbj.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483966&idx=1&sn=b90a73739d4bd354cdde3a0c34805c01&chksm=fc237f6dcb54f67bddc33e8fd008eac4e9c291c1706beb2b23c3dbf66bfe3927dac4c9007877&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记-工具篇17-PrimitivePoint自定义渲染-点](http://blog.sina.com.cn/s/blog_15e866bbe0102y0ji.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483981&idx=1&sn=3c9a8b70b15460d563d53948c94c5095&chksm=fc237f1ecb54f6087d9b6ad40d5d0ea9a860da7024ec8990cf9ad8b022cad9c14c7127a1d8e5&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记-工具篇18-PrimitivePolyline自定义渲染-线](http://blog.sina.com.cn/s/blog_15e866bbe0102y0jj.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247483990&idx=1&sn=e78abc5c08b4dab545b69ed140186209&chksm=fc237f05cb54f6139f586cda6ba2fb70dce0c3a9058922ecdefc666492fcb58d860d852a43ee&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记-工具篇19-PrimitiveTriangles自定义渲染-面](http://blog.sina.com.cn/s/blog_15e866bbe0102y0jl.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247484000&idx=1&sn=e2a99635a17874109191c78481bc0151&chksm=fc237f33cb54f62511e8ef60af05749ea98a50eb4dd140cd2dd30bd6a7da7a26548de87aa2b9&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记-工具篇20-PrimitiveTexture自定义渲染-贴图](http://blog.sina.com.cn/s/blog_15e866bbe0102y0jm.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247484016&idx=1&sn=4566516a8a9d4d6abf170d5987db2a9c&chksm=fc237f23cb54f635e81424197a77cbd08fa64f21c86838866dac9c2b9a80e61ed82c728b40c5&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记-工具篇21-PrimitiveWaterface渲染水面](http://blog.sina.com.cn/s/blog_15e866bbe0102y0ql.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247484022&idx=1&sn=d498e3b1967a22293ae6be97f550ca87&chksm=fc237f25cb54f633642769f4ed2694c23ca79f1521f9d16dcf562fec8bb5c1e61a9aaa4637b1&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记-工具篇22-PrimitiveEllipse自定义渲染椭圆](http://blog.sina.com.cn/s/blog_15e866bbe0102y0qn.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247484030&idx=1&sn=68b4e42953bd33b57358d53eb67d48c2&chksm=fc237f2dcb54f63b24b5c59cf9afc9ccce7f17b1436bcf9060a0f157b18dea4609d9a2fe8bf7&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记-工具篇23-PrimitiveSector自定义渲染扇形](http://blog.sina.com.cn/s/blog_15e866bbe0102y12s.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247484036&idx=1&sn=0500d38264e47bfbda484f2d92d99351&chksm=fc237fd7cb54f6c1dd1d52a956fd94206d10c0cb561c29859234121cfa35d16147bed505faa3&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记-工具篇24-CesiumCanvas2image场景截屏](http://blog.sina.com.cn/s/blog_15e866bbe0102y136.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&tempkey=MTAxMV85Ylc3Wno0RXNKUnFoS2x6X1FfcmlramdFdjJHX2lWSVJRNFdPT25uSHI2cFJ6aGpmc3dSWFY4MkxoaEptcjlyQ3N0M2hsUURzYjRFMUk1a1ByV3lBdTdlNVpfZVIxbHpuU21udm05V2xZTElDUzA5UHhLdlZ3cVJaY2NVcjdJNXAza2xNRUV5LXVHMG1CY21HZjc4cU1WVTQ3SlRCczk2WDYxNEt3fn4%3D&chksm=7c237fdd4b54f6cb115566461bc7b5205a35547708bf67465e085df853b553612bf91e0a3641#rd)</br>
*[Cesium学习笔记-工具篇25-Cesium加载geoserver影像服务-tif](http://blog.sina.com.cn/s/blog_15e866bbe0102y2iz.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247484064&idx=1&sn=3b9649c9d7fe0cebe7ffbf22308e850d&chksm=fc237ff3cb54f6e5e26e1af5ac2401530e1b907ebfdb7f397fdc9dadc38e7e8d78cf5845547c&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记-工具篇26-Cesium加载geoserver矢量服务-shp](http://blog.sina.com.cn/s/blog_15e866bbe0102y2ps.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247484079&idx=1&sn=50457f77090a89aae4900f6ec7dcdef2&chksm=fc237ffccb54f6ea19b0610ec4a0e18de48fc377129e568905719ef6cc35c8572007f0dfa8e2&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记-工具篇27-Cesium查询wms服务自定义信息框](http://blog.sina.com.cn/s/blog_15e866bbe0102y32b.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247484091&idx=1&sn=66bb880798be047ec876f9707780626e&chksm=fc237fe8cb54f6fe2dc93d5667e7df52f229f12876b53b12f2baec259ed643cd523f35451417&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记-工具篇28-ChangeablePrimitiveClampGround可编辑图形--贴地](http://blog.sina.com.cn/s/blog_15e866bbe0102y47m.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247484131&idx=1&sn=49ee83f63acc32d36aa6769597b94d82&chksm=fc237fb0cb54f6a69a43eb9d59c11441f6cd15e370c6a11a2ba5c0870b97323ed4072e6a5fe8&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记-工具篇29-GetCurrentExtent获取当前场景范围](http://blog.sina.com.cn/s/blog_15e866bbe0102y5no.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247484131&idx=2&sn=8784eefefb00e115a638103a92d49007&chksm=fc237fb0cb54f6a65c609f5325d8d9a661b9b6b8742408a762f0cd09776340c00b03aed6cfb0&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记-工具篇30-CesiumSceneWeather添加雨雪天气场景](http://blog.sina.com.cn/s/blog_15e866bbe0102yfpc.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247484131&idx=3&sn=0699a253a788319511753246f241caed&chksm=fc237fb0cb54f6a6abcaa2294b7e6f982d2d56d6a16b9861ab61183e29b6e8d87d5b6514f544&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记-工具篇31-cesium加载geoserver发布图层组](http://blog.sina.com.cn/s/blog_15e866bbe0102ygtt.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247484145&idx=1&sn=1e00a2f239dc5dd0c1b0b15ca696e8fe&chksm=fc237fa2cb54f6b44572ccdfad9039848ab1ee1e92493367ece5afaebc78bb8290291bc108f6&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记-工具篇32-cesium圆形扫面线](http://blog.sina.com.cn/s/blog_15e866bbe0102yiw2.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247484152&idx=1&sn=9591c6314f9081b522668deab312e8f0&chksm=fc237fabcb54f6bd37ce8ae090f098a1c2c4a0f86572028b26b189705cea6a2438202282e0c6&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记-工具篇33-cesium雷达扫描](http://blog.sina.com.cn/s/blog_15e866bbe0102yj4e.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247484161&idx=1&sn=7de7d21410ed1feaaf80297c381f09db&chksm=fc237e52cb54f7448154be8ea424eb0214bde39ccc38cd5fa34b222346c982b942e2a2ccbecd&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记-工具篇34-cesium流动纹理](http://blog.sina.com.cn/s/blog_15e866bbe0102yjaj.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247484168&idx=1&sn=badf695e4a63903b751ef41d820317f6&chksm=fc237e5bcb54f74ddae2017dda52b18856a580d29ae18e3f7d95c4086b5ff2822d1acab92ba2&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习笔记-工具篇35-cesium流动纹理-飞行路径](http://blog.sina.com.cn/s/blog_15e866bbe0102yjdy.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247484174&idx=1&sn=672704cc04b50e6d70541b22370b5495&chksm=fc237e5dcb54f74bc743aaa0fb70bcd1a99bc566cea9eb43b3adbf424299067c135502de4c24&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习系列-工具篇36-挖地形、态势标绘、可视域](http://blog.sina.com.cn/s/blog_15e866bbe0102ykk1.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247484183&idx=1&sn=419f26da2c26464e7b350d8b5a437706&chksm=fc237e44cb54f7529e42d35fcfa0b68ce48664fc3cc81ccd45ddf07bdaed465091e7e1c7d612&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习系列-工具篇37-风场绘制](http://blog.sina.com.cn/s/blog_15e866bbe0102ykkb.html) [公众号阅读](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247484190&idx=1&sn=761d82ac49bd2e411a5a6005706c53a5&chksm=fc237e4dcb54f75b28f4be1b58603060e76bbf278d42abfc6a76a4d3a92b686ed88353ca088c&token=1964897234&lang=zh_CN#rd)</br>
*[Cesium学习系列-工具篇38-CesiumHeatmap热力图](https://mp.weixin.qq.com/s?__biz=MzU1ODcyMjEwOA==&mid=2247484266&idx=1&sn=d72bf78f5e8799190e4f27b8bb4bc08c&chksm=fc237e39cb54f72f748908c5f877581dfba1e6b492873e928ad8d4cdec0487aa4c3d7bec5b33&scene=21#wechat_redirect)
### WebGL篇
*[Cesium学习笔记-WebGL篇01-绘制圆点、闪烁点](http://blog.sina.com.cn/s/blog_15e866bbe0102yeq7.html) </br>
*[Cesium学习笔记-WebGL篇02-选中对象](http://blog.sina.com.cn/s/blog_15e866bbe0102yfyv.html) </br>
*[Cesium学习笔记-WebGL篇03-blending混合](http://blog.sina.com.cn/s/blog_15e866bbe0102yhw5.html) </br>
*[Cesium学习笔记-WebGL篇04-切换着色器](http://blog.sina.com.cn/s/blog_15e866bbe0102yhwf.html) </br>
*[Cesium学习笔记-WebGL篇05-渲染到纹理](http://blog.sina.com.cn/s/blog_15e866bbe0102yi3v.html) </br>
*[Cesium学习笔记-WebGL篇06-绘制阴影](http://blog.sina.com.cn/s/blog_15e866bbe0102yi8o.html)
### 原理篇
*[Cesium学习笔记-原理篇01-Cesium源码编译](http://blog.sina.com.cn/s/blog_15e866bbe0102y8c2.html) [公众号阅读]()
### 号外
我的学习公众号也开通，感兴趣的小伙伴们可以加关注：giserYZ2SS </br>
![Image text](https://github.com/YanzheZhang/Cesium.HPUZYZ.Demo/blob/master/%E5%85%AC%E4%BC%97%E5%8F%B7.png) </br>
### 示例展示
*1-模型加载 </br>
![Image text](https://github.com/YanzheZhang/Cesium.HPUZYZ.Demo/blob/master/Assets/3-1LoadModel-GLTF.png) </br>
*2-3dtiles加载 </br>
![Image text](https://github.com/YanzheZhang/Cesium.HPUZYZ.Demo/blob/master/Assets/6-1Tileset-Laod.html.png) </br>
*3-场景汉化 </br>
![Image text](https://github.com/YanzheZhang/Cesium.HPUZYZ.Demo/blob/master/Assets/Tools-10Mouse-ButtonLanguage.png) </br>
*4-水面 </br>
![Image text](https://github.com/YanzheZhang/Cesium.HPUZYZ.Demo/blob/master/Assets/Tools-20PrimitiveWaterface.png) </br>
*5-扇形 </br>
![Image text](https://github.com/YanzheZhang/Cesium.HPUZYZ.Demo/blob/master/Assets/Tools-22PrimitiveSector.png) </br>
*6-天气场景-雪 </br>
![Image text](https://github.com/YanzheZhang/Cesium.HPUZYZ.Demo/blob/master/Assets/Tools-29postProcess-Snow.png) </br>
*7-天气场景-雨 </br>
![Image text](https://github.com/YanzheZhang/Cesium.HPUZYZ.Demo/blob/master/Assets/Tools-30postProcess-Rain.png) </br>
*8-挖地形 </br>
![Image text](https://github.com/YanzheZhang/Cesium.HPUZYZ.Demo/blob/master/Assets/CircleClipping.gif) </br>
*9-态势标绘 </br>
![Image text](https://github.com/YanzheZhang/Cesium.HPUZYZ.Demo/blob/master/Assets/Plot.gif) </br>
*10-可视域-基于DEM </br>
![Image text](https://github.com/YanzheZhang/Cesium.HPUZYZ.Demo/blob/master/Assets/Tools-36ViewBaseDEM.gif) </br>
*11-圆形扫描 </br>
![Image text](https://github.com/YanzheZhang/Cesium.HPUZYZ.Demo/blob/master/Assets/Tools32-CricleScan.gif) </br>
*12-雷达扫描 </br>
![Image text](https://github.com/YanzheZhang/Cesium.HPUZYZ.Demo/blob/master/Assets/Tools33-RadarScan.gif) </br>
*13-流动纹理 </br>
![Image text](https://github.com/YanzheZhang/Cesium.HPUZYZ.Demo/blob/master/Assets/Tools34-TrailLine.gif) </br>
*14-飞行航迹 </br>
![Image text](https://github.com/YanzheZhang/Cesium.HPUZYZ.Demo/blob/master/Assets/Tools35-FlyPath.gif) </br>
*15-流场-3d </br>
![Image text](https://github.com/YanzheZhang/Cesium.HPUZYZ.Demo/blob/master/Assets/Tools-37CesiumWind-3d.gif) </br>
*16-流场-2d </br>
![Image text](https://github.com/YanzheZhang/Cesium.HPUZYZ.Demo/blob/master/Assets/Tools-37Wind-2d.gif) </br>
