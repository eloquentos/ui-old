AC_INIT(
    [arc-theme],
    [20151031],
    [https://github.com/horst3180/Arc-theme/issues],
    [arc-theme],
    [https://github.com/horst3180/Arc-theme],
    []
)

AC_CONFIG_AUX_DIR([build-aux])
AC_CONFIG_MACRO_DIR([m4])
AM_INIT_AUTOMAKE([foreign])
AC_PROG_MKDIR_P

ARC_ENABLE([LIGHT],         [light],         [Arc Light],     [disable])
ARC_ENABLE([GNOME_SHELL],   [gnome-shell],   [GNOME Shell],   [disable])
ARC_ENABLE([GTK2],          [gtk2],          [GTK2],          [disable])
ARC_ENABLE([GTK3],          [gtk3],          [GTK3],          [disable])
ARC_ENABLE([METACITY],      [metacity],      [Metacity],      [disable])
ARC_ENABLE([TRANSPARENCY],  [transparency],  [transparency],  [disable])

ARC_GNOME

AC_CONFIG_FILES([
    common/Makefile
    Makefile
])

AC_OUTPUT
