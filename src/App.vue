<script setup>
import '@kyndryl-design-system/shidoka-applications/components/global/uiShell';
import '@kyndryl-design-system/shidoka-applications/components/global/header';
import '@kyndryl-design-system/shidoka-applications/components/global/localNav';
import '@kyndryl-design-system/shidoka-applications/components/global/footer';

import SwitcherIcon from '@kyndryl-design-system/shidoka-foundation/assets/svg/switcher.svg?component';
import UserAvatar24 from '@carbon/icons-vue/es/user--avatar/24';
import UserAvatar20 from '@carbon/icons-vue/es/user--avatar/20';

import HelloWorld from './components/HelloWorld.vue';
</script>

<template>
  <kyn-ui-shell>
    <kyn-header divider="" apptitle="Shidoka Vue">
      <kyn-header-panel slot="left" heading="Panel Heading">
        <SwitcherIcon slot="button" />

        <kyn-header-panel-link href="javascript:void(0)">
          <UserAvatar24 />
          Link 1
        </kyn-header-panel-link>
        <kyn-header-panel-link href="javascript:void(0)">
          <UserAvatar24 />
          Link 2
        </kyn-header-panel-link>
        <kyn-header-panel-link href="javascript:void(0)">
          <UserAvatar24 />
          Link 3
        </kyn-header-panel-link>
      </kyn-header-panel>

      <kyn-header-nav>
        <kyn-header-link href="javascript:void(0)"> Link 1 </kyn-header-link>
        <kyn-header-link href="javascript:void(0)" isActive> Link 2 </kyn-header-link>
        <kyn-header-link href="javascript:void(0)">
          Link 3

          <kyn-header-link slot="links" href="javascript:void(0)"> Sub Link # 1 </kyn-header-link>
          <kyn-header-link slot="links" href="javascript:void(0)"> Sub Link 2 </kyn-header-link>
        </kyn-header-link>
      </kyn-header-nav>

      <kyn-header-flyouts>
        <kyn-header-flyout>
          <span slot="button">Sign in</span>

          <div>
            <kyn-header-link href="javascript:void(0)"> Login </kyn-header-link>
            <kyn-header-link href="javascript:void(0)"> Sign up </kyn-header-link>
          </div>
        </kyn-header-flyout>

        <kyn-header-flyout assistiveText="My Account" hideArrow>
          <kyn-header-avatar initials="KB" slot="button" />

          <kyn-header-link href="javascript:void(0)"> Logout </kyn-header-link>
        </kyn-header-flyout>
      </kyn-header-flyouts>
    </kyn-header>

    <kyn-local-nav>
      <kyn-local-nav-link href="javascript:void(0)" active="">
        <UserAvatar20 slot="icon" />
        Link 1
      </kyn-local-nav-link>

      <kyn-local-nav-link href="javascript:void(0)">
        <UserAvatar20 slot="icon" />
        Link 2

        <kyn-local-nav-link slot="links" href="javascript:void(0)"> L2 Link 1 </kyn-local-nav-link>
        <kyn-local-nav-link slot="links" href="javascript:void(0)"> L2 Link 2 </kyn-local-nav-link>
      </kyn-local-nav-link>

      <kyn-local-nav-link href="javascript:void(0)" expanded="">
        <UserAvatar20 slot="icon" />
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
      <span slot="copyright"> Copyright &copy; 2023 Kyndryl Inc. All rights reserved. </span>
    </kyn-footer>
  </kyn-ui-shell>
</template>
