<script>
export default {
  mounted() {
    $("#items").sortable({
      handle: ".dragger-item",
    });
    $(".boton").click(function () {
      $(this).toggleClass("inactivo activo");
      $(this).find(".fa-solid").toggleClass(".fa-thumbs-down fa-thumbs-up")
    });
  },
};
</script>

<template>
  <!-- <ul id="items">
    <li class="flex gap-4 items-center" v-for="i in 5">
      <span class="font-bold text-2xl dragger">X</span>
      <span class="font-bold text-2xl">Bendiciones</span>
    </li>
  </ul> -->

  <div class="bg-black/60 h-screen flex items-center justify-center">
    <div class="bg-white rounded-lg shadow w-full max-w-2xl p-4 grid gap-4">
      <h1 class="font-bold text-xl">Limpieza de departamentos</h1>
      <div class="overflow-x-auto">
        <table class="w-full">
          <thead>
            <tr class="bg-blue-900 rounded text-white text-xs">
              <th class="py-6"></th>
              <th>Orden</th>
              <th class="text-left">Departamento</th>
              <th>Sala</th>
              <th>Cocina</th>
              <th>Habitaciones</th>
              <th>SSHH</th>
              <th>Completado</th>
            </tr>
          </thead>
          <tbody id="items">
            <tr class="item bg-gray-100" v-for="i in 10">
              <td class="pl-4 py-2">
                <button class="dragger-item">
                  <i class="fa-solid fa-grip-vertical"> </i>
                </button>
              </td>
              <td class="text-xs font-bold text-center">{{ i }}</td>
              <td class="text-xs font-bold">A301</td>
              <td>
                <div class="w-full flex justify-center text-xs">
                  <button
                    class="rounded-full w-6 h-6 boton inactivo flex items-center justify-center"
                  >
                    <i class="fa-solid fa-thumbs-down"></i>
                  </button>
                </div>
              </td>

              <td>
                <div class="w-full flex justify-center text-xs">
                  <button
                    class="rounded-full w-6 h-6 boton inactivo flex items-center justify-center"
                  >
                    <i class="fa-solid fa-thumbs-down"></i>
                  </button>
                </div>
              </td>
              <td>
                <div class="w-full flex justify-center text-xs">
                  <button
                    class="rounded-full w-6 h-6 boton inactivo flex items-center justify-center"
                  >
                    <i class="fa-solid fa-thumbs-down"></i>
                  </button>
                </div>
              </td>

              <td>
                <div class="w-full flex justify-center text-xs">
                  <button
                    class="rounded-full w-6 h-6 boton inactivo flex items-center justify-center"
                  >
                    <i class="fa-solid fa-thumbs-down"></i>
                  </button>
                </div>
              </td>
              <td class="bg-gray-200">
                <div class="w-full flex justify-center">
                  <button
                    class="rounded-full w-6 h-6 boton inactivo flex items-center justify-center"
                  >
                    <i class="fa-solid fa-xmark"></i>
                  </button>
                </div>
              </td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</template>

<style scoped>
.inactivo {
  @apply bg-red-200 text-red-600;
}
.activo {
  @apply bg-green-200 text-green-600;
}
</style>
