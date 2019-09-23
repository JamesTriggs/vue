<template>
  <sidebar-menu :menu="menu" />
</template>

<script>
    export default {
        name:'Sidebar',
        data() {
            return {
                menu: [
                    {
                        header: true,
                        title: 'Main Navigation',
                        hiddenOnCollapse: true
                    },
                    {
                        href: '/',
                        title: 'Dashboard',
                        icon: 'fa fa-user'
                    },
                    {
                        to:"/about",
                        //href: '/charts',
                        title: 'Charts',
                        icon: 'fa fa-chart-area',
                        child: [
                            {
                                href: '/charts/sublink',
                                title: 'Sub Link'
                            }
                        ]
                    }
                ]
            }
        },
        props: {
            // Sidebar Collapse state
            collapsed: {
            type: Boolean,
            default: true
            }
        }
    }
</script>

<style>

</style>
