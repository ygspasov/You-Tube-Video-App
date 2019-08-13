<template>

    <ul class="list-group list-group-flush col-md-4">
      <VideoListItem
      :video="video"  
      v-for="video in videos"
      :key="video.etag"
      @videoSelect="onVideoSelect"></VideoListItem>
    </ul>
  
</template>

<script>
import VideoListItem from './VideoListItem';
export default {
  props: {
      videos: Array
  },
  name: "VideoList",
  components: {
    VideoListItem
  },
  methods: {
    onVideoSelect(video){
      this.$emit('videoSelect',video);
    }
  }
};
</script>

<style>
</style>
