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




#======== ICONS ========

# Install our icons in all the required sizes
icon_sizes = ['16', '24', '32', '48', '64', '128']


fs = import('fs')
configdir = fs.expanduser('~/.local/share/io.github.teamcons.storyline')

foreach i : icon_sizes
    install_data(
        join_paths('icons', i, i + '.svg'),
        install_dir: join_paths(get_option('datadir'), 'icons', 'hicolor', i + 'x' + i, 'apps')
    )
endforeach

foreach i : icon_sizes
    install_data(
        join_paths('icons', i, i + '.svg'),
        install_dir: join_paths(get_option('datadir'), 'icons', 'hicolor', i + 'x' + i + '@2', 'apps')
    )
endforeach

install_data(
    join_paths('icons', '16', '16.svg'),
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
