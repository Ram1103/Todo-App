<script>
    let todo = '';
    import { addTodo } from "../stores/todoStore.js";

    const handleSubmit = () => {
        addTodo(todo);
        todo = '';
        console.log("submitting")
    }
</script>
<form class="my-6" on:submit|preventDefault={handleSubmit}>
    <div class="flex flex-col text-sm mb-2">
        <label class="font-bold mb-2 text-gray-800" for="todo"></label>
        <input type="text" bind:value={todo} name="todo" placeholder="Whatchya gotta do?" class="apperance-none shadow-sm border border-gray-200 p-2 focus:outline-none
        focus:border-gray-500 rounded-lg py-2 px-4">
    </div>
    <button type="submit" class="w-full shadow-md rounded bg-black hover:bg-blue-600 text-white py-2 px-4 ">
        Submit</button>
</form>

<!-- <button class="w-full relative inline-flex items-center justify-center p-0.5 mb-2 mr-2 overflow-hidden text-sm font-medium text-gray-900 rounded-lg group bg-gradient-to-br from-cyan-500 to-blue-500 group-hover:from-cyan-500 group-hover:to-blue-500 hover:text-white dark:text-white focus:ring-4 focus:outline-none focus:ring-cyan-200 dark:focus:ring-cyan-800">
    <span class="w-full relative px-5 py-2.5 transition-all ease-in duration-75 bg-white dark:bg-gray-900 rounded-md group-hover:bg-opacity-0">
        Cyan to blue
    </span>
  </button> -->