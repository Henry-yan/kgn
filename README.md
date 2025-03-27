# KGN向量数据库

# 安装

## 配置环境依赖
    sudo apt install -y git cmake g++ python3 python3-setuptools python3-pip libblas-dev liblapack-dev
## 下载代码
    git clone https://github.com/Henry-yan/kgn.git
## 安装
    pip3 install kgn/pykgn-1.0.0-cp310-cp310-linux_x86_64.whl

# 运行
示例python代码(包含构建与搜索)位于`./demo/`中的`run.py`文件，其对应的配置文件为`./demo/config.json`。

# 具体运行示例
## 导入python包
    import pykgn

## 构建索引并保存
    Index = kgn.Index(nb=n, dim=d, base=X, topK=topk,metric=metric,level=level, R=R)
    Index.build(path)
## 读取索引
    Index = kgn.Index(nb=n, dim=d, base=X, topK=topk, metric=metric, level=level, R=R)
    Index.load(path)
## 搜索
    if metric == 'IP':
        q = q / np.linalg.norm(q)
    res = Index.search(ef, q)

# 参数
示例中向量数据库索引的代码为
    Index = kgn.Index(nb=n, dim=d, base=X, topK=topk, metric=metric, level=level, R=R)
其中主要有level和R两个参数，建议取值如下：

| 数据集  |  level | R  |
| ------- | ------------ | ------------ |
|  sift-128-euclidean | 2  | 160  |
| gist-960-euclidean  | 2  | 160  |
| fashion-mnist-784-euclidean  |  2 |  160 |
| glove-25-angular  | 1  |  160 |
| nytimes-256-angular  |  2 | 128  |
|  glove-100-angular | 2  |  128 |





