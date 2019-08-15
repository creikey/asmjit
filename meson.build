project('asmjit', 'cpp')

sources = files()
inc = include_directories('src')
subdir('src')

asmjit_dependencies = [dependency('threads'), meson.get_compiler('cpp').find_library('rt', required : false)]

libasmjit = static_library('asmjit',
    sources,
    c_args : ['-DASMJIT_BUILD_X86', '-DASMJIT_STATIC'],
    dependencies : asmjit_dependencies,
    include_directories : inc)

libasmjit_dep = declare_dependency(include_directories : inc,
    link_with : libasmjit)
