<template>
    <div>
        <el-table
                :data="tableData"  
                border  
                ref="multipleTable" 
                style="width: 100%"
                class="m20"
            >
            <sort></sort>
        </el-table>
        <el-row class="m20" v-if="total>0">
            <el-button type="primary" style="float:left" @click="handelConfigAll" :disabled="multipleSelection.length==0">批量分配</el-button>
             <div style="float:right">
                 <el-pagination
                   @current-change="handleCurrentChange"
                    @size-change="handleSizeChange"
                   :current-page="npage"
                    :page-sizes="[10, 20, 30, 40]"
                     :page-size="pagesize"
                   background
                   layout="total,sizes,prev, pager, next,jumper"
                   :total="total">
                 </el-pagination>   
             </div>
        </el-row>        
    </div>
</template>

<script>
</script>

<style lang="scss" scoped>
</style>

