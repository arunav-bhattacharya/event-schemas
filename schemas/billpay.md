---
layout: default
title: Billpay Event Schema
---

# Billpay Event Schema

Below is the schema definition for Billpay events:

<div class="schema-viewer" id="schema-viewer"></div>

<script src="https://cdn.jsdelivr.net/npm/@json-editor/json-editor@latest/dist/jsoneditor.min.js"></script>
<script>
document.addEventListener('DOMContentLoaded', function() {
  fetch('/event-schemas/v1/BillpayEvents.json')
    .then(response => response.json())
    .then(schema => {
      const container = document.getElementById('schema-viewer');
      const options = {
        schema: schema,
        disable_edit_json: true,
        disable_properties: true,
        disable_collapse: false,
        show_errors: "never",
        no_additional_properties: true,
        theme: 'bootstrap4'
      };
      const editor = new JSONEditor(container, options);
    });
});
</script>

<style>
.schema-viewer {
  min-height: 500px;
  border: 1px solid #ddd;
  border-radius: 4px;
  padding: 10px;
  margin: 20px 0;
}
</style>
