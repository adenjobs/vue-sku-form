<template>
    <div>
        <SkuForm
            :spec-types="specTypes"
            :max-specs="4"
            :source-attribute="sourceAttribute"
            :attribute.sync="attribute"
            :sku.sync="sku"
        />
        <el-row type="flex" :gutter="20">
            <el-col>
                <el-divider content-position="left">attribute 数据</el-divider>
                <pre><code>{{ attribute }}</code></pre>
            </el-col>
            <el-col>
                <el-divider content-position="left">sku 数据</el-divider>
                <pre><code>{{ sku }}</code></pre>
            </el-col>
        </el-row>
    </div>
</template>

<script>
export default {
    data() {
        return {
            sourceAttribute: [
                {
                    name: '颜色',
                    item: ['黑', '金', '白']
                },
                {
                    name: '内存',
                    item: ['16G', '32G']
                }
            ],
            attribute: [],
            sku: [],
            specTypes: [
                {
                    id: 1,
                    name: '尺寸'
                },
                {
                    id: 2,
                    name: '型号'
                },
                {
                    id: 3,
                    name: '款式'
                },
                {
                    id: 4,
                    name: '器型'
                },
                {
                    id: 5,
                    name: '材质'
                },
                {
                    id: 6,
                    name: '口味'
                }
            ]
        }
    }
}
</script>
