<template>
  <!-- Sidebar -->
  <div
    class="hidden lg:block fixed lg:max-w-[295px] w-full overflow-y-auto h-full bg-white z-[999]"
    id="sidebarHRIS"
  >
    <div class="px-6 py-[50px] gap-y-[50px] flex flex-col">
      <div class="flex items-center justify-between">
        <a href="#" class="flex justify-center">
          <img src="/assets/svgs/logo-type.svg" alt="" />
        </a>
        <a href="#" id="toggleCloseSidebar" class="lg:hidden">
          <svg
            class="w-6 h-6 text-dark"
            fill="none"
            stroke="currentColor"
            viewBox="0 0 24 24"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M6 18L18 6M6 6l12 12"
            ></path>
          </svg>
        </a>
      </div>
      <div class="flex flex-col gap-4">
        <div class="text-sm text-grey">Daily Use</div>
        <NavLink
          v-for="(navLink, index) in navLinks"
          :key="index"
          :to="navLink.to"
          :label="navLink.label"
          :iconSrc="navLink.iconSrc"
          :isActive="navLink.isActive"
        />
      </div>
      <div class="flex flex-col gap-4">
        <div class="text-sm text-grey">Others</div>
        <a href="#" class="nav-link">
          <img src="/assets/svgs/ic-box.svg" alt="" />
          Insurances
        </a>
        <a href="#" class="nav-link">
          <img src="/assets/svgs/ic-home.svg" alt="" />
          Company
        </a>
        <a href="#" class="nav-link">
          <img src="/assets/svgs/ic-gift.svg" alt="" />
          Rewards
        </a>
        <a href="#" class="nav-link">
          <img src="/assets/svgs/ic-settings.svg" alt="" />
          Settings
        </a>
        <a href="#" class="nav-link">
          <img src="/assets/svgs/ic-signout.svg" alt="" />
          Logout
        </a>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      navLinks: [
        {
          to: { name: 'companies-id' },
          label: 'Overview',
          iconSrc: '/assets/svgs/ic-grid.svg',
        },
        {
          to: { name: 'companies-id-employees' },
          label: 'Employees',
          iconSrc: '/assets/svgs/ic-users.svg',
        },
        {
          to: { name: 'companies-id-teams' },
          label: 'My Teams',
          iconSrc: '/assets/svgs/ic-briefcase.svg',
        },
        {
          to: { name: 'companies-id-roles' },
          label: 'Roles',
          iconSrc: '/assets/svgs/ic-flag.svg',
        },
        // tambahkan data lainnya sesuai kebutuhan
      ],
    }
  },
}
</script>
