<template>
  <div>
    <div class="flex w-full justify-between items-center">
      <Breadcrumb breadcrumb="" />
      <!--Banner get you to github repo-->
      <Banner />
      <div class="flex justify-end">
        <button
          @click="updateStocks"
          class="flex items-center justify-between bg-indigo-600 px-6 shadow-xl py-2 border font-semibold text-md text-white rounded-tr-3xl rounded-bl-3xl hover:bg-indigo-700"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            class="w-6 h-6 mr-4"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M16.023 9.348h4.992v-.001M2.985 19.644v-4.992m0 0h4.992m-4.993 0l3.181 3.183a8.25 8.25 0 0013.803-3.7M4.031 9.865a8.25 8.25 0 0113.803-3.7l3.181 3.182m0-4.991v4.99"
            />
          </svg>

          Update Stocks
        </button>
      </div>
    </div>
    <!-- <div class="mt-4">
      <div class="flex flex-wrap -mx-6">
        <div class="w-full px-6 sm:w-1/2 xl:w-1/3">
          <div
            class="flex items-center px-5 py-6 bg-white rounded-md shadow-sm"
          >
            <div class="p-3 bg-indigo-600 bg-opacity-75 rounded-full">
              <svg
                class="w-8 h-8 text-white"
                viewBox="0 0 28 30"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M18.2 9.08889C18.2 11.5373 16.3196 13.5222 14 13.5222C11.6804 13.5222 9.79999 11.5373 9.79999 9.08889C9.79999 6.64043 11.6804 4.65556 14 4.65556C16.3196 4.65556 18.2 6.64043 18.2 9.08889Z"
                  fill="currentColor"
                />
                <path
                  d="M25.2 12.0444C25.2 13.6768 23.9464 15 22.4 15C20.8536 15 19.6 13.6768 19.6 12.0444C19.6 10.4121 20.8536 9.08889 22.4 9.08889C23.9464 9.08889 25.2 10.4121 25.2 12.0444Z"
                  fill="currentColor"
                />
                <path
                  d="M19.6 22.3889C19.6 19.1243 17.0927 16.4778 14 16.4778C10.9072 16.4778 8.39999 19.1243 8.39999 22.3889V26.8222H19.6V22.3889Z"
                  fill="currentColor"
                />
                <path
                  d="M8.39999 12.0444C8.39999 13.6768 7.14639 15 5.59999 15C4.05359 15 2.79999 13.6768 2.79999 12.0444C2.79999 10.4121 4.05359 9.08889 5.59999 9.08889C7.14639 9.08889 8.39999 10.4121 8.39999 12.0444Z"
                  fill="currentColor"
                />
                <path
                  d="M22.4 26.8222V22.3889C22.4 20.8312 22.0195 19.3671 21.351 18.0949C21.6863 18.0039 22.0378 17.9556 22.4 17.9556C24.7197 17.9556 26.6 19.9404 26.6 22.3889V26.8222H22.4Z"
                  fill="currentColor"
                />
                <path
                  d="M6.64896 18.0949C5.98058 19.3671 5.59999 20.8312 5.59999 22.3889V26.8222H1.39999V22.3889C1.39999 19.9404 3.2804 17.9556 5.59999 17.9556C5.96219 17.9556 6.31367 18.0039 6.64896 18.0949Z"
                  fill="currentColor"
                />
              </svg>
            </div>

            <div class="mx-5">
              <h4 class="text-2xl font-semibold text-gray-700">8,282</h4>
              <div class="text-gray-500">New Users</div>
            </div>
          </div>
        </div>

        <div class="w-full px-6 mt-6 sm:w-1/2 xl:w-1/3 sm:mt-0">
          <div
            class="flex items-center px-5 py-6 bg-white rounded-md shadow-sm"
          >
            <div class="p-3 bg-blue-600 bg-opacity-75 rounded-full">
              <svg
                class="w-8 h-8 text-white"
                viewBox="0 0 28 28"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M4.19999 1.4C3.4268 1.4 2.79999 2.02681 2.79999 2.8C2.79999 3.57319 3.4268 4.2 4.19999 4.2H5.9069L6.33468 5.91114C6.33917 5.93092 6.34409 5.95055 6.34941 5.97001L8.24953 13.5705L6.99992 14.8201C5.23602 16.584 6.48528 19.6 8.97981 19.6H21C21.7731 19.6 22.4 18.9732 22.4 18.2C22.4 17.4268 21.7731 16.8 21 16.8H8.97983L10.3798 15.4H19.6C20.1303 15.4 20.615 15.1004 20.8521 14.6261L25.0521 6.22609C25.2691 5.79212 25.246 5.27673 24.991 4.86398C24.7357 4.45123 24.2852 4.2 23.8 4.2H8.79308L8.35818 2.46044C8.20238 1.83722 7.64241 1.4 6.99999 1.4H4.19999Z"
                  fill="currentColor"
                />
                <path
                  d="M22.4 23.1C22.4 24.2598 21.4598 25.2 20.3 25.2C19.1403 25.2 18.2 24.2598 18.2 23.1C18.2 21.9402 19.1403 21 20.3 21C21.4598 21 22.4 21.9402 22.4 23.1Z"
                  fill="currentColor"
                />
                <path
                  d="M9.1 25.2C10.2598 25.2 11.2 24.2598 11.2 23.1C11.2 21.9402 10.2598 21 9.1 21C7.9402 21 7 21.9402 7 23.1C7 24.2598 7.9402 25.2 9.1 25.2Z"
                  fill="currentColor"
                />
              </svg>
            </div>

            <div class="mx-5">
              <h4 class="text-2xl font-semibold text-gray-700">200,521</h4>
              <div class="text-gray-500">Total Orders</div>
            </div>
          </div>
        </div>

        <div class="w-full px-6 mt-6 sm:w-1/2 xl:w-1/3 xl:mt-0">
          <div
            class="flex items-center px-5 py-6 bg-white rounded-md shadow-sm"
          >
            <div class="p-3 bg-pink-600 bg-opacity-75 rounded-full">
              <svg
                class="w-8 h-8 text-white"
                viewBox="0 0 28 28"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M6.99998 11.2H21L22.4 23.8H5.59998L6.99998 11.2Z"
                  fill="currentColor"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linejoin="round"
                />
                <path
                  d="M9.79999 8.4C9.79999 6.08041 11.6804 4.2 14 4.2C16.3196 4.2 18.2 6.08041 18.2 8.4V12.6C18.2 14.9197 16.3196 16.8 14 16.8C11.6804 16.8 9.79999 14.9197 9.79999 12.6V8.4Z"
                  stroke="currentColor"
                  stroke-width="2"
                />
              </svg>
            </div>

            <div class="mx-5">
              <h4 class="text-2xl font-semibold text-gray-700">215,542</h4>
              <div class="text-gray-500">Available Products</div>
            </div>
          </div>
        </div>
      </div>
    </div> -->

    <div class="mt-8"></div>
    
    <div class="flex flex-col mt-8">
      <div class="py-2 -my-2 overflow-x-auto sm:-mx-6 sm:px-6 lg:-mx-8 lg:px-8">
        <div
          class="inline-block min-w-full overflow-hidden align-middle border-b border-gray-200 shadow sm:rounded-lg"
        >
          <table class="min-w-full">
            <thead>
              <tr>
                <th
                  class="px-6 py-3 text-xs font-medium leading-4 tracking-wider text-left text-gray-500 uppercase border-b border-gray-200 bg-gray-50"
                >
                  Date
                </th>
                <th
                  class="px-6 py-3 text-xs font-medium leading-4 tracking-wider text-left text-gray-500 uppercase border-b border-gray-200 bg-gray-50"
                >
                  Item
                </th>
                <th
                  class="px-6 py-3 text-xs font-medium leading-4 tracking-wider text-left text-gray-500 uppercase border-b border-gray-200 bg-gray-50"
                >
                  Action
                </th>
                <th
                  class="px-6 py-3 text-xs font-medium leading-4 tracking-wider text-left text-gray-500 uppercase border-b border-gray-200 bg-gray-50"
                >
                  Stock
                </th>
                <th
                  class="px-6 py-3 text-xs font-medium leading-4 tracking-wider text-left text-gray-500 uppercase border-b border-gray-200 bg-gray-50"
                >
                  Message
                </th>
                <th
                  class="px-6 py-3 text-xs font-medium leading-4 tracking-wider text-left text-gray-500 uppercase border-b border-gray-200 bg-gray-50"
                >
                  Success
                </th>
                <!-- <th class="px-6 py-3 border-b border-gray-200 bg-gray-50"></th> -->
              </tr>
            </thead>

            <tbody class="bg-white">
              <tr v-for="(log,id) in logs.data" :key="id">
                <td
                  class="px-4 py-2 border-b border-gray-200 whitespace-nowrap"
                >
                  <div class="flex items-center w-full">
                    <div class="text-sm font-medium leading-5 text-gray-900">
                      {{ log.created_at }}
                    </div>
                    <!-- <div class="text-sm leading-5 text-gray-500">
                        {{ u.email }}
                      </div> -->
                  </div>
                </td>

                <td
                  class="px-4 py-2 border-b border-gray-200 whitespace-nowrap"
                >
                  <div class="text-sm leading-5 text-gray-900">
                    {{ log?.data?.sku }}
                  </div>
                  <!-- <div class="text-sm leading-5 text-gray-500">
                    {{ u.title2 }}
                  </div> -->
                </td>

                <td
                  class="px-4 py-2 border-b border-gray-200 whitespace-nowrap"
                >
                  <span
                    class="inline-flex px-4 text-xs font-semibold leading-5 text-green-800 bg-green-100 rounded-full"
                    >
                    {{ log.type }}
                    </span
                  >
                </td>

                <td
                  class="px-4 py-2 text-sm leading-5 text-gray-500 border-b border-gray-200 whitespace-nowrap"
                >
                  {{ log?.data?.stock }}
                </td>
                <td
                  class="px-4 py-2 text-sm leading-5 text-gray-500 border-b border-gray-200 whitespace-nowrap"
                >
                {{ log?.data?.error_message }}

                </td>
                <td
                  class="px-4 py-2 text-sm leading-5 text-gray-500 border-b border-gray-200 whitespace-nowrap"
                >
                {{ log?.success }}

                </td>

                <!-- <td
                  class="
                    px-6
                    py-4
                    text-sm
                    font-medium
                    leading-5
                    text-right
                    border-b border-gray-200
                    whitespace-nowrap
                  "
                >
                  <div class="flex justify-around">
                    <span class="text-yellow-500 flex justify-center">
                      <a href="#" class="mx-2 px-2 rounded-md"
                        ><svg
                          xmlns="http://www.w3.org/2000/svg"
                          class="h-5 w-5 text-green-700"
                          viewBox="0 0 20 20"
                          fill="currentColor"
                        >
                          <path
                            d="M17.414 2.586a2 2 0 00-2.828 0L7 10.172V13h2.828l7.586-7.586a2 2 0 000-2.828z"
                          />
                          <path
                            fill-rule="evenodd"
                            d="M2 6a2 2 0 012-2h4a1 1 0 010 2H4v10h10v-4a1 1 0 112 0v4a2 2 0 01-2 2H4a2 2 0 01-2-2V6z"
                            clip-rule="evenodd"
                          />
                        </svg>
                      </a>
                      <form method="POST">
                        <button class="mx-2 px-2 rounded-md">
                          <svg
                            xmlns="http://www.w3.org/2000/svg"
                            class="h-5 w-5 text-red-700"
                            viewBox="0 0 20 20"
                            fill="currentColor"
                          >
                            <path
                              fill-rule="evenodd"
                              d="M9 2a1 1 0 00-.894.553L7.382 4H4a1 1 0 000 2v10a2 2 0 002 2h8a2 2 0 002-2V6a1 1 0 100-2h-3.382l-.724-1.447A1 1 0 0011 2H9zM7 8a1 1 0 012 0v6a1 1 0 11-2 0V8zm5-1a1 1 0 00-1 1v6a1 1 0 102 0V8a1 1 0 00-1-1z"
                              clip-rule="evenodd"
                            />
                          </svg>
                        </button>
                      </form>
                    </span>
                  </div>
                </td> -->
              </tr>
            </tbody>
          </table>
        </div>
      </div>
      <div class="flex justify-end align-middle mt-3 pr-3">{{ logs?.pagination.total }}
      <div
        class="pagination inline-flex items-center justify-center rounded bg-blue-600 py-1 text-white"
      >
        <a
        @click="fetchLogs(page > 1 ? page-- : page)"
          href="#"
          class="inline-flex h-8 w-8 items-center justify-center rtl:rotate-180"
        >
          <span class="sr-only">Prev Page</span>
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-3 w-3"
            viewBox="0 0 20 20"
            fill="currentColor"
          >
            <path
              fill-rule="evenodd"
              d="M12.707 5.293a1 1 0 010 1.414L9.414 10l3.293 3.293a1 1 0 01-1.414 1.414l-4-4a1 1 0 010-1.414l4-4a1 1 0 011.414 0z"
              clip-rule="evenodd"
            />
          </svg>
        </a>

        <!-- <span class="h-4 w-px bg-white/25" aria-hidden="true"></span> -->

        <!-- <div>
          <label for="PaginationPage" class="sr-only">Page</label>

          <span
            class="h-8 w-12 rounded border-none bg-transparent p-0 text-center text-md font-medium [-moz-appearance:_textfield] focus:outline-none focus:ring-inset focus:ring-white [&::-webkit-inner-spin-button]:m-0 [&::-webkit-inner-spin-button]:appearance-none [&::-webkit-outer-spin-button]:m-0 [&::-webkit-outer-spin-button]:appearance-none"
            
            id="PaginationPage">
          {{page}}
          </span>
          
        </div> -->

        <span class="h-4 w-px bg-white/25"></span>

        <a
          @click="fetchLogs(page++)"
          href="#"
          class="inline-flex h-8 w-8 items-center justify-center rtl:rotate-180"
        >
          <span class="sr-only">Next Page</span>
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-3 w-3"
            viewBox="0 0 20 20"
            fill="currentColor"
          >
            <path
              fill-rule="evenodd"
              d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z"
              clip-rule="evenodd"
            />
          </svg>
        </a>
      </div>

      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted, reactive } from "vue";
import Banner from "../partials/Banner.vue";
import Breadcrumb from "../partials/Breadcrumb.vue";
import { useRouter } from "vue-router";
const router = useRouter();

// interface User {
//   name: string;
//   email: string;
//   title: string;
//   title2: string;
//   status: string;
//   role: string;
// }

// const testUser: User = {
//   name: "John Doe",
//   email: "john@example.com",
//   title: "Software Engineer",
//   title2: "Web dev",
//   status: "Active",
//   role: "Owner",
// };

// const users = ref<User[]>([...Array(10).keys()].map(() => testUser));

interface Log {
  id: string,
  type: string
  data: {
    sku: string,
    stock: number,
    sellable_id: number,
    product_id: number,
    product_title: string,
    sellable_title: string,
    sellable_full_title: string,
    error_message: string
  },
  success: boolean,
  created_at: string,
}
interface Logs {
  data: [Log],
  success: boolean,
  pagination: {
    total: number
  }
}
const logs: Logs = reactive({
  data: [
    {
      "id": "",
      "type": "",
      "data": {
        "sku": "",
        "stock": 0,
        "sellable_id": 0,
        "product_id": 0,
        "product_title": "",
        "sellable_title": "",
        "sellable_full_title": "",
        "error_message": ""
      },
      "success": false,
      "created_at": "2000-01-01T00:00:00.000000Z"
    }
  ],
  success: false,
  pagination: {
    total: 0
  }
})

const page = 1;

onMounted(() => {
  fetchLogs(page);
  // setInterval(() => {fetchLogs(page);}, 3000)
})

async function fetchLogs(page: number): Promise<void> {
  const API_URL = process.env.VUE_APP_API_URL;

  const token = localStorage.getItem("token");

  const url = API_URL + "/logs" + "?page=" + page + "&limit=20";
  const options = {
    method: "GET",
    headers: {
      "Accept": "application/json",
      "Content-Type": "application/json;charset=UTF-8",
      "Authorization": "Bearer " + token
    },
  };

  fetch(url, options)
  .then((response) => response.json())
  .then((data) => {
    // console.log('data fetch: ', data);
    logs.data = data?.data;
    logs.success = data?.success;
    logs.pagination = data?.pagination
  })
}

async function updateStocks(): Promise<void> {
  // console.log("stocks page opened.");
  router.push("/stocks");
}

// http://sirri.fthyuksel.com/api/v1/logs/
// Bearer 4|xvuFHl1aVWXeuEE21NiYu5FER0vimuBlvH8eb585
// GET
// {
//   "success": true,
//   "data":[],
//   "pagination":{
//     "total": 0,
//     "perPage": 15,
//     "currentPage": 1,
//     "lastPage": 1,
//     "from": null,
//     "to": null
//   }
// }
</script>
