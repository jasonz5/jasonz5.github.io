---
layout: post
title:  ChatGPT Plus 支付教程
date:   2023-11-04 16:40:16
description: 记录从openai账号注册到Plus支付，以及避开风控的建议。
tags: openai
categories: 效率工具
toc:
  sidebar: right
---

>💡因为openai的风控，用了一个月的plus号后又不能支持虚拟信用卡支付了，每次重新注册openai账号和支付流程都很繁琐，特此总结下流程，方便后续查阅，本博客内容主要总结于[VPS大玩家](https://www.vpsdawanjia.com/)。

## ChatGPT注册准备

1. 注册环境：国外的ip，ip地址建议和电话号码的国家保持相同
   + 方式一：机场，缺点是ip不纯净（容易支付失败
   + 方式二：使用美国的VPS/住宅IP。
2. 国外手机号码：使用接码平台[sms-activate.org](https://sms-activate.org/cn)。
3. 电子邮箱：建议使用Gmail邮箱。
   + 注册谷歌邮箱流程
     + 准备工作：**使用Edge浏览器+无痕模式**；如果是Chrome需要退出之前的Google账号并清空浏览器缓存，然后使用无痕模式。
     + 注册网址连接：[英文](https://support.google.com/accounts/answer/27441?hl=en) [中文](https://support.google.com/accounts/answer/27441?hl=zh-Hans)
     + Tips：按准备工作走可以避免手机号码验证，如果没有避免，使用接码平台。


## ChatGPT注册流程
- 注册官网：[chat.openai.com](https://chat.openai.com/auth/login) 
- Tips：Edge浏览器无痕模式注册，运气好的话可以避开短信验证，没有的话就平台接码。

## 订阅ChatGPT Plus
#### 准备工作
- 虚拟信用卡购买网址：
  - [倍易付vvcard](https://www.vvacard.com)
- 信用卡注册要点
  - 美国五个免税州：使用免税州的帐单地址，可以免消费税
    - 特拉华州 Delaware
    - 新罕布什尔州 New Hampshire
    - 蒙大拿州 Montana
    - 俄勒冈州 Oregon
    - 阿拉斯加州 Alaska
  - 账单地址填写
    - [如何在谷歌(Google)地图上找一个真实的美国地址](https://www.vpsdawanjia.com/2594.html)
    - [zillow](www.zillow.com) 租房网站上找
    - 基本原则：卡是哪个国家的，就用哪个国家的地址

#### 支付一：openai官网上信用卡支付
缺点：容易被风控

#### 方式二：Apple Pay支付
优点：这种订阅方式成功率很高，后面续费也容易，因为OpenAI无法通过卡头过行风控。

前提条件：独享的美区id，注册教程：[2023年美区apple id注册教程，无需信用卡，直接使用中国IP注册](https://www.vpsdawanjia.com/6863.html)。

Tips：如果通过Apple ID注册ChatGPT帐号，建议选择“隐藏邮件地址”，避免OpenAI通过邮件地址风控账号。

## 购买API key
网站：[OpenAI platform](https://platform.openai.com/)

1. 绑定付款方式
  <p align="center">
    <img src="https://www.vpsdawanjia.com/wp-content/uploads/2023/03/setuppaidaccount.png" alt="Your image alt text" style="width: 100%; height: auto;"/>
  </p>
2. 绑卡时要预扣5美元，因此在绑卡前，一定要保证卡上至少有5美元的余额，否则会绑卡失败！另外，如果IP不干净，也会导致绑卡不成功。


## 其他
**信息补充：**
  1. **准备好IP地址以后，可以通过whoer.net和ipdata.co评估一下自己的注册环境和IP的质量。**
  2. 倍易付虚拟信用卡：根据虚拟信用卡平台的反馈，目前556766、556735以及531847已经不能充值ChatGPT。（2023年6月17日更新）
  3. 如果在订阅ChatGPT Plus过程中遇到“信用卡被拒绝”的信息提示，那么这个账号就极有可能进入openai的风控名单，建议注册新账号订阅。

**常见问题**
1. 为什么老号不容易支付成功？
    - 因为注册以及后期使用时，使用了不同的IP地址登录，IP地址在不同的国家和地区跳来跳去，被OpenAI列入了风控名单。
2. 老号有机会支付成功吗？
    - 有！但是非常难，可以通过更换不同的IP来解决。美国不行就换新加坡、日本，或者别的地区，总有能成功的。只是买来的VPN哪有干净、独享的IP地址，大概率不能成功。
3. 升级成功后可以使用购买的梯子登录使用吗？
    - 可以，但是记得提前往虚拟信用卡存入足够的资金来支付月租续费。如果ChatGPT自动扣费不成功，有可能又要重新注册新号。


Reference：
- [2023年ChatGPT、OpenAI注册付费购买教程](https://www.vpsdawanjia.com/6177.html)
- [ChatGPT Plus如何购买？信用卡付款失败怎么办？如何使用Apple Pay升级ChatGPT Plus](https://www.vpsdawanjia.com/6220.html)
- [如何获得OpenAI API Key及OpenAI绑卡充值教程](https://www.vpsdawanjia.com/6455.html)

