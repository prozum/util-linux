subdir('src')

libuuid_inc = include_directories('src')

libuuid = library('libuuid',
                  libuuid_srcs,
                  include_directories: [global_inc, libuuid_inc],
                  link_with: lib
)

