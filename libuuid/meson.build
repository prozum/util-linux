subdir('uuid')

libuuid_inc = include_directories('.')

libuuid = library('libuuid',
                  libuuid_srcs,
                  include_directories: [global_inc, libuuid_inc],
                  link_with: lib
)


libuuid_dep = declare_dependency(link_with: libuuid, include_directories: libuuid_inc)
