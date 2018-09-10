## 说明

此项目模板用于测试feflow的基于webpack的构建器

构建器要求支持多页面构建、less、热更新。

## 使用

将此项目`git clone`到`./test/`目录下

请自行编写测试代码，测试开发环境和生产环境的构建是否能够成功。

## 建议测试用例：

在`.travis.yml`中配置如下命令：
```
language: node_js

sudo: false

cache:
  apt: true
  directories:
    - node_modules

node_js: stable  #设置相应的版本

install:
  - npm install -D  #安装builder-webpack3依赖
  - cd ./test/template-project
  - npm install -D #安装模板项目依赖

script:
  - npm test
```
