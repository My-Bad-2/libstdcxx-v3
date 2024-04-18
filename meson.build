project('libstdcxx', language: ['c', 'cpp']. version: '13.2.0')

include_dirs = []

if get_option('stdlib') == 'libstdc++'
    include_dirs += include_directories('libstdcxx/include')
    
    if get_option('architecture') == 'x86_64'
        include_dirs += include_directories('libstdcxx/arch/x86_64-elf')
    endif
else
    include_dirs += include_directories('libc++/include')
endif

libstdcxx_dep = declare_dependency(include_directories: include_dirs)