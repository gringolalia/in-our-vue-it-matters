<template lang="pug">
#app
	.page-container.md-layout-column
		md-toolbar.md-primary
			md-button.md-icon-button(@click='showNavigation = true')
				md-icon menu
			span.md-title 
				i.fas.fa-sun.fa-2x.mr-2.ml-0
				| Engenho Novo LLC
			.md-toolbar-section-end
				md-button(@click='showSidepanel = true') Collateral Dommage
		md-drawer(:md-active.sync='showNavigation' md-swipeable)
			md-toolbar.md-transparent(md-elevation='0')
				span.md-title The Oca Engenhoca
			md-list
				md-list-item
					md-icon move_to_inbox
					span.md-list-item-text Inbox
				md-list-item
					md-icon send
					span.md-list-item-text Sent Mail
				md-list-item
					md-icon delete
					span.md-list-item-text Trash
				md-list-item
					md-icon error
					span.md-list-item-text Spam
		md-drawer.md-right(:md-active.sync='showSidepanel')
			md-toolbar.md-transparent(md-elevation='0')
				span.md-title Selections
			md-list
				md-list-item
					span.md-list-item-text Abbey Christansen
					md-button.md-icon-button.md-list-action
						md-icon.md-primary chat_bubble
				md-list-item
					span.md-list-item-text Alex Nelson
					md-button.md-icon-button.md-list-action
						md-icon.md-primary chat_bubble
				md-list-item
					span.md-list-item-text Mary Johnson
					md-button.md-icon-button.md-list-action
						md-icon chat_bubble
		md-content
			router-view
</template>

<script>
  export default {
    name: 'Temporary',
    data: () => ({
      showNavigation: false,
      showSidepanel: false
    })
  }
</script>

<style lang="scss">

@import "~vue-material/dist/theme/engine";

@include md-register-theme("default", (
	primary: #607d8b,
	accent: #2a3439, 
));

@import "~vue-material/dist/theme/all"; 

.page-container {
    min-height: 300px;
    overflow: hidden;
    position: relative;
    border: 1px solid rgba(#000, .12);
  }

   // Demo purposes only
  .md-drawer {
    width: 230px;
    max-width: calc(100vw - 125px);
  }

  .md-content {
    padding: 16px;
  }
</style>
