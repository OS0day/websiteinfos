<template>
  <div>
    <div><H1 style="margin: 0 auto">软件工程师常用网址导航</H1></div>
    <TopNav/>
    <div>
      <el-row>
        <el-col :span="3">
          <LeftNav/>
        </el-col>
        <el-col :span="18">
          <div class="rightBoardPosition">
            <div v-for="url in urls" :key="url" lazy>
              <a :href="url.url" target="_blank">
                <el-col :span="6">
                  <el-image
                      style="width: auto; height: 160px"
                      :src="url.url"
                      class="imagePosition"
                  >
                    <div slot="error" class="image-slot">
                      <i class="el-icon-picture-outline"></i>
                    </div>
                  </el-image>
                  <div>
                    <span><a :href="url.url" target="_blank" style="text-decoration: blink">{{url.title}}</a></span>
                  </div>
                </el-col>
              </a>
            </div>
          </div>
        </el-col>
      </el-row>
    </div>
  </div>
</template>

<script>
import TopNav from '@/components/NavMenu/TopNav/Index'
import LeftNav from '@/components/NavMenu/LeftNav/Index'

export default {
  name: 'HomePage',
  components: {
    LeftNav,
    TopNav
  },
  data() {
    return {
      urls: [
        {
          url: 'https://fuss10.elemecdn.com/a/3f/3302e58f9a181d2509f3dc0fa68b0jpeg.jpeg',
          title: '一'
        },
        {
          url: 'https://fuss10.elemecdn.com/1/34/19aa98b1fcb2781c4fba33d850549jpeg.jpeg',
          title: '二'
        },
        {
          url: 'https://fuss10.elemecdn.com/0/6f/e35ff375812e6b0020b6b4e8f9583jpeg.jpeg',
          title: '仨'
        },
        {
          url: 'https://fuss10.elemecdn.com/9/bb/e27858e973f5d7d3904835f46abbdjpeg.jpeg',
          title: '四'
        },
        {
          url: 'https://fuss10.elemecdn.com/d/e6/c4d93a3805b3ce3f323f7974e6f78jpeg.jpeg',
          title: '五'
        },
        {
          url: 'https://fuss10.elemecdn.com/a/3f/3302e58f9a181d2509f3dc0fa68b0jpeg.jpeg',
          title: '六'
        }
      ]
    }
  }
}
</script>
<style scoped>
.rightBoardPosition{
  margin: 10px auto;
}
.imagePosition{
  margin: 15px auto;
}
a {
  color: #42b983;
}
</style>
