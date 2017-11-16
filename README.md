CEOS 数据立方体（Data Cube）用户界面系统
=================
CEOS 数据立方体（Data Cube）用户界面系统是一个完全基于Python的网络应用程序，该程序采用数据立方体（Data Cube）对栅格数据集进行分析。基于通用和广泛接受的程序框架和类库，使得我们的用户界面在展示数据立方体的能力以及一些可能的应用程序和架构方面，成为了一个很好的工具。用户界面的核心技术包括：
* [**Django**](https://www.djangoproject.com/): 前端网络程序框架, 对象关系映射（ORM）, 模板处理程序, 纯模型(M)－视图(V)－控制器(C)堆栈
* [**Celery + Redis**](http://www.celeryproject.org/): 异步任务处理
* [**Data Cube**](http://datacube-core.readthedocs.io/en/stable/): 数据访问和分析接口
* [**PostgreSQL**](https://www.postgresql.org/): 后端数据库
* **Apache/Mod WSGI**: 一种基于标准服务的应用程序，支撑Django应用程序运行，同时也为静态文件提供托管
* [**Bootstrap3**](http://getbootstrap.com/): 一种简单、标准、易用的前端样式

采用这些通用技术为想开发数据立方体（Data Cube）应用程序的用户提供了一个良好的启动平台。采用Celery可以执行简单的分布式任务处理，同时还能保持性能。我们的用户界面是为高水平使用数据立方体而设计的，并允许用户执行:
* Access various datasets that we have ingested访问数据立方体中的各种数据集
* 运行用户选择区域和时间范围的自定义分析案例
* 生成可视(图像)和数据产品 (GeoTiff/NetCDF)
* 提供易于访问的元数据和运行的历史分析案例

系统安装
=================
```
git clone https://github.com/ceos-seo/data_cube_ui.git -b master
cd ~/Datacube/data_cube_ui
git submodule init && git submodule update
```

系统要求
=================

* Full Data Cube installation with ingested data

* apache2
* libapache2-mod-wsgi-py3
* redis-server
* libfreeimage3
* tmux
* django
* redis
* celery
* imageio
* django-bootstrap3
* matplotlib
* stringcase

更详细的说明, 请阅读该[文档](docs/ui_install.md). 如果你想给系统添加一个新的算法, 你可以参考[添加一个新的算法](docs/adding_new_pages.md) 文档.
