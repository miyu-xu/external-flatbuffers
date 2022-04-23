inc_flatbuffers = include_directories('include')

files_flatc = files(
  'src/idl_parser.cpp',
  'src/idl_gen_text.cpp',
  'src/reflection.cpp',
  'src/util.cpp',
  'src/idl_gen_cpp.cpp',
  'src/idl_gen_csharp.cpp',
  'src/idl_gen_dart.cpp',
  'src/idl_gen_kotlin.cpp',
  'src/idl_gen_go.cpp',
  'src/idl_gen_java.cpp',
  'src/idl_gen_js_ts.cpp',
  'src/idl_gen_php.cpp',
  'src/idl_gen_python.cpp',
  'src/idl_gen_lobster.cpp',
  'src/idl_gen_lua.cpp',
  'src/idl_gen_rust.cpp',
  'src/idl_gen_fbs.cpp',
  'src/idl_gen_grpc.cpp',
  'src/idl_gen_json_schema.cpp',
  'src/idl_gen_swift.cpp',
  'src/flatc.cpp',
  'src/flatc_main.cpp',
  'include/flatbuffers/code_generators.h',
  'src/code_generators.cpp',
  'grpc/src/compiler/schema_interface.h',
  'grpc/src/compiler/cpp_generator.h',
  'grpc/src/compiler/cpp_generator.cc',
  'grpc/src/compiler/go_generator.h',
  'grpc/src/compiler/go_generator.cc',
  'grpc/src/compiler/java_generator.h',
  'grpc/src/compiler/java_generator.cc',
  'grpc/src/compiler/python_generator.h',
  'grpc/src/compiler/python_private_generator.h',
  'grpc/src/compiler/python_generator.cc',
  'grpc/src/compiler/swift_generator.h',
  'grpc/src/compiler/swift_generator.cc',
)

flatc = executable(
  'flatc',
  files_flatc,
  cpp_args: [
    '-fsigned-char',
    '-pedantic',
    '-Wall',
    '-Werror',
    '-Wextra',
    '-Werror=shadow',
    '-Wno-implicit-fallthrough', # in reflection.cpp
  ],
  include_directories: [
    inc_flatbuffers,
    'grpc',
  ]
)

files_flatbuffers = files(
  'src/code_generators.cpp',
  'src/idl_gen_fbs.cpp',
  'src/idl_gen_text.cpp',
  'src/idl_parser.cpp',
  'src/reflection.cpp',
  'src/util.cpp',
)

lib_flatbuffers = static_library(
  'flatbuffers',
  files_flatbuffers,
  include_directories: [inc_flatbuffers]
)

