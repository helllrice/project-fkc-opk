<template>
  <!-- begin:: Body -->
  <div class="page d-flex flex-row flex-column-fluid">
    <!-- begin:: Aside Left -->
    <KTAside
      v-if="asideEnabled"
      :lightLogo="themeLightLogo"
      :darkLogo="themeDarkLogo"
    />
    <!-- end:: Aside Left -->

    <div id="kt_wrapper" class="d-flex flex-column flex-row-fluid wrapper">
      <KTHeader />

      <!-- begin:: Content -->
      <div id="kt_content" class="content d-flex flex-column flex-column-fluid">
        <!-- begin:: Content Body -->
        <div class="post d-flex flex-column-fluid">
          <div
            id="kt_content_container"
            :class="{
              'container-fluid': contentWidthFluid,
              'container-xxl': !contentWidthFluid,
            }"
          >
            <router-view />
          </div>
        </div>

        <div class="table-container" style="padding: 20px">
          <table class="table m-auto table-row-dashed table-borderless table-row-gray-300 gy-2 gx-4 mb-9">
            <thead>
            <tr class="fw-bolder fs-9 border-gray-800 text-gray-800">
              <th>Дата завершения</th>
              <th>Полное название опроса</th>
              <th>Всего задач</th>
              <th>Были начаты</th>
              <th>НЕ были начаты</th>
              <th>Приняты</th>
              <th>На проверке</th>
              <th>Черновики</th>
              <th>На доработке</th>
              <th>Пустые</th>
              <th>Не заполнены</th>
              <th>ID</th>
            </tr>
            </thead>
            <tbody>
            <tr class="fs-9">
              <td>2011/04/25</td>
              <td>Tiger Nixon</td>
              <td>System Architect</td>
              <td>Edinburgh</td>
              <td>61</td>
              <td>$320,800</td>
              <td>134</td>
              <td>134</td>
              <td>134</td>
              <td>134</td>
              <td>134</td>
              <td>134</td>
            </tr>
            <tr class="fs-9">
              <td>2011/07/25</td>
              <td>Garrett Winters</td>
              <td>Accountant</td>
              <td>Tokyo</td>
              <td>63</td>
              <td>$170,750</td>
              <td>134</td>
              <td>134</td>
              <td>134</td>
              <td>134</td>
              <td>134</td>
              <td>134</td>
            </tr>
            </tbody>
          </table>

          <table class=" table table-row-dashed table-row-gray-300 gy-2 gx-4">
            <thead>
            <tr class="fw-bolder fs-9 border-gray-800 text-gray-800">
              <th>Дата завершения</th>
              <th>Полное название опроса</th>
              <th>Всего задач</th>
              <th>Были начаты</th>
              <th>НЕ были начаты</th>
              <th>Приняты</th>
              <th>На проверке</th>
              <th>Черновики</th>
              <th>На доработке</th>
              <th>Пустые</th>
              <th>Не заполнены</th>
              <th>ID</th>
            </tr>
            </thead>
            <tbody>
            <tr class="fs-9">
              <td>2011/04/25</td>
              <td>Tiger Nixon</td>
              <td>System Architect</td>
              <td>Edinburgh</td>
              <td>61</td>
              <td>$320,800</td>
              <td>134</td>
              <td>134</td>
              <td>134</td>
              <td>134</td>
              <td>134</td>
              <td>134</td>
            </tr>
            <tr class="fs-9">
              <td>2011/07/25</td>
              <td>Garrett Winters</td>
              <td>Accountant</td>
              <td>Tokyo</td>
              <td>63</td>
              <td>$170,750</td>
              <td>134</td>
              <td>134</td>
              <td>134</td>
              <td>134</td>
              <td>134</td>
              <td>134</td>
            </tr>
            </tbody>
          </table>
        </div>



        <!-- button -->


        <div class="table-btn">
          <button
            type="button"
            class="btn btn-primary m-3"
            data-bs-toggle="modal"
            data-bs-target="#kt_modal_1"
          >
            Добавить данные в таблицу
          </button>
        </div>

        <div class="modal fade" tabindex="-1" id="kt_modal_1">
          <div class="modal-dialog">
            <div class="modal-content">
              <div class="modal-header">
                <h2 class="modal-title">Введите данные</h2>

                <!--begin::Close-->
                <div
                  class="btn btn-icon btn-sm btn-active-light-primary ms-2"
                  data-bs-dismiss="modal"
                  aria-label="Close"
                >
                  <span class="svg-icon svg-icon-2x"></span>
                </div>
                <!--end::Close-->
              </div>

              <div class="modal-body p-4 d-flex justify-content-center flex-column">
                <input type="text" class="mb-3 form-control form-control-solid" placeholder="Полное название опроса">
                <input type="text" class="mb-3 form-control form-control-solid" placeholder="Дата завершения">
                <input type="text" class="mb-3 form-control form-control-solid" placeholder="ID">
                <input type="text" class="mb-3 form-control form-control-solid" placeholder="Всего задач">
                <input type="text" class="mb-3 form-control form-control-solid" placeholder="НЕ были начаты">
                <input type="text" class="mb-3 form-control form-control-solid" placeholder="Приняты">
                <input type="text" class="mb-3 form-control form-control-solid" placeholder="На проверке">
                <input type="text" class="mb-3 form-control form-control-solid" placeholder="Черновики">
                <input type="text" class="mb-3 form-control form-control-solid" placeholder="На доработке">
                <input type="text" class="mb-3 form-control form-control-solid" placeholder="Пустые">
                <input type="text" class="mb-3 form-control form-control-solid" placeholder="Не заполненытые">
              </div>

              <div class="modal-footer">
                <button
                  type="button"
                  class="btn btn-light"
                  data-bs-dismiss="modal"
                >
                  Закрыть
                </button>
                <button type="button" class="btn btn-primary">
                 Сохранить данные
                </button>
              </div>
            </div>
          </div>
        </div>

        <!-- end:: Content Body -->
      </div>
      <!-- end:: Content -->
      <KTFooter />
    </div>
  </div>
  <!-- end:: Body -->
  <KTScrollTop />
  <KTDrawerMessenger />
  <KTActivivityDrawer />
  <KTCreateApp />
  <KTInviteFriendsModal />

  <KTToolButtons />
  <KTDemosDrawer />
  <KTHelpDrawer />
</template>

<script lang="ts">
import {
  defineComponent,
  onMounted,
  watch,
  nextTick,
  onBeforeMount,
} from "vue";
import { useRoute } from "vue-router";
import KTAside from "@/layouts/main-layout/aside/Aside.vue";
import KTHeader from "@/layouts/main-layout/header/Header.vue";
import KTFooter from "@/layouts/main-layout/footer/Footer.vue";
import KTScrollTop from "@/layouts/main-layout/extras/ScrollTop.vue";
import KTActivivityDrawer from "@/layouts/main-layout/drawers/ActivityDrawer.vue";
import KTCreateApp from "@/components/modals/wizards/create-app-modal/CreateAppModal.vue";
import KTInviteFriendsModal from "@/components/modals/general/InviteFriendsModal.vue";
import KTDemosDrawer from "@/layouts/main-layout/extras/DemosDrawer.vue";
import KTHelpDrawer from "@/layouts/main-layout/extras/HelpDrawer.vue";
import KTDrawerMessenger from "@/layouts/main-layout/extras/MessengerDrawer.vue";
import { reinitializeComponents } from "@/core/plugins/keenthemes";
import {
  toolbarDisplay,
  loaderEnabled,
  contentWidthFluid,
  loaderLogo,
  asideEnabled,
  subheaderDisplay,
  themeLightLogo,
  themeDarkLogo,
} from "@/core/helpers/config";
import LayoutService from "@/core/services/LayoutService";

export default defineComponent({
  name: "master-layout",
  components: {
    KTAside,
    KTHeader,
    KTFooter,
    KTScrollTop,
    KTCreateApp,
    KTInviteFriendsModal,
    KTActivivityDrawer,
    KTDemosDrawer,
    KTHelpDrawer,
    KTDrawerMessenger,
  },
  setup() {
    const route = useRoute();

    onBeforeMount(() => {
      LayoutService.init();
    });

    onMounted(() => {
      nextTick(() => {
        reinitializeComponents();
      });
    });

    watch(
      () => route.path,
      () => {
        nextTick(() => {
          reinitializeComponents();
        });
      }
    );

    return {
      toolbarDisplay,
      loaderEnabled,
      contentWidthFluid,
      loaderLogo,
      asideEnabled,
      subheaderDisplay,
      themeLightLogo,
      themeDarkLogo,
    };
  },
});
</script>
