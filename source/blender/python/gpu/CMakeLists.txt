# SPDX-License-Identifier: GPL-2.0-or-later

set(INC
  .
  ../../blenkernel
  ../../blenlib
  ../../editors/include
  ../../gpu
  ../../imbuf
  ../../makesdna
  ../../../../intern/glew-mx
  ../../../../intern/guardedalloc
)

set(INC_SYS
  ${GLEW_INCLUDE_PATH}
  ${PYTHON_INCLUDE_DIRS}
)

set(SRC
  gpu_py.c
  gpu_py_api.c
  gpu_py_batch.c
  gpu_py_buffer.c
  gpu_py_capabilities.c
  gpu_py_element.c
  gpu_py_framebuffer.c
  gpu_py_matrix.c
  gpu_py_offscreen.c
  gpu_py_platform.c
  gpu_py_select.c
  gpu_py_shader.c
  gpu_py_state.c
  gpu_py_texture.c
  gpu_py_types.c
  gpu_py_uniformbuffer.c
  gpu_py_vertex_buffer.c
  gpu_py_vertex_format.c

  gpu_py.h
  gpu_py_api.h
  gpu_py_batch.h
  gpu_py_buffer.h
  gpu_py_capabilities.h
  gpu_py_element.h
  gpu_py_framebuffer.h
  gpu_py_matrix.h
  gpu_py_offscreen.h
  gpu_py_platform.h
  gpu_py_select.h
  gpu_py_shader.h
  gpu_py_state.h
  gpu_py_texture.h
  gpu_py_types.h
  gpu_py_uniformbuffer.h
  gpu_py_vertex_buffer.h
  gpu_py_vertex_format.h
)

set(LIB
  ${PYTHON_LINKFLAGS}
  ${PYTHON_LIBRARIES}
)

add_definitions(${GL_DEFINITIONS})

blender_add_lib(bf_python_gpu "${SRC}" "${INC}" "${INC_SYS}" "${LIB}")
