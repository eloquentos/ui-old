themedir        = $(datadir)/themes/Eloquent

ithemedir       = $(DESTDIR)$(themedir)

install-exec-hook:

install-data-local:

if ENABLE_LIGHT
	$(MKDIR_P) $(ithemedir)
	cp --no-preserve=mode,ownership $(srcdir)/index.theme $(ithemedir)
endif # ENABLE_LIGHT


if ENABLE_GNOME_SHELL
	$(MKDIR_P) $(ithemedir)/gnome-shell

	cd $(srcdir)/gnome-shell/$(GNOME_VERSION) && cp -r --no-preserve=mode,ownership \
		common-assets \
		light-assets \
		gnome-shell.css \
		$(ithemedir)/gnome-shell

endif # ENABLE_GNOME_SHELL


if ENABLE_GTK2

if ENABLE_LIGHT
	$(MKDIR_P) $(ithemedir)/gtk-2.0

	cd $(srcdir)/gtk-2.0 && cp -r --no-preserve=mode,ownership \
		assets \
		menubar-toolbar \
		*.rc \
		gtkrc \
		$(ithemedir)/gtk-2.0
endif # ENABLE_LIGHT

endif # ENABLE_GTK2


if ENABLE_GTK3

if ENABLE_LIGHT
	$(MKDIR_P) $(ithemedir)/gtk-3.0

	cd $(srcdir)/gtk-3.0/$(GNOME_VERSION) && cp -r --no-preserve=mode,ownership \
		assets \
		gtk.css \
		gtk-contained.css \
		gtk-dark.css \
		gtk-contained-dark.css \
		$(ithemedir)/gtk-3.0
endif # ENABLE_LIGHT

if !ENABLE_TRANSPARENCY

if ENABLE_LIGHT
	cd $(srcdir)/gtk-3.0/$(GNOME_VERSION) && cp -r --no-preserve=mode,ownership \
		gtk-contained-solid.css \
		$(ithemedir)/gtk-3.0/gtk-contained.css

	cd $(srcdir)/gtk-3.0/$(GNOME_VERSION) && cp -r --no-preserve=mode,ownership \
		gtk-contained-solid-dark.css \
		$(ithemedir)/gtk-3.0/gtk-contained-dark.css
endif # ENABLE_LIGHT

endif #!ENABLE_TRANSPARENCY

endif # ENABLE_GTK3


if ENABLE_METACITY

if ENABLE_LIGHT
	cp -r --no-preserve=mode,ownership $(srcdir)/metacity-1 $(ithemedir)
endif # ENABLE_LIGHT
endif # ENABLE_METACITY

uninstall-local:
	rm -rf $(ithemedir)

EXTRA_DIST = $(srcdir)/gnome-shell \
	     $(srcdir)/gtk-2.0 \
	     $(srcdir)/gtk-3.0 \
	     $(srcdir)/metacity-1 \
	     $(srcdir)/index.theme
