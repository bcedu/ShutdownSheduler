project('com.github.bcedu.shutdownscheduler', 'c', 'vala', version: '0.1.0')

i18n = import('i18n')
gnome = import('gnome')

# Install files listed in gresources
asresources = gnome.compile_resources(
	'as-resources',
    join_paths('data', 'resources', meson.project_name() + '.gresource.xml'),
    source_dir: 'data',
	c_name: 'as'
)

add_global_arguments('-DGETTEXT_PACKAGE="@0@"'.format (meson.project_name()), language:'c')

subdir('src')
subdir('data')
subdir('po')

meson.add_install_script('meson/post_install.py')