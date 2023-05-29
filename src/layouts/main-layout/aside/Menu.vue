<template>
  <!--begin::Menu wrapper-->
  <div
    id="kt_aside_menu_wrapper"
    ref="scrollElRef"
    class="hover-scroll-overlay-y px-2 my-5 my-lg-5"
    data-kt-scroll="true"
    data-kt-scroll-height="auto"
    data-kt-scroll-dependencies="{default: '#kt_aside_toolbar, #kt_aside_footer', lg: '#kt_header, #kt_aside_toolbar, #kt_aside_footer'}"
    data-kt-scroll-wrappers="#kt_aside_menu"
    data-kt-scroll-offset="5px"
  >
    <!--begin::Menu-->
    <div
      id="#kt_aside_menu"
      class="menu menu-column menu-title-gray-800 menu-state-title-primary menu-state-icon-primary menu-state-bullet-primary menu-arrow-gray-500"
      data-kt-menu="true"
    >
      <div class="menu-item">

        <a
          class="menu-link"
          href="/dashboard"
        >
          <span class="menu-icon">
            <i
              v-if="asideMenuIcons === 'font'"
              class="bi bi-card-text fs-3"
            ></i>
            <span
              v-else-if="asideMenuIcons === 'svg'"
              class="svg-icon svg-icon-2"
            >
            <i class="fa-solid fa-house"></i>
            </span>
          </span>
          <span class="menu-title"
          >{{ translate("главная") }}
          </span>
        </a>
        <a
          class="menu-link"
          href="#"
        >
          <span class="menu-icon">
            <i
              v-if="asideMenuIcons === 'font'"
              class="bi bi-card-text fs-3"
            ></i>
            <span
              v-else-if="asideMenuIcons === 'svg'"
              class="svg-icon svg-icon-2"
            >
            <i class="fa-solid fa-square-poll-horizontal"></i>
            </span>
          </span>
          <span class="menu-title"
          >{{ translate("Опросы (49)") }}
          </span>
        </a>
        <a
          class="menu-link"
          href="#"
        >
          <span class="menu-icon">
            <i
              v-if="asideMenuIcons === 'font'"
              class="bi bi-card-text fs-3"
            ></i>
            <span
              v-else-if="asideMenuIcons === 'svg'"
              class="svg-icon svg-icon-2"
            >
              <inline-svg
                :src="getAssetPath('media/icons/duotune/general/gen005.svg')"
              />
            </span>
          </span>
          <span class="menu-title"
          >{{ translate("Упр. опросами") }}
          </span>
        </a>
        <a
          class="menu-link"
          href="#"
        >
          <span class="menu-icon">
            <i
              v-if="asideMenuIcons === 'font'"
              class="bi bi-card-text fs-3"
            ></i>
            <span
              v-else-if="asideMenuIcons === 'svg'"
              class="svg-icon svg-icon-2"
            >
              <inline-svg
                :src="getAssetPath('media/icons/duotune/general/gen005.svg')"
              />
            </span>
          </span>
          <span class="menu-title"
          >{{ translate("Инф. материалы") }}
          </span>
        </a>
        <a
          class="menu-link"
          href="#"
        >
          <span class="menu-icon">
            <i
              v-if="asideMenuIcons === 'font'"
              class="bi bi-card-text fs-3"
            ></i>
            <span
              v-else-if="asideMenuIcons === 'svg'"
              class="svg-icon svg-icon-2"
            >
              <inline-svg
                :src="getAssetPath('media/icons/duotune/general/gen005.svg')"
              />
            </span>
          </span>
          <span class="menu-title"
          >{{ translate("Организация ОПК") }}
          </span>
        </a>
        <a
          class="menu-link"
          href="#"
        >
          <span class="menu-icon">
            <i
              v-if="asideMenuIcons === 'font'"
              class="bi bi-card-text fs-3"
            ></i>
            <span
              v-else-if="asideMenuIcons === 'svg'"
              class="svg-icon svg-icon-2"
            >
              <inline-svg
                :src="getAssetPath('media/icons/duotune/general/gen005.svg')"
              />
            </span>
          </span>
          <span class="menu-title  menu-sub-accordion"
          >{{ translate("Субьекты") }}
          </span>
        </a>
        <a
          class="menu-link"
          href="#"
        >
          <span class="menu-icon">
            <i
              v-if="asideMenuIcons === 'font'"
              class="bi bi-card-text fs-3"
            ></i>
            <span
              v-else-if="asideMenuIcons === 'svg'"
              class="svg-icon svg-icon-2"
            >
              <inline-svg
                :src="getAssetPath('media/icons/duotune/general/gen005.svg')"
              />
            </span>
          </span>
          <span class="menu-title"
          >{{ translate("Вузы") }}
          </span>
        </a>
        <a
          class="menu-link"
          href="#"
        >
          <span class="menu-icon">
            <i
              v-if="asideMenuIcons === 'font'"
              class="bi bi-card-text fs-3"
            ></i>
            <span
              v-else-if="asideMenuIcons === 'svg'"
              class="svg-icon svg-icon-2"
            >
              <inline-svg
                :src="getAssetPath('media/icons/duotune/general/gen005.svg')"
              />
            </span>
          </span>
          <span class="menu-title"
          >{{ translate("Филиалы вузов") }}
          </span>
        </a>
        <a
          class="menu-link"
          href="#"
        >
          <span class="menu-icon">
            <i
              v-if="asideMenuIcons === 'font'"
              class="bi bi-card-text fs-3"
            ></i>
            <span
              v-else-if="asideMenuIcons === 'svg'"
              class="svg-icon svg-icon-2"
            >
              <inline-svg
                :src="getAssetPath('media/icons/duotune/general/gen005.svg')"
              />
            </span>
          </span>
          <span class="menu-title"
          >{{ translate("Колледжи") }}
          </span>
        </a>
        <a
          class="menu-link"
          href="#"
        >
          <span class="menu-icon">
            <i
              v-if="asideMenuIcons === 'font'"
              class="bi bi-card-text fs-3"
            ></i>
            <span
              v-else-if="asideMenuIcons === 'svg'"
              class="svg-icon svg-icon-2"
            >
              <inline-svg
                :src="getAssetPath('media/icons/duotune/general/gen005.svg')"
              />
            </span>
          </span>
          <span class="menu-title"
          >{{ translate("Специальности") }}
          </span>
        </a>
        <a
          class="menu-link"
          href="#"
        >
          <span class="menu-icon">
            <i
              v-if="asideMenuIcons === 'font'"
              class="bi bi-card-text fs-3"
            ></i>
            <span
              v-else-if="asideMenuIcons === 'svg'"
              class="svg-icon svg-icon-2"
            >
              <inline-svg
                :src="getAssetPath('media/icons/duotune/general/gen005.svg')"
              />
            </span>
          </span>
          <span class="menu-title"
          >{{ translate("Профстандарты") }}
          </span>
        </a>
        <a
          class="menu-link"
          href="#"
        >
          <span class="menu-icon">
            <i
              v-if="asideMenuIcons === 'font'"
              class="bi bi-card-text fs-3"
            ></i>
            <span
              v-else-if="asideMenuIcons === 'svg'"
              class="svg-icon svg-icon-2"
            >
              <inline-svg
                :src="getAssetPath('media/icons/duotune/general/gen005.svg')"
              />
            </span>
          </span>
          <span class="menu-title"
          >{{ translate("Наименования") }}
          </span>
        </a>
        <a
          class="menu-link"
          href="#"
        >
          <span class="menu-icon">
            <i
              v-if="asideMenuIcons === 'font'"
              class="bi bi-card-text fs-3"
            ></i>
            <span
              v-else-if="asideMenuIcons === 'svg'"
              class="svg-icon svg-icon-2"
            >
              <inline-svg
                :src="getAssetPath('media/icons/duotune/general/gen005.svg')"
              />
            </span>
          </span>
          <span class="menu-title"
          >{{ translate("Пользователи") }}
          </span>
        </a>
        <a
          class="menu-link"
          href="#"
        >
          <span class="menu-icon">
            <i
              v-if="asideMenuIcons === 'font'"
              class="bi bi-card-text fs-3"
            ></i>
            <span
              v-else-if="asideMenuIcons === 'svg'"
              class="svg-icon svg-icon-2"
            >
              <inline-svg
                :src="getAssetPath('media/icons/duotune/general/gen005.svg')"
              />
            </span>
          </span>
          <span class="menu-title"
          >{{ translate("Студенты-целевики") }}
          </span>
        </a>
        <a
          class="menu-link"
          href="#"
        >
          <span class="menu-icon">
            <i
              v-if="asideMenuIcons === 'font'"
              class="bi bi-card-text fs-3"
            ></i>
            <span
              v-else-if="asideMenuIcons === 'svg'"
              class="svg-icon svg-icon-2"
            >
              <inline-svg
                :src="getAssetPath('media/icons/duotune/general/gen005.svg')"
              />
            </span>
          </span>
          <span class="menu-title"
          >{{ translate("Резюме студентов") }}
          </span>
        </a>
        <a
          class="menu-link"
          href="#"
        >
          <span class="menu-icon">
            <i
              v-if="asideMenuIcons === 'font'"
              class="bi bi-card-text fs-3"
            ></i>
            <span
              v-else-if="asideMenuIcons === 'svg'"
              class="svg-icon svg-icon-2"
            >
              <inline-svg
                :src="getAssetPath('media/icons/duotune/general/gen005.svg')"
              />
            </span>
          </span>
          <span class="menu-title"
          >{{ translate("КЦП") }}
          </span>
        </a>
        <a
          class="menu-link"
          href="#"
        >
          <span class="menu-icon">
            <i
              v-if="asideMenuIcons === 'font'"
              class="bi bi-card-text fs-3"
            ></i>
            <span
              v-else-if="asideMenuIcons === 'svg'"
              class="svg-icon svg-icon-2"
            >
              <inline-svg
                :src="getAssetPath('media/icons/duotune/general/gen005.svg')"
              />
            </span>
          </span>
          <span class="menu-title"
          >{{ translate("История событий") }}
          </span>
        </a>
        <a
          class="menu-link"
          href="#"
        >
          <span class="menu-icon">
            <i
              v-if="asideMenuIcons === 'font'"
              class="bi bi-card-text fs-3"
            ></i>
            <span
              v-else-if="asideMenuIcons === 'svg'"
              class="svg-icon svg-icon-2"
            >
              <inline-svg
                :src="getAssetPath('media/icons/duotune/general/gen005.svg')"
              />
            </span>
          </span>
          <span class="menu-title"
          >{{ translate("Отправка писем") }}
          </span>
        </a>
        <a
          class="menu-link"
          href="#"
        >
          <span class="menu-icon">
            <i
              v-if="asideMenuIcons === 'font'"
              class="bi bi-card-text fs-3"
            ></i>
            <span
              v-else-if="asideMenuIcons === 'svg'"
              class="svg-icon svg-icon-2"
            >
              <inline-svg
                :src="getAssetPath('media/icons/duotune/general/gen005.svg')"
              />
            </span>
          </span>
          <span class="menu-title"
          >{{ translate("Обратная связь") }}
          </span>
        </a>
      </div>
    </div>
    <!--end::Menu-->
  </div>
  <!--end::Menu wrapper-->
</template>

<script lang="ts">
import { getAssetPath } from "@/core/helpers/assets";
import { defineComponent, onMounted, ref } from "vue";
import { useI18n } from "vue-i18n";
import { useRoute } from "vue-router";
import { version } from "@/core/helpers/documentation";
import { asideMenuIcons } from "@/core/helpers/config";
import MainMenuConfig from "@/core/config/MainMenuConfig";

export default defineComponent({
  name: "kt-menu",
  components: {},
  setup() {
    const { t, te } = useI18n();
    const route = useRoute();
    const scrollElRef = ref<null | HTMLElement>(null);

    onMounted(() => {
      if (scrollElRef.value) {
        scrollElRef.value.scrollTop = 0;
      }
    });

    const translate = (text: string) => {
      if (te(text)) {
        return t(text);
      } else {
        return text;
      }
    };

    const hasActiveChildren = (match: string) => {
      return route.path.indexOf(match) !== -1;
    };

    return {
      hasActiveChildren,
      MainMenuConfig,
      asideMenuIcons,
      version,
      translate,
      scrollElRef,
      getAssetPath
    };
  }
});
</script>
