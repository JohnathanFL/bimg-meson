project('bimg', 'cpp')
bimgHeaders = include_directories('bimg/include')
thirdParty = include_directories('bimg/3rdparty')

cpp = meson.get_compiler('cpp')
dl = cpp.find_library('dl', required: true)


bimg = library('bimg', 'bimg/src/amalgamated.cpp', include_directories: [bimgHeaders, thirdParty], dependencies: [dl])

bx_dep = declare_dependency(include_directories: [bimgHeaders, thirdParty], link_with: [bimg])
