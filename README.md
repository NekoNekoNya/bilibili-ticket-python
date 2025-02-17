# B站会员购 蹲票脚本

[![GitHub release](https://img.shields.io/github/v/release/bilibili-ticket/bilibili-ticket-python)](https://github.com/bilibili-ticket/bilibili-ticket-python/releases)
[![Build and Release](https://github.com/bilibili-ticket/bilibili-ticket-python/actions/workflows/ci.yml/badge.svg)](https://github.com/bilibili-ticket/bilibili-ticket-python/actions/workflows/ci.yml)

> 目前处于开发阶段, 我们无法保证软件的稳定性!

## 声明

[电报交流群](https://t.me/bilibili_ticket)

本程序仅供学习交流, 不得用于商业用途,

使用本程序进行违法操作产生的法律责任由操作者自行承担,

对本程序进行二次开发/分发时请注意遵守GPL-3.0开源协议,

本脚本仅适用于蹲回流票, 我们反对将其用于抢票,

黄牛４０００＋.

## 使用

[下载地址](https://github.com/bilibili-ticket/bilibili-ticket-python/releases)

注意:

1. 现仅支持部分活动, 主要是类似于BW2024这样的*实名制 一人一票 无选座*活动, 后期会增加更多类型的票务支持;
2. 如使用浏览器登录功能, 您的电脑里必须安装Chrome/Edge/Firefox浏览器, 如有安装还是提供无法启动, 则需要自行安装其中一个浏览器的Web Driver.

```bash
pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple
pip install poetry virtualenv pre-commit

virtualenv venv
source venv/script/activate
poetry install
python cli.py
```

## 运行流程

![FSM](assest/fsm.png)

## 开发计划

- [ ] 替代inquirer
- [ ] 抢票流程细节补充/修复
- [ ] 成功付款后返回CLI第一步
- [ ] 进度条代替循环的输出
- [ ] 短信验证码错误修复
- [ ] Header补充
- [ ] Pylint
- [ ] UPX
- [ ] JS逆向 + biliTicker_gt
- [ ] 多人购票
- [ ] 多种类型活动抢票
- [ ] 图形界面(PySide6)
- [ ] 网页界面(Gradio)

## 开发

- Python >=3.10,<3.13

```bash
pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple
pip install poetry virtualenv

virtualenv venv
source venv/script/activate
poetry install --with dev,doc,graph
pre-commit install

# 更新
poetry update
pre-commit autoupdate

# 打包
pyinstaller --clean --noconfirm --log-level WARN cli.spec
```

## 感谢

- [Amorter/biliTicker_gt](https://github.com/Amorter/biliTicker_gt)
- [Just-Prog/Bilibili_show_ticket_auto_order](https://github.com/Just-Prog/Bilibili_show_ticket_auto_order)
- [biliticket/BHYG](https://github.com/biliticket/BHYG)
- [mikumifa/biliTickerBuy](https://github.com/mikumifa/biliTickerBuy)
