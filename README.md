<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>夜曲优选</title>
    <style>
        /* 网页占据浏览器的全部高度 */
        html,
        body {
            height: 100%;
        }
        
        /* 重置body内外边距,将内容按列布局 */
        body {
            /* 设置布局 */
            display: flex;
            flex-direction: column;
            margin: 0;
            padding: 0;
        }

        /* 设置导航栏样式 */
        .top {
            /* 设置布局方式 */
            display: flex;
            justify-content: center;

            /* 盒子大小、颜色 */
            width: 100%;
            height: 40px;
            color: #C4C4C4;
            font-size: 12px;
            background-color: #333333;
        }

        /* 为top中的段落布局 */
        .top p {
            margin-right: 20%;
        }

        /* 设置列表的布局方式 */
        ul {
            display: flex;
        }

        /* 取消原点、添加边框 */
        ul li {
            list-style-type: none;
            border-right: 1px solid #C4C4C4;
        }

        /* 取消最后一个元素的边框 */
        ul li:last-child {
            border-right: none;
        }

        /* 设置a元素样式 */
        ul a {
            color: #c4c4c4;
            text-decoration: none;
            padding: 0 20px;
        }

        .footer {
            width: 100%;
            height: 40px;
            background-color: #333333;
            color: #C4C4C4;
            font-size: 12px;
            text-align: center;
            line-height: 40px;
            /* margin-top: 20px; */
        }

        .shop {
            /* 商城占据页面的所有空间 */
            flex: auto;
            /* 设置商城区域的宽度、并居中显示 */
            width: 930px;
            margin: auto;
        }

        /* 商城头部样式 */
        .header {
            /* 设置布局 */
            display: flex;
            justify-content: space-between;
            width: 100%;
            margin-top: 25px;
            background-color: white;
            border-radius: 0 0 8px 8px;
            position: sticky;
            top: 0px;
        }

        /* 设置表单样式 */
        .search form {
            display: flex;
            border: 1px solid #2F5DF2;
            border-radius: 26px;
            width: 400px;
            height: 26px;
        }

        /* 取消input的默认边框 */
        .header input {
            border: none;
            border-radius: 26px;
            font-size: 12px;
        }

        /* 设置输入框样式 */
        .header input[type="text"] {
            width: 80%;
            margin: 0 10px;
        }

        /* 设置按钮样式 */
        .header input[type="submit"] {
            /* 设置大小与颜色 */
            background-color: #2F5DF2;
            color: #FFFFFF;
            width: 20%;
        }

        /* 整体样式 */
        .banner {
            width: 100%;
            display: flex;
            justify-content: center;
            margin-top: 20px;
        }

        /* 横幅广告大小 */
        .ad {
            width: 80%;
            height: 311px;
        }

        /* 菜单样式 */
        .menu {
            width: 20%;
            height: 311px;
            background-color: #2F5DF2;
        }

        .menu p, .menu a {
            text-decoration: none;
            color: #FFFFFF;
            text-align: center;
            font-size: 12px;
            padding: 4px 0;
        }

        .menu a:hover {
            color: yellow;
            cursor: pointer;
        }

        /* 商品样式 */
        .goods {
            width: 100%;
            margin-top: 20px;
        }

        .goods_title {
            font-size: 25px;
            color: #333333;
        }

        .container {
            width: 100%;
            display: flex;
            justify-content: space-between;
        }

        .item img {
            padding: 10px 0;
        }

        .item {
            font-size: 13px;
            text-align: center;
            background-color: #FFFFFF;
            transition: all 0.3s;
        }

        .item:hover {
            border-radius: 12px;
            cursor: pointer;
            box-shadow: 0 19px 39px 0 #999999;
            transform: translate(0, -4px);
        }

        .name {
            color: #333333;
        }

        .info {
            color: #787878;
        }

        .price {
            color: #E92845;
            font-weight: 500;
        }
        
        /* TODO 为price类中的span元素设置样式，要求：
             1、字体颜色为#787878，大小为12px；
             2、在文字中添加删除线；
             3、设置左右内边距为10px（上下为0）。
          */
        .price span {
            color: #787878;
            font-size: 12px;
            text-decoration: line-through;
            padding: 0 10px 0 10px;
        }
    </style>
</head>

<body>
    <!--导航栏-->
    <div class="top">
        <p>优选欢迎你</p>
        <ul>
            <li><a href="#">登录</a></li>
            <li><a href="#">注册</a></li>
            <li><a href="#">我的订单</a></li>
            <li><a href="#">个人中心</a></li>
            <li><a href="#">帮助中心</a></li>
        </ul>
    </div>

    <!-- 商品内容 -->

    <div class="shop">
        <!--搜索栏-->
        <div class="header">
            <!-- LOGO -->
            <div class="logo">
                <img src="http://nocturne.bczcdn.com/file/1654596484278_38295/Frame.png" width="127px" height="32px">
            </div>
            <!-- 搜索栏 -->
            <div class="search">
                <form action="#">
                    <input type="text" placeholder="请输入搜索内容">
                    <input type="submit" value="搜一搜">
                </form>
            </div>
        </div>

        <!-- 分类与横幅广告  -->
        <div class="banner">
            <!-- 分类菜单 -->
            <div class="menu">
                <p><a href="#">优选推荐</a> / <a href="#">手机数码</a></p>
                <p><a href="#">家用电器</a> / <a href="#">智能家庭</a></p>
                <p><a href="#">美容美妆</a> / <a href="#">鞋靴箱包</a></p>
                <p><a href="#">电脑办公</a> / <a href="#">实用工具</a></p>
                <p><a href="#">服装配饰</a> / <a href="#">运动户外</a></p>
                <p><a href="#">健康保养</a> / <a href="#">美妆个护</a></p>
                <p><a href="#">日用文创</a> / <a href="#">家纺餐厨</a></p>
                <p><a href="#">美酒乳饮</a> / <a href="#">休闲零食</a></p>
            </div>
            <!-- 广告 -->
            <div class="ad">
                <img src="http://nocturne.bczcdn.com/file/1655778990948_37974/ad.png" height="311px">
            </div>
        </div>

        <!-- 新品首发 -->
        <div class="goods">
            <p class="goods_title">新品首发</p>
            <div class="container">
                <div class="item">
                    <img src="http://nocturne.bczcdn.com/file/1654592718319_27806/Rectangle 11.png">
                    <p class="name">指甲油</p>
                    <p class="info">持久滋养强韧打底</p>
                    <p class="price">￥299</p>
                </div>
                <div class="item">
                    <img src="http://nocturne.bczcdn.com/file/1654589721254_13972/image 12.png">
                    <p class="name">睫毛膏</p>
                    <p class="info">加密加长惊艳旋翘睫毛膏</p>
                    <p class="price">￥399</p>
                </div>
                <div class="item">
                    <img src="http://nocturne.bczcdn.com/file/1654592732264_60234/Rectangle 13.png">
                    <p class="name">四色散粉</p>
                    <p class="info">四色散粉1号 慕斯淡彩 12g</p>
                    <p class="price">￥559</p>
                </div>
                <div class="item">
                    <img src="http://nocturne.bczcdn.com/file/1654592764559_90265/Rectangle 14.png">
                    <p class="name">睫毛膏</p>
                    <p class="info">立体臻魅睫毛膏</p>
                    <p class="price">￥499</p>
                </div>
                <div class="item">
                    <img src="http://nocturne.bczcdn.com/file/1654592788696_97648/Rectangle 15.png">
                    <p class="name">口红</p>
                    <p class="info">菁纯丝绒雾面哑光唇膏</p>
                    <p class="price">￥599</p>
                </div>
            </div>
        </div>
       
        <div class="goods">
            <p class="goods_title">优选秒杀</p>
            <div class="container">
                <div class="item">
                    <img src="http://nocturne.bczcdn.com/file/1654592806852_60086/Rectangle 16.png">
                    <p class="name">清透持妆粉底液</p>
                    <p class="info">控油持妆</p>
                    <p class="price">￥499<span>￥599</span></p>
                </div>
                <div class="item">
                    <img src="http://nocturne.bczcdn.com/file/1654593266543_22664/fen.png">
                    <p class="name">粉饼</p>
                    <p class="info">遮瑕干湿两用</p>
                    <p class="price">￥399<span>￥499</span></p>
                </div>
                <div class="item">
                    <img src="http://nocturne.bczcdn.com/file/1654592868499_25301/Rectangle 18.png">
                    <p class="name">男士淡香水60ml</p>
                    <p class="info">木质香调 持久香氛</p>
                    <p class="price">￥539<span>￥739</span></p>
                </div>
                <div class="item">
                    <img src="http://nocturne.bczcdn.com/file/1654592840373_77690/Rectangle 19.png">
                    <p class="name">口红</p>
                    <p class="info">魅惑釉唇膏</p>
                    <p class="price">￥899<span>￥999</span></p>
                </div>
                <div class="item">
                    <img src="http://nocturne.bczcdn.com/file/1654592897223_25009/Rectangle 20.png">
                    <p class="name">美妆包</p>
                    <p class="info">送老婆 送女友 生日礼物</p>
                    <p class="price">￥799<span>￥999</span></p>
                </div>
            </div>
        </div>
    </div>

    <!-- 页脚 -->
    <div class="footer">Copyright@夜曲优选</div>
</body>

</html>



<div>

    
    <p>hello，everyone,这是一个李怡宁做到小网站
    to lily</p>
    <img src="https://img2.baidu.com/it/u=1451850213,890568603&fm=253&fmt=auto&app=120&f=JPEG?w=500&h=670"
    alt="lilyflower" width="100px">
    <p>lilyflower</p>
</div>
