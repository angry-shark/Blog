<script>
var AV = require("leancloud-storage");
var { Query, User } = AV;

var APP_ID = "arir6CG0gfz2098HXVMSGCgI-gzGzoHsz";
var APP_KEY = "4g4PPvnFjKOVtKUtFTD9ON93";

AV.init({
  appId: APP_ID,
  appKey: APP_KEY
});
export default {
  AV,
}
</script>