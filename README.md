# mai_draw

## 项目简介

`mai_draw` 是一个使用 Python 编写用于生成与舞萌DX机台上方副屏风格相似图片的工具。

1. [安装](#安装)
2. [使用示例](#项目简介)

### 安装

克隆项目到本地；

通过[链接](https://1drv.ms/u/s!AoBHZVMZvJZscVmqRoY5ecLbst8?e=PUHXwh)下载项目的资源文件，然后将压缩包中的`out`文件夹复制到项目根目录中；

在项目根目录下运行以下命令安装所需的依赖：

```sh 
pip install -r requirements.txt
```

### 示例

#### 代码示例

```python
from draw import CardDraw, UserChara

if __name__ == '__main__':
    cd = CardDraw(
        name="gllc",
        icon=255201,
        title=255299,
        plate=255201,
        frame=255201,
        chara=[
            UserChara(characterId=255201, level=61),
            UserChara(characterId=255202, level=157),
            UserChara(characterId=255203, level=604),
            UserChara(characterId=255204, level=1376),
            UserChara(characterId=200201, level=9999),
        ]
    )
    cd.draw()
    cd.get_image().save("example.png")
```

#### 输出结果

![example.png](example.png)

#### 致谢
字体来源项目[Error063/maicard](https://github.com/Error063/maicard)
