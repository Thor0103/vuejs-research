<template>
  <FontAwesomeIcon :icon="[type, Icon.iconName]" />
</template>

<script>
import { library } from "@fortawesome/fontawesome-svg-core";
import { fas } from "@fortawesome/free-solid-svg-icons";
import { far } from "@fortawesome/free-regular-svg-icons";
import { fab } from "@fortawesome/free-brands-svg-icons";
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";

const Icons = {
  fas,
  far,
  fab,
};

library.add(fas, fab, far);

export default {
  name: "Icon",
  props: {
    keyName: {
      type: String,
      required: true,
    },
    type: {
      type: String,
      required: true,
    },
  },
  components: {
    FontAwesomeIcon,
  },
  data() {
    return {
      Icon: Icons[this.type][this.keyName],
    };
  },
};
</script>

<style scoped></style>
