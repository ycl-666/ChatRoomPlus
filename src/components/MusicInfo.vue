<!--
 * @Author: YCL
 * @Date: 2021-07-04 17:50:51
 * @LastEditTime: 2021-07-06 16:42:57
 * @LastEditors: Author YCl
 * @Description: 
 * @FilePath: \web\src\components\MusicInfo.vue
-->
:<template>
  <div class="show_music_info">
    <svg
      xmlns="http://www.w3.org/2000/svg"
      xmlns:xlink="http://www.w3.org/1999/xlink"
      width="280"
      height="160"
    >
      <clipPath id="songBgPath">
        <use xlink:href="#songBgRech" />
      </clipPath>
      <clipPath id="songImagePath">
        <use xlink:href="#songImageRect" />
      </clipPath>
      <g
        font-family="Consolas, PingFangSC-Regular, Microsoft YaHei"
        font-size="15"
      >
      <foreignObject x="137" y="22" width="120" height="100">
        <div style="color: orange; overflow: hidden; text-overflow: ellipsis; white-space: nowrap;">
         {{ songInfo.song.name }}
        </div>
      </foreignObject>

        <!-- <text x="137" y="41" fill="orange"></text> -->
      </g>

      <g
        font-family="Consolas, PingFangSC-Regular, Microsoft YaHei"
        font-size="14"
      >
        <text size="16" x="138" y="60" fill="orange">
          {{ songInfo.song.singer }}
        </text>
      </g>
      <g
        font-family="Consolas, PingFangSC-Regular, Microsoft YaHei"
        font-size="12"
      >
        <text size="16" x="138" y="100" fill="#097ad8">
          点歌人: {{ songInfo.user.user_name }}
        </text>
      </g>

      <a
        xlink:href="#"
        target="_blank"
        style="cursor: pointer"
      >
        <g
          font-family="Consolas, PingFangSC-Regular, Microsoft YaHei"
          font-size="12"
          text-anchor="right"
        >
          <text size="16" x="138" y="120" fill="orangered">
            ID:{{ global.room_id }}    {{ global.roomInfo.room_name }}
          </text>
        </g>
      </a>
    </svg>
  </div>
</template>
<script>
export default {
  props: ["songInfo"],
};
</script>
<style>
</style>