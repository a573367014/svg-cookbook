<style lang="less">
    @import './less/main.less';
</style>

<style lang="css">
    @import './css/main.css';
</style>

<template>
    <div id="app">
        <aside>
            <ul class="mod-menu list-chapter">
                <li
                    v-for="(chapter, index) in chapters"
                    :key="index"
                    class="item"
                >
                    <router-link
                        :to="chapter.route"
                        :class="{active: $route.path.startsWith(chapter.route)}"
                        v-text="chapter.name">
                    </router-link>
                </li>
            </ul>
        </aside>
        <router-view></router-view>
    </div>
</template>

<script>
    /**
     * 这个文件提供了路由的挂载元素
     */
    import './components/categories';

    export default {
        data() {
            return {
                chapters: [
                    {
                        name: '坐标系统',
                        route: '/coordinates'
                    }, {
                        name: '基本形状',
                        route: '/basic-shapes'
                    }, {
                        name: '坐标系统转换',
                        route: '/transforming-the-coordinate-system'
                    }, {
                        name: '路径',
                        route: '/paths'
                    }, {
                        name: '图案和渐变',
                        route: '/patterns-and-gradients'
                    }, {
                        name: '文本',
                        route: '/text'
                    }, {
                        name: '裁剪',
                        route: '/clip-path'
                    }, {
                        name: '蒙版',
                        route: '/mask'
                    }, {
                        name: '滤镜',
                        route: '/filters'
                    }, {
                        name: '动画',
                        route: '/animation'
                    }, {
                        name: '交互',
                        route: '/interactivity'
                    }, {
                        name: '实例',
                        route: '/instances'
                    }, {
                        name: 'lottie',
                        route: '/lottie'
                    }, {
                        name: 'Snap.svg',
                        route: '/snapsvg'
                    },

                    // {
                    //     name: '入门指南',
                    //     route: '/getting-started'
                    // }, {
                    //     name: '文档结构',
                    //     route: '/document-structure'
                    // }, {
                    //     name: '生成',
                    //     route: '/generating-svg'
                    // }, {
                    //     name: 'serving',
                    //     route: '/serving-svg-files'
                    // }, {
                    //     name: 'DOM',
                    //     route: '/dom'
                    // }, {
                    //     name: '附录 - XML',
                    //     route: '/appendix-xml'
                    // }, {
                    //     name: '附录 - 样式表',
                    //     route: '/appendix-stylesheets'
                    // }, {
                    //     name: '附录 - 编程概念',
                    //     route: '/appendix-programming-concepts'
                    // }, {
                    //     name: '附录 - 矩阵代数',
                    //     route: '/appendix-matrix-algebra'
                    // }, {
                    //     name: '附录 - 创建字体',
                    //     route: '/appendix-creating-fonts'
                    // }, {
                    //     name: '附录 - 应用',
                    //     route: '/appendix-applications'
                    // },
                ]
            }
        }
    };
</script>
