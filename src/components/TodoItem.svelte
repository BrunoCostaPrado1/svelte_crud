<script>
  export let index;
  export let todo;
  export let editTodo;
  export let removeTodo;
</script>

<div class="todo">
  <p>
    {index + 1} - {todo}
  </p>
  <div class="actions">
    <button
      on:click={() => {
        editTodo(index);
      }}>edit</button
    >
    <button
      on:click={() => {
        removeTodo(index);
      }}>remove</button
    >
  </div>
</div>

<style>
  .todo {
    border-left: 1px solid cyan;
    padding: 8px 14px;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  .actions {
    display: flex;
    align-items: center;
    gap: 8px;
    font-size: 1.3rem;
  }
  .actions button {
    color: coral;
  }
</style>
