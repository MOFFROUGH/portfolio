<template>
  <div>
    <vue-goodshare-facebook
      page_url="http://moffhubsolutions.com/blog"
      title_social="Facebook"
      has_counter
      has_icon
    ></vue-goodshare-facebook>
    <share-whatsapp page_url="http://moffhubsolutions.com/blog" title_social="WhatsApp" has_icon></share-whatsapp>
    <share-twitter page_url="http://moffhubsolutions.com/blog" title_social="Twitter" has_icon></share-twitter>
  </div>
</template>
<script>
import VueGoodshareFacebook from "vue-goodshare/src/providers/Facebook.vue";
import ShareWhatsapp from "vue-goodshare/src/providers/WhatsApp.vue";
import ShareTwitter from "vue-goodshare/src/providers/Twitter.vue";
export default {
  components: {
    VueGoodshareFacebook,
    ShareWhatsapp,
    ShareTwitter
  },
  name: "shareTo"
};
</script>