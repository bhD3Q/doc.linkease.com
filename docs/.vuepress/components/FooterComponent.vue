<template>
    <div class="footer">
        <div class="footer-content max-width">
            <div class="content_text">
                <div class="content_block">
                    <template v-for="(item, i) in menus">
                        <ul class="content_list" :key="i">
                            <li class="content_title" :title="item.title">{{ item.title }}</li>
                            <template v-for="(ole, k) in item.childer">
                                <li :key="k"><a :href="ole.value" :title="ole.label" target="_blank">{{ ole.label }}</a>
                                </li>
                            </template>
                        </ul>
                    </template>
                </div>
            </div>
            <div class="content_info" title="易有云网络科技有限责任公司 Copyright © 2019-2021  备案号： 粤ICP备20024441号">易有云网络科技有限责任公司
                Copyright © 2019-2021<br />
                <a href="https://beian.miit.gov.cn/#/Integrated/index" target="_blank">备案号： 粤ICP备20024441号</a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            menus: [
                {
                    title: "所有产品",
                    childer: [
                        {
                            label: "iStoreOS",
                            value: "/zh/guide/istoreos/",
                        },
                        {
                            label: "易有云软件",
                            value: "https://app.linkease.com/",
                        },
                        {
                            label: "DDNSTO",
                            value: "https://www.ddnsto.com",
                        },
                        {
                            label: "iStore",
                            value: "/zh/guide/istore/",
                        },
                        {
                            label: "EasePi",
                            value: "https://easepi.linkease.com",
                        }
                    ]
                },
                {
                    title: "购买渠道",
                    childer: [
                        {
                            label: "KoolCenter淘宝店",
                            value: "https://koolcenter.taobao.com/"
                        }
                    ]
                },
                {
                    title: "帮助与沟通",
                    childer: [
                        {
                            label: "问题反馈",
                            value: "https://github.com/linkease/doc.linkease.com/issues"
                        },
                        {
                            label: "商务洽谈",
                            value: "mailto:admin@linkease.com"
                        }

                    ]
                },
                {
                    title: "关于易有云",
                    childer: [
                        {
                            label: "关于我们",
                            value: "https://www.linkease.com/about"
                        },
                        // {
                        //     label: "联系我们",
                        //     value: "mailto:xiaobao@linkease.com"
                        // }
                    ]
                },
                {
                    title: "合作伙伴",
                    childer: [
                        {
                            label: "KoolCenter",
                            value: "https://www.koolcenter.com/"
                        },
                    ]
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
* {
    -webkit-box-sizing: border-box;
    -webkit-tap-highlight-color: transparent;
    box-sizing: border-box;
    word-wrap: break-word;
    outline: none;
}

.footer {
    // background-color: #f4f4f4;
    min-height: 234px;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;

    .footer-content {
        display: flex;
        flex-wrap: wrap;

        .content_text {
            width: 1064px;
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            flex: 0 0 100%;
            border-bottom: 1.5px solid rgba(0, 0, 0, 0.7);
            margin-bottom: 10px;
            border-top: 1.5px solid rgba(0, 0, 0, 0.7);
            padding-top: 24px;
            padding-bottom: 14px;

            .content_block {
                display: flex;
                justify-content: space-between;
                flex-wrap: wrap;
                width: 1020px;

                .content_list {
                    padding: 0;
                    margin: 0;

                    .content_title {
                        font-size: 16px;
                        font-family: PingFangSC-Semibold, PingFang SC;
                        font-weight: 600;
                        color: #000000;
                        line-height: 22px;
                        padding-bottom: 22px;
                    }

                    a {
                        display: block;
                        font-size: 14px;
                        font-family: PingFangSC-Regular, PingFang SC;
                        font-weight: 400;
                        color: #464646;
                        line-height: 20px;
                        margin-bottom: 8px;
                    }

                    a:hover {
                        color: #0060ff;
                    }
                }
            }
        }

        .content_info {
            flex: 0 0 100%;
            font-size: 12px;
            color: #8e8e8e;

            a {
                color: #8e8e8e;
            }

            a:hover {
                color: #0060ff;
            }
        }
    }
}

li {
    list-style: none;
}
</style>
<style lang="scss" scoped>
@media screen and (max-width:1300px) {
    .footer {
        .footer-content {
            .content_text {
                // padding-bottom: 0px;
                padding: 20px 20px 0;

                .content_block {
                    width: 100%;
                    padding: 0px;

                    .content_list {
                        flex: 0 0 100%;
                        max-width: 25%;
                        margin: 0;
                        padding: 0;
                        margin-bottom: 20px;

                        .content_title {
                            padding-bottom: 8px;
                        }

                        a {
                            margin-bottom: 2px;
                        }
                    }
                }
            }
        }
    }
}

@media screen and (max-width:1100px) {
    .footer {
        .footer-content {
            .content_text {
                // width: 100%;
                padding: 20px 20px 0;

                // .content_block {
                //     // width: 100%;
                //     padding: 0;
                // }
            }
        }
    }
}

@media screen and (max-width:900px) {
    .footer {
        .footer-content {
            .content_text {
                width: 100%;
                padding: 20px 20px 0;

                .content_block {
                    width: 100%;
                    padding: 0 10px;

                    .content_list {
                        flex: 0 0 100%;
                        max-width: 50%;
                        margin: 0;
                        padding: 0;
                        margin-bottom: 14px;

                        .content_title {
                            padding-bottom: 6px;
                        }

                        a {
                            margin-bottom: 6px;
                        }
                    }
                }
            }

            // .content_info {
            //     padding-left: 10px;
            // }
        }
    }
}
</style>
