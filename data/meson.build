# Gnome resources
gnome = import('gnome')

# Icons
icon_sizes = ['16', '24', '32', '48', '64', '128']

foreach i : icon_sizes
  install_data(
    'images/logo/' + i + '.png',
    install_dir: get_option('datadir') + '/icons/hicolor/' + i + 'x' + i + '/apps',
    rename: meson.project_name() + '.png',
  )

  install_data(
    'images/logo/' + i + '.png',
    install_dir: get_option('datadir') + '/icons/hicolor/' + i + 'x' + i + '@2/apps',
    rename: meson.project_name() + '.png',
  )
endforeach

# Settings
install_data(
  'gschema.xml',
  install_dir: get_option('datadir') + '/glib-2.0/schemas',
  rename: meson.project_name() + '.gschema.xml',
)

# Desktop file
i18n.merge_file(
  type: 'desktop',
  input: meson.project_name() + '.desktop.in',
  output: meson.project_name() + '.desktop',
  po_dir: meson.source_root() + '/po',
  install_dir: get_option('datadir') + '/applications',
  install: true,
)

# Metainfo file
i18n.merge_file(
  input: meson.project_name() + '.appdata.xml.in',
  output: meson.project_name() + '.appdata.xml',
  po_dir: meson.source_root() + '/po',
  install_dir: get_option('datadir') + '/metainfo',
  install: true,
)