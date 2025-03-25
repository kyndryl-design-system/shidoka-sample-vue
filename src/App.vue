<script setup>
import '@kyndryl-design-system/shidoka-applications/components/global/uiShell';
import '@kyndryl-design-system/shidoka-applications/components/global/header';
import '@kyndryl-design-system/shidoka-applications/components/global/localNav';
import '@kyndryl-design-system/shidoka-applications/components/global/footer';

import UserAvatar from '@kyndryl-design-system/shidoka-icons/svg/monochrome/16/user.svg';
import sampleIcon from '@kyndryl-design-system/shidoka-icons/svg/monochrome/16/circle-stroke.svg';

import HelloWorld from './components/HelloWorld.vue';
</script>

<template>
  <kyn-ui-shell>
    <kyn-header divider="" apptitle="Shidoka Vue">
      <kyn-header-nav>
        <kyn-header-link href="javascript:void(0)"><sampleIcon /> Link 1 </kyn-header-link>
        <kyn-header-link href="javascript:void(0)" isActive><sampleIcon /> Link 2 </kyn-header-link>
        <kyn-header-link href="javascript:void(0)"><sampleIcon />
          Link 3

          <kyn-header-link slot="links" href="javascript:void(0)"> Sub Link # 1 </kyn-header-link>
          <kyn-header-link slot="links" href="javascript:void(0)"> Sub Link 2 </kyn-header-link>
        </kyn-header-link>
      </kyn-header-nav>

      <kyn-header-flyouts>
        <kyn-header-flyout label="Account">
          <UserAvatar slot="button" />
            <kyn-header-link href="javascript:void(0)"> Login </kyn-header-link>
            <kyn-header-link href="javascript:void(0)"> Sign up </kyn-header-link>
        </kyn-header-flyout>

        <kyn-header-flyout assistiveText="My Account" hideArrow>
          <kyn-header-avatar initials="KB" slot="button" />

          <kyn-header-link href="javascript:void(0)"> Logout </kyn-header-link>
        </kyn-header-flyout>
      </kyn-header-flyouts>
    </kyn-header>

    <kyn-local-nav>
      <kyn-local-nav-link href="javascript:void(0)" active="">
        <UserAvatar slot="icon"/>
        Link 1
      </kyn-local-nav-link>

      <kyn-local-nav-link href="javascript:void(0)">
        <UserAvatar slot="icon"/>
        Link 2

        <kyn-local-nav-link slot="links" href="javascript:void(0)"> L2 Link 1 </kyn-local-nav-link>
        <kyn-local-nav-link slot="links" href="javascript:void(0)"> L2 Link 2 </kyn-local-nav-link>
      </kyn-local-nav-link>

      <kyn-local-nav-link href="javascript:void(0)" expanded="">
        <UserAvatar slot="icon"/>
        Link 3

        <kyn-local-nav-link slot="links" href="javascript:void(0)">
          L2 Link 1

          <kyn-local-nav-link slot="links" href="javascript:void(0)">
            L3 Link 1
          </kyn-local-nav-link>
          <kyn-local-nav-link slot="links" href="javascript:void(0)">
            L3 Link 2
          </kyn-local-nav-link>
        </kyn-local-nav-link>
      </kyn-local-nav-link>
    </kyn-local-nav>

    <main>
      <HelloWorld />
    </main>

    <kyn-footer>
      <span slot="copyright"> Copyright &copy; 2025 Kyndryl Inc. All rights reserved. </span>
    </kyn-footer>
  </kyn-ui-shell>
</template>
