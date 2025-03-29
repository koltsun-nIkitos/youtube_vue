<template>
  <aside
    :class="classes"
  >
    <section>
      <ul>
        <li>
          <a
            href="#"
            class="flex flex-col items-center px-6 py-5 text-red-500 hover:bg-gray-100"
          >
            <svg
              class="2-6 h-6 mb-1.5"
              viewBox="0 0 24 24"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M6.5 20V11H3L12 5L21 11H17.5V20H14.5V16.5C14.5 15.6716 13.8284 15 13 15H11C10.1716 15 9.5 15.6716 9.5 16.5V20H6.5Z"
                fill="rgba(220, 38, 38, 1)"
                stroke="rgba(220, 38, 38, 1)"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
            </svg>
            <span class="text-xs">Home</span>
          </a>
        </li>
        <li>
          <a
            href="#"
            class="flex flex-col items-center px-6 py-5 hover:bg-gray-100"
          >
            <svg
              class="2-6 h-6 mb-1.5"
              xmlns="http://www.w3.org/2000/svg"
              fill="#4f4f4f"
              viewBox="0 0 24 24"
              stroke-width="1.5"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M15.362 5.214A8.252 8.252 0 0 1 12 21 8.25 8.25 0 0 1 6.038 7.047 8.287 8.287 0 0 0 9 9.601a8.983 8.983 0 0 1 3.361-6.867 8.21 8.21 0 0 0 3 2.48Z"
              />
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M12 18a3.75 3.75 0 0 0 .495-7.468 5.99 5.99 0 0 0-1.925 3.547 5.975 5.975 0 0 1-2.133-1.001A3.75 3.75 0 0 0 12 18Z"
                fill="white"
              />
            </svg>
            <span class="text-xs">Trending</span>
          </a>
        </li>
        <li>
          <a
            href="#"
            class="flex flex-col items-center px-6 py-5 hover:bg-gray-100"
          >
            <svg
              class="w-6 h-6 mb-1.5"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 24 24"
              fill="currentColor"
            >
              <path
                d="M5.566 4.657A4.505 4.505 0 0 1 6.75 4.5h10.5c.41 0 .806.055 1.183.157A3 3 0 0 0 15.75 3h-7.5a3 3 0 0 0-2.684 1.657ZM2.25 12a3 3 0 0 1 3-3h13.5a3 3 0 0 1 3 3v6a3 3 0 0 1-3 3H5.25a3 3 0 0 1-3-3v-6ZM5.25 7.5c-.41 0-.806.055-1.184.157A3 3 0 0 1 6.75 6h10.5a3 3 0 0 1 2.683 1.657A4.505 4.505 0 0 0 18.75 7.5H5.25Z"
              />
            </svg>

            <span class="text-xs">Subscriptions</span>
          </a>
        </li>
        <li>
          <a
            href="#"
            class="flex flex-col items-center px-6 py-5 hover:bg-gray-100"
          >
            <svg
              class="w-6 h-6 mb-1.5"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 24 24"
              fill="currentColor"
            >
              <path
                d="M16.5 6a3 3 0 0 0-3-3H6a3 3 0 0 0-3 3v7.5a3 3 0 0 0 3 3v-6A4.5 4.5 0 0 1 10.5 6h6Z"
              />
              <path
                d="M18 7.5a3 3 0 0 1 3 3V18a3 3 0 0 1-3 3h-7.5a3 3 0 0 1-3-3v-7.5a3 3 0 0 1 3-3H18Z"
              />
            </svg>

            <span class="text-xs">Library</span>
          </a>
        </li>
        <li>
          <a
            href="#"
            class="flex flex-col items-center px-6 py-5 hover:bg-gray-100"
          >
            <svg
              class="w-6 h-6 mb-1.5"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 24 24"
              fill="currentColor"
            >
              <path
                fill-rule="evenodd"
                d="M12 2.25c-5.385 0-9.75 4.365-9.75 9.75s4.365 9.75 9.75 9.75 9.75-4.365 9.75-9.75S17.385 2.25 12 2.25ZM12.75 6a.75.75 0 0 0-1.5 0v6c0 .414.336.75.75.75h4.5a.75.75 0 0 0 0-1.5h-3.75V6Z"
                clip-rule="evenodd"
              />
            </svg>

            <span class="text-xs">History</span>
          </a>
        </li>
      </ul>
    </section>
  </aside>
</template>


<script>
export default{

  computed:{
    classes(){
      return[
        'min-h-screen', 
        'no-scrollbar', 
        'overflow-auto', 
        'fixed ', 
        'top-0',
        'pt-14', 
        'bg-white', 
        'z-20',
      ]
    }
  },
}
</script>