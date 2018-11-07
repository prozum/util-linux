cc = meson.get_compiler('c')
cdata = configuration_data()
check_headers = [
  ['HAVE_SYS_FILE_H', 'sys/file.h']
]

foreach h : check_headers
  message(cc.has_header(h.get(1)))
  if cc.has_header(h.get(1))
    cdata.set(h.get(0), 1)
  endif
endforeach

check_functions = [
# check token ('HAVE_PROGRAM_INVOCATION_SHORT_NAME',)
# check token ('HAVE_ERR',)
# check token ('HAVE_ERRX',)
# check token ('HAVE_WARN',)
# check token ('HAVE_WARNX',)
# check token ('HAVE_LOFF_T',)
  ['HAVE_NANOSLEEP', 'nanosleep', '#include<time.h>'],
  ['HAVE_USLEEP', 'usleep', '#include<unistd.h>'],
# check token ('HAVE_SCANF_MS_MODIFIER',)
]

foreach f : check_functions
  if cc.has_function(f.get(1), prefix : f.get(2))
    cdata.set(f.get(0), 1)
  endif
endforeach


configure_file(output : 'config.h',
  configuration : cdata)