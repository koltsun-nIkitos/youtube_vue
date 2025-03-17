<template>
  <aside
    class="no-scrollbar hidden xl:block w-64 max-h-screen overflow-auto fixed top-0 pt-12 bg-white z-20"
  >
    <section class="py-2 border-b">
      <ul>
        <li>
          <a
            href="#"
            class="flex items-center px-6 py-2 text-sm font-medium text-gray-800 bg-gray-200 hover:bg-gray-300"
          >
            <svg
              class="2-6 h-6 mr-6"
              viewBox="0 0 24 24"
              fill="rgba(220, 38, 38, 1)"
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
            <span class="">Home</span>
          </a>
        </li>
        <li>
          <a
            href="#"
            class="flex items-center px-6 py-2 text-sm hover:bg-gray-100"
          >
            <svg
              class="2-6 h-6 mr-6"
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
            <span class="">Trending</span>
          </a>
        </li>
        <li>
          <a
            href="#"
            class="flex items-center px-6 py-2 text-sm hover:bg-gray-100"
          >
            <svg
              class="w-6 h-6 mr-6"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 24 24"
              fill="currentColor"
            >
              <path
                d="M5.566 4.657A4.505 4.505 0 0 1 6.75 4.5h10.5c.41 0 .806.055 1.183.157A3 3 0 0 0 15.75 3h-7.5a3 3 0 0 0-2.684 1.657ZM2.25 12a3 3 0 0 1 3-3h13.5a3 3 0 0 1 3 3v6a3 3 0 0 1-3 3H5.25a3 3 0 0 1-3-3v-6ZM5.25 7.5c-.41 0-.806.055-1.184.157A3 3 0 0 1 6.75 6h10.5a3 3 0 0 1 2.683 1.657A4.505 4.505 0 0 0 18.75 7.5H5.25Z"
              />
            </svg>

            <span class="">Subscriptions</span>
          </a>
        </li>
      </ul>
    </section>

    <section class="py-2 border-b">
      <ul>
        <li>
          <a
            href="#"
            class="flex items-center px-6 py-2 text-sm hover:bg-gray-100"
          >
            <svg
              class="w-6 h-6 mr-6"
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
            <span class="">Library</span>
          </a>
        </li>
        <li>
          <a
            href="#"
            class="flex items-center px-6 py-2 text-sm hover:bg-gray-100"
          >
            <svg
              class="w-6 h-6 mr-6"
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

            <span class="">History</span>
          </a>
        </li>
      </ul>
    </section>

    <section class="px-8 py-4 border-b font-medium leading-5">
      <span class="text-sm"
        >Sign in to like videos, comment, and subscribe</span
      >

      <button
        class="focus:outline-none flex items-center px-2 py-0.5 mt-3 text-sm text-blue-700 uppercase border border-blue-700 rounded-sm"
      >
        <svg
          class="mr-2 w-7 h-7"
          width="800px"
          height="800px"
          viewBox="0 0 24 24"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            fill-rule="evenodd"
            fill="rgb(29,78,216)"
            clip-rule="evenodd"
            d="M22 12C22 17.5228 17.5228 22 12 22C6.47715 22 2 17.5228 2 12C2 6.47715 6.47715 2 12 2C17.5228 2 22 6.47715 22 12ZM15 9C15 10.6569 13.6569 12 12 12C10.3431 12 9 10.6569 9 9C9 7.34315 10.3431 6 12 6C13.6569 6 15 7.34315 15 9ZM12 20.5C13.784 20.5 15.4397 19.9504 16.8069 19.0112C17.4108 18.5964 17.6688 17.8062 17.3178 17.1632C16.59 15.8303 15.0902 15 11.9999 15C8.90969 15 7.40997 15.8302 6.68214 17.1632C6.33105 17.8062 6.5891 18.5963 7.19296 19.0111C8.56018 19.9503 10.2159 20.5 12 20.5Z"
          />
        </svg>
        Sign In
      </button>
    </section>

    <section class="py-2 border-b">
      <div class="uppercase text-sm font-semibold px-6 py-2">
        best of YouTube
      </div>
      <ul>
        <li>
          <a
            href="#"
            class="flex items-center px-6 py-2 text-sm hover:bg-gray-100"
          >
            <div class="p-1 mr-6 bg-gray-700 rounded-full">
              <svg
                class="w-4 h-4 text-white"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 20 20"
                fill="currentColor"
              >
                <path
                  d="M18 3a1 1 0 00-1.196-.98l-10 2A1 1 0 006 5v9.114A4.369 4.369 0 005 14c-1.657 0-3 .895-3 2s1.343 2 3 2 3-.895 3-2V7.82l8-1.6v5.894A4.37 4.37 0 0015 12c-1.657 0-3 .895-3 2s1.343 2 3 2 3-.895 3-2V3z"
                />
              </svg>
            </div>

            <span class="">Music</span>
          </a>
        </li>
        <li>
          <a
            href="#"
            class="flex items-center px-6 py-2 text-sm hover:bg-gray-100"
          >
            <div class="p-1 mr-6 bg-gray-700 rounded-full">
              <svg
                class="w-4 h-4 text-white"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 20 20"
                fill="currentColor"
              >
                <path
                  fill-rule="evenodd"
                  d="M18 3a1 1 0 00-1.447-.894L8.763 6H5a3 3 0 000 6h.28l1.771 5.316A1 1 0 008 18h1a1 1 0 001-1v-4.382l6.553 3.276A1 1 0 0018 15V3z"
                  clip-rule="evenodd"
                />
              </svg>
            </div>

            <span class="">Sports</span>
          </a>
        </li>
        <li>
          <a
            href="#"
            class="flex items-center px-6 py-2 text-sm hover:bg-gray-100"
          >
            <div class="p-1 mr-6 bg-gray-700 rounded-full">
              <svg
                class="w-4 h-4 text-white"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 20 20"
                fill="currentColor"
              >
                <path
                  d="M10 3.5a1.5 1.5 0 013 0V4a1 1 0 001 1h3a1 1 0 011 1v3a1 1 0 01-1 1h-.5a1.5 1.5 0 000 3h.5a1 1 0 011 1v3a1 1 0 01-1 1h-3a1 1 0 01-1-1v-.5a1.5 1.5 0 00-3 0v.5a1 1 0 01-1 1H6a1 1 0 01-1-1v-3a1 1 0 00-1-1h-.5a1.5 1.5 0 010-3H4a1 1 0 001-1V6a1 1 0 011-1h3a1 1 0 001-1v-.5z"
                />
              </svg>
            </div>

            <span class="">Gaming</span>
          </a>
        </li>
        <li>
          <a
            href="#"
            class="flex items-center px-6 py-2 text-sm hover:bg-gray-100"
          >
            <div class="p-1 mr-6 bg-gray-700 rounded-full">
              <svg
                class="w-4 h-4 text-white"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 20 20"
                fill="currentColor"
              >
                <path
                  fill-rule="evenodd"
                  d="M4 3a2 2 0 00-2 2v10a2 2 0 002 2h12a2 2 0 002-2V5a2 2 0 00-2-2H4zm3 2h6v4H7V5zm8 8v2h1v-2h-1zm-2-2H7v4h6v-4zm2 0h1V9h-1v2zm1-4V5h-1v2h1zM5 5v2H4V5h1zm0 4H4v2h1V9zm-1 4h1v2H4v-2z"
                  clip-rule="evenodd"
                />
              </svg>
            </div>

            <span class="">Movies</span>
          </a>
        </li>
        <li>
          <a
            href="#"
            class="flex items-center px-6 py-2 text-sm hover:bg-gray-100"
          >
            <div class="p-1 mr-6 bg-gray-700 rounded-full">
              <svg
                class="w-4 h-4 text-white"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 20 20"
                fill="currentColor"
              >
                <path
                  fill-rule="evenodd"
                  d="M2 5a2 2 0 012-2h8a2 2 0 012 2v10a2 2 0 002 2H4a2 2 0 01-2-2V5zm3 1h6v4H5V6zm6 6H5v2h6v-2z"
                  clip-rule="evenodd"
                />
                <path d="M15 7h1a2 2 0 012 2v5.5a1.5 1.5 0 01-3 0V7z" />
              </svg>
            </div>

            <span class="">News</span>
          </a>
        </li>
        <li>
          <a
            href="#"
            class="flex items-center px-6 py-2 text-sm hover:bg-gray-100"
          >
            <div class="p-1 mr-6 bg-gray-700 rounded-full">
              <svg
                class="w-4 h-4 text-white"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 20 20"
                fill="currentColor"
              >
                <path
                  fill-rule="evenodd"
                  d="M5.05 3.636a1 1 0 010 1.414 7 7 0 000 9.9 1 1 0 11-1.414 1.414 9 9 0 010-12.728 1 1 0 011.414 0zm9.9 0a1 1 0 011.414 0 9 9 0 010 12.728 1 1 0 11-1.414-1.414 7 7 0 000-9.9 1 1 0 010-1.414zM7.879 6.464a1 1 0 010 1.414 3 3 0 000 4.243 1 1 0 11-1.415 1.414 5 5 0 010-7.07 1 1 0 011.415 0zm4.242 0a1 1 0 011.415 0 5 5 0 010 7.072 1 1 0 01-1.415-1.415 3 3 0 000-4.242 1 1 0 010-1.415zM10 9a1 1 0 011 1v.01a1 1 0 11-2 0V10a1 1 0 011-1z"
                  clip-rule="evenodd"
                />
              </svg>
            </div>

            <span class="">Live</span>
          </a>
        </li>
        <li>
          <a
            href="#"
            class="flex items-center px-6 py-2 text-sm hover:bg-gray-100"
          >
            <div class="p-1 mr-6 bg-gray-700 rounded-full">
              <svg
                class="w-4 h-4 text-white"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 20 20"
                fill="currentColor"
              >
                <path d="M10 12a2 2 0 100-4 2 2 0 000 4z" />
                <path
                  fill-rule="evenodd"
                  d="M.458 10C1.732 5.943 5.522 3 10 3s8.268 2.943 9.542 7c-1.274 4.057-5.064 7-9.542 7S1.732 14.057.458 10zM14 10a4 4 0 11-8 0 4 4 0 018 0z"
                  clip-rule="evenodd"
                />
              </svg>
            </div>

            <span class="">360&deg; Video</span>
          </a>
        </li>
      </ul>
    </section>

    <section class="py-2 border-b">
      <ul>
        <li>
          <a
            href="#"
            class="flex items-center px-6 py-2 text-sm hover:bg-gray-100"
          >
            <svg
              class="w-6 h-6 mr-6"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 20 20"
              fill="currentColor"
            >
              <path
                fill-rule="evenodd"
                d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-11a1 1 0 10-2 0v2H7a1 1 0 100 2h2v2a1 1 0 102 0v-2h2a1 1 0 100-2h-2V7z"
                clip-rule="evenodd"
              />
            </svg>
            <span class="">Browse channels</span>
          </a>
        </li>
      </ul>
    </section>

    <section class="py-2 border-b">
      <div class="uppercase text-sm font-semibold px-6 py-2">
        more from youtube
      </div>
      <ul>
        <li>
          <a
            href="#"
            class="flex items-center px-6 py-2 text-sm hover:bg-gray-100"
          >
            <svg
              class="w-6 h-6 mr-6"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 20 20"
              fill="currentColor"
            >
              <path
                fill-rule="evenodd"
                d="M10 18a8 8 0 100-16 8 8 0 000 16zM9.555 7.168A1 1 0 008 8v4a1 1 0 001.555.832l3-2a1 1 0 000-1.664l-3-2z"
                clip-rule="evenodd"
              />
            </svg>

            <span class="">YouTube Premium</span>
          </a>
        </li>
        <li>
          <a
            href="#"
            class="flex items-center px-6 py-2 text-sm hover:bg-gray-100"
          >
            <svg
              class="w-6 h-6 mr-6"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 20 20"
              fill="currentColor"
            >
              <path
                fill-rule="evenodd"
                d="M5.05 3.636a1 1 0 010 1.414 7 7 0 000 9.9 1 1 0 11-1.414 1.414 9 9 0 010-12.728 1 1 0 011.414 0zm9.9 0a1 1 0 011.414 0 9 9 0 010 12.728 1 1 0 11-1.414-1.414 7 7 0 000-9.9 1 1 0 010-1.414zM7.879 6.464a1 1 0 010 1.414 3 3 0 000 4.243 1 1 0 11-1.415 1.414 5 5 0 010-7.07 1 1 0 011.415 0zm4.242 0a1 1 0 011.415 0 5 5 0 010 7.072 1 1 0 01-1.415-1.415 3 3 0 000-4.242 1 1 0 010-1.415zM10 9a1 1 0 011 1v.01a1 1 0 11-2 0V10a1 1 0 011-1z"
                clip-rule="evenodd"
              />
            </svg>

            <span class="">Live</span>
          </a>
        </li>
      </ul>
    </section>

    <section class="py-2 border-b">
      <ul>
        <li>
          <a
            href="#"
            class="flex items-center px-6 py-2 text-sm hover:bg-gray-100"
          >
            <svg
              class="2-6 h-6 mr-6"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 20 20"
              fill="currentColor"
            >
              <path
                fill-rule="evenodd"
                d="M11.49 3.17c-.38-1.56-2.6-1.56-2.98 0a1.532 1.532 0 01-2.286.948c-1.372-.836-2.942.734-2.106 2.106.54.886.061 2.042-.947 2.287-1.561.379-1.561 2.6 0 2.978a1.532 1.532 0 01.947 2.287c-.836 1.372.734 2.942 2.106 2.106a1.532 1.532 0 012.287.947c.379 1.561 2.6 1.561 2.978 0a1.533 1.533 0 012.287-.947c1.372.836 2.942-.734 2.106-2.106a1.533 1.533 0 01.947-2.287c1.561-.379 1.561-2.6 0-2.978a1.532 1.532 0 01-.947-2.287c.836-1.372-.734-2.942-2.106-2.106a1.532 1.532 0 01-2.287-.947zM10 13a3 3 0 100-6 3 3 0 000 6z"
                clip-rule="evenodd"
              />
            </svg>
            <span class="">Settings</span>
          </a>
        </li>
        <li>
          <a
            href="#"
            class="flex items-center px-6 py-2 text-sm hover:bg-gray-100"
          >
            <svg
              class="2-6 h-6 mr-6"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 20 20"
              fill="currentColor"
            >
              <path
                fill-rule="evenodd"
                d="M3 6a3 3 0 013-3h10a1 1 0 01.8 1.6L14.25 8l2.55 3.4A1 1 0 0116 13H6a1 1 0 00-1 1v3a1 1 0 11-2 0V6z"
                clip-rule="evenodd"
              />
            </svg>
            <span class="">Report history</span>
          </a>
        </li>
        <li>
          <a
            href="#"
            class="flex items-center px-6 py-2 text-sm hover:bg-gray-100"
          >
            <svg
              class="2-6 h-6 mr-6"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 20 20"
              fill="currentColor"
            >
              <path
                fill-rule="evenodd"
                d="M18 10a8 8 0 11-16 0 8 8 0 0116 0zm-8-3a1 1 0 00-.867.5 1 1 0 11-1.731-1A3 3 0 0113 8a3.001 3.001 0 01-2 2.83V11a1 1 0 11-2 0v-1a1 1 0 011-1 1 1 0 100-2zm0 8a1 1 0 100-2 1 1 0 000 2z"
                clip-rule="evenodd"
              />
            </svg>
            <span class="">Help</span>
          </a>
        </li>
        <li>
          <a
            href="#"
            class="flex items-center px-6 py-2 text-sm hover:bg-gray-100"
          >
            <svg
              class="2-6 h-6 mr-6"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 20 20"
              fill="currentColor"
            >
              <path
                fill-rule="evenodd"
                d="M18 13V5a2 2 0 00-2-2H4a2 2 0 00-2 2v8a2 2 0 002 2h3l3 3 3-3h3a2 2 0 002-2zM5 7a1 1 0 011-1h8a1 1 0 110 2H6a1 1 0 01-1-1zm1 3a1 1 0 100 2h3a1 1 0 100-2H6z"
                clip-rule="evenodd"
              />
            </svg>
            <span class="">Send feedback</span>
          </a>
        </li>
      </ul>
    </section>

    <section class="px-6 py-4 text-xs font-semibold space-y-4">
      <div>
        <a href="#" class="mr-2">About</a>
        <a href="#" class="mr-2">Press</a>
        <a href="#" class="mr-2">Copyright</a>
        <a href="#" class="mr-2">Contact us</a>
        <a href="#" class="mr-2">Creators</a>
        <a href="#" class="mr-2">Advertise</a>
        <a href="#" class="mr-2">Developers</a>
      </div>
      <div>
        <a href="#" class="mr-2">Terms</a>
        <a href="#" class="mr-2">Privacy</a>
        <a href="#" class="mr-2">Policy & Safety</a>
        <a href="#" class="mr-2">How YouTube works</a>
        <a href="#" class="mr-2">Test new features</a>
      </div>
      <div class="font-normal text-gray-500">&copy; 2025 Google LLC</div>
    </section>
  </aside>
</template>
