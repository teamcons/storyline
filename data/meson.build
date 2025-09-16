#======== SETTINGS ========
install_data (
    'storyline.gschema.xml',
    install_dir: get_option('datadir') / 'glib-2.0' / 'schemas',
    rename: meson.project_name() + '.gschema.xml'
)

#======== Internationalization ========
#Translate and install our .desktop file
i18n.merge_file(
    input: 'storyline.desktop.in',
    output: meson.project_name() + '.desktop',
    po_dir: meson.project_source_root() / 'po' / 'extra',
    type: 'desktop',
    install: true,
    install_dir: get_option('datadir') / 'applications'
)

#Translate and install our .metainfo file
i18n.merge_file(
    input: 'storyline.metainfo.xml.in',
    output: meson.project_name() + '.metainfo.xml',
    po_dir: meson.project_source_root() / 'po' / 'extra',
    install: true,
    install_dir: get_option('datadir') / 'metainfo'
)




fs = import('fs')

icon_sizes = ['32', '48', '64', '128']

configdir = fs.expanduser('~/.local/share/io.github.teamcons.storyline')

foreach i : icon_sizes
    install_data(
        join_paths('icons', i, 'io.github.teamcons.storyline.svg'),
        install_dir: join_paths(get_option('datadir'), 'icons', 'hicolor', i + 'x' + i, 'apps')
    )
endforeach

foreach i : icon_sizes
    install_data(
        join_paths('icons', i, 'io.github.teamcons.storyline.svg'),
        install_dir: join_paths(get_option('datadir'), 'icons', 'hicolor', i + 'x' + i + '@2', 'apps')
    )
endforeach

install_data(
    join_paths('icons', '16', 'io.github.teamcons.storyline-symbolic.svg'),
    install_dir: join_paths(get_option('datadir'), 'icons', 'hicolor', 'symbolic', 'apps')
)

install_data(
    join_paths('schemes', 'io.github.teamcons.storyline.xml'),
    install_dir: join_paths(get_option('datadir'), 'gtksourceview-4', 'styles')
)

install_data(
    join_paths('schemes', 'io.github.teamcons.storyline-sepia.xml'),
    install_dir: join_paths(get_option('datadir'), 'gtksourceview-4', 'styles')
)

install_data(
    join_paths('schemes', 'io.github.teamcons.storyline-dark.xml'),
    install_dir: join_paths(get_option('datadir'), 'gtksourceview-4', 'styles')
)

install_data(
    join_paths('font', 'QuiltMono.ttf'),
    install_dir: join_paths(get_option('datadir'), 'fonts', 'truetype', 'quilt')
)

install_data(
    join_paths('font', 'QuiltZwei.ttf'),
    install_dir: join_paths(get_option('datadir'), 'fonts', 'truetype', 'quilt')
)

install_data(
    join_paths('font', 'QuiltVier.ttf'),
    install_dir: join_paths(get_option('datadir'), 'fonts', 'truetype', 'quilt')
)

install_subdir(
    'plugin/highlight.js',
    install_dir: configdir
)

install_subdir(
    'plugin/katex',
    install_dir: configdir
)

install_subdir(
    'plugin/mermaid',
    install_dir: configdir
)

install_subdir(
    'wordlist',
    install_dir: configdir
)

# Resources
resources = gnome.compile_resources(
  'resources',
  'app.gresource.xml',
  gresource_bundle: true,
  source_dir: meson.current_build_dir()
)

