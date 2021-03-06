
# [打造个人户外运动主页](http://workouts.ben29.xyz) 
简体中文 | [English](README.md)

本项目基于 [running_page](https://github.com/yihong0618/running_page/blob/master/README-CN.md) , 添加了支持多种运动类型。部署可参考原项目操作步骤

## 新增特性
1. 支持多种运动类型，如骑行、徒步、游泳
1. 新增支持
    - **[咕咚](#codoon咕咚)** (因咕咚限制单个设备原因，无法自动化)
    - **[行者](#行者)**

## 一些个性化选项

### 自定义运动颜色

* 修改骑行颜色: `src/utils/const.js` 里的 `RIDE_COLOR`

### 新增运动类型
* 修改 `scripts/config.py`, `TYPE_DICT` 增加类型映射关系
* 修改 `src/utils/util.js` 里的 `colorFromType`, 增加case

---
### Codoon（咕咚）

<details>
<summary>获取您的咕咚数据</summary>

```python
python3(python) scripts/codoon_sync.py ${your mobile or email} ${your password}
```

示例：
```python
python3(python) scripts/codoon_sync.py 13333xxxx xxxx
```

> 注：我增加了 Codoon 可以导出 gpx 功能, 执行如下命令，导出的 gpx 会加入到 GPX_OUT 中，方便上传到其它软件

```python
python3(python) scripts/codoon_sync.py ${your mobile or email} ${your password} --with-gpx
```

示例：

```python
python3(python) scripts/codoon_sync.py 13333xxxx xxxx --with-gpx
```

> 注：因为登录token有过期时间限制，我增加了 refresh_token&user_id 登陆的方式， refresh_token 及 user_id 在您登陆过程中会在控制台打印出来

![image](https://user-images.githubusercontent.com/6956444/105690972-9efaab00-5f37-11eb-905c-65a198ad2300.png)

示例：

```python
python3(python) scripts/codoon_sync.py 54bxxxxxxx fefxxxxx-xxxx-xxxx --from-auth-token
```

</details>

### 行者

<details>
<summary>获取您的行者数据</summary>

```python
python3(python) scripts/xingzhe_sync.py ${your mobile or email} ${your password}
```

示例：
```python
python3(python) scripts/xingzhe_sync.py 13333xxxx xxxx
```

> 注：我增加了 行者 可以导出 gpx 功能, 执行如下命令，导出的 gpx 会加入到 GPX_OUT 中，方便上传到其它软件

```python
python3(python) scripts/xingzhe_sync.py ${your mobile or email} ${your password} --with-gpx
```

示例：

```python
python3(python) scripts/xingzhe_sync.py 13333xxxx xxxx --with-gpx
```

> 注：因为登录token有过期时间限制，我增加了 refresh_token&user_id 登陆的方式， refresh_token 及 user_id 在您登陆过程中会在控制台打印出来

![image](https://user-images.githubusercontent.com/6956444/106879771-87c97380-6716-11eb-9c28-fbf70e15e1c3.png)

示例：

```python
python3(python) scripts/xingzhe_sync.py w0xxx 185000 --from-auth-token
```

</details>


# 致谢
- @[yihong0618](https://github.com/yihong0618) 特别棒的项目 [running_page](https://github.com/yihong0618/running_page) 非常感谢
