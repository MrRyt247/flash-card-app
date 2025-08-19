<script lang="ts">
    let { data } = $props();
</script>

<div class="card">
   <h2>{ data.question }</h2>
</div>

<style>
.card {
    border-radius: 5px;
    background-color: #eee;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    font-size: 18px;
    color: #333;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    transition: transform 0.2s ease-in-out;
}
</style>