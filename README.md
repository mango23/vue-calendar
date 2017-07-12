# vue-picker

> A Vue.js project

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report

# run unit tests
npm run unit

# run e2e tests
npm run e2e

# run all tests
npm test
```

For detailed explanation on how things work, checkout the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
<template>
    <div id="one">
        <vue-picker :originDateValue="originSetDateValue" :tipsData="tipsData" @set-Calendar="setCalendar" :startYear="startYear" :endYear="endYear"></vue-picker>
    </div>
    </div>
</template>

<script>
    // import Hello from 'Hello'
    import vuePicker from '@/components/vueCalendar'
    
    
    export default {
        name: 'datePickertest',
        data() {
            return {
                today: 0,
                originSetDateValue: '2017-11-8', //设置初始日期
                startYear:1990,
                endYear:2020,
                tipsData: { //传入的日历数据
                    '2017-7-6': [{
                        contest: 'hellohello'
                    }, {
                        'task': ['100', '200']
                    }],
                    '2017-7-5': [{
                        contest: 'pk'
                    }, {
                        'task': ['100', '200']
                    }],
                    '2017-7-9': [{
                        contest: 'nba'
                    }, {
                        'task': ['100', '200']
                    }],
                    '2017-8-5': [{
                        contest: 'hello world'
                    }, {
                        'task': ['100', '200']
                    }],
                     '2017-9-5': [{
                        contest: 'hello world'
                    }, {
                        'task': ['100', '200']
                    }]
    
                }
            }
        },
        methods: {
            setCalendar(args) {
                console.log(args)
            }
        },
        components: {
            vuePicker
        },
        created() {
            // this.init()
        },
        updated() {
    
        },
        mounted() {
    
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    .box {
        width: 100%;
    }
</style>

</html>