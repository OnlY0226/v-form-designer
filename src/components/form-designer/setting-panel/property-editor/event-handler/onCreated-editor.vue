<template>
  <el-form-item label-width="150px" v-if="!optionModel.noCreatedEvent">
    <template #label>
      <div>onCreated</div>
      <div :class="{ redPoint: optionModel.onCreated }"></div>
    </template>
    <el-button
      type="info"
      icon="el-icon-edit"
      plain
      round
      @click="editEventHandler('onCreated', eventParams)"
    >
      {{ $t("designer.setting.addEventHandler") }}</el-button
    >
  </el-form-item>
</template>

<script>
import i18n from "@/utils/i18n";
import eventMixin from "@/components/form-designer/setting-panel/property-editor/event-handler/eventMixin";

export default {
  name: "onCreated-editor",
  mixins: [i18n, eventMixin],
  props: {
    designer: Object,
    selectedWidget: Object,
    optionModel: Object,
  },
  data() {
    return {
      eventParams: [],
    };
  },
};
</script>

<style scoped></style>
