<template>
  <div>
    <button
      type="button"
      class="btn btn-primary"
      data-toggle="modal"
      data-target="#modalAccepted"
    >
      Xác nhận
    </button>
    <div
      class="modal fade"
      id="modalAccepted"
      tabindex="-1"
      role="dialog"
      aria-labelledby="modalAcceptedLabel"
      aria-hidden="true"
    >
      <div class="modal-dialog modal-dialog-centered" role="document">
        <div class="modal-content">
          <div class="modal-body">
            <span class="material-symbols-outlined"> check_circle </span>
            <div class="model-content">Đã duyệt đơn thành công!</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "modal-content",
};
</script>

<style></style>
