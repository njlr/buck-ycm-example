load('//:subdir_glob.bzl', 'subdir_glob')
load('//:buckaroo_macros.bzl', 'buckaroo_deps')

cxx_binary(
  name = 'app',
  header_namespace = '',
  headers = subdir_glob([
    ('include', '**/*.hpp'),
  ]),
  srcs = glob([
    'src/**/*.cpp',
  ]),
  deps = buckaroo_deps(),
)
