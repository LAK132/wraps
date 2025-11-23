project(
  'glm',
  'cpp',
)

glm_dep = subproject('glm-wrap').get_variable('glm_dep')
meson.override_dependency('glm-1.0.2', glm_dep)
