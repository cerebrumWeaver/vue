<template>
    <el-select v-model="selectValue"
               placeholder="选择文件下载"
               size="large"
    >
        <el-option
                v-for="item in list"
                :key="item.value"
                :label="item.label"
                :value="item.value"
        >
        </el-option>
    </el-select>
    <el-button type="info" plain  v-if="selectValue!=''">
    <a :href=selectValue download>Download</a>
    </el-button>

</template>

<script lang="ts">
  import { defineComponent, ref, computed } from "vue";
  import {useStore} from "vuex"


  export default defineComponent({
    data(){
      return{
        isEmpty:false,
      }
    },
    setup() {
      let store = useStore()
      let list = computed(()=> {
        return store.state.url
      })


      return {
        options: ref([
          {
            value: "CleanBases.pdf",
            label: "CleanBases.pdf"
          },
          {
            value: "CleanBases.png",
            label: "CleanBases.png"
          },
          {
            value: "Option3",
            label: "Option3"
          },
          {
            value: "Option4",
            label: "Option4"
          },
          {
            value: "Option5",
            label: "Option5"
          }
        ]),
        list,
        selectValue: ref(""),

      };
    },
    methods: {
      methods2: function() {

      }
    }
  });
</script>
