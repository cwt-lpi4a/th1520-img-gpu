# Maintainer: Chaiwat Suttipongsakul <cwt@bashell.com>
_reponame="thead-gles-addons"
pkgname="th1520-img-gpu"
pkgver=r4.8d02e2c
pkgrel=1
pkgdesc="TH1520 Imagination PowerVR GPU with OpenGL ES, Vulkan, and OpenCL for Arch Linux"
arch=('riscv64')
url="https://github.com/revyos/${_reponame}"
license=('proprietary')
depends=('gcc-libs' 'libdrm' 'libffi' 'wayland' 'vulkan-icd-loader')
makedepends=('git')
options=('!strip')
source=("git+https://github.com/revyos/${_reponame}.git")
md5sums=('SKIP')

pkgver() {
  cd "$srcdir/$_reponame"
  printf 'r%s.%s' "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
  cd "$srcdir/$_reponame/addons"

  install -Dm644 etc/OpenCL/vendors/IMG.icd \
    "${pkgdir}/etc/OpenCL/vendors/IMG.icd"
  install -Dm644 etc/vulkan/icd.d/icdconf.json \
    "${pkgdir}/etc/vulkan/icd.d/icdconf.json"

  install -Dm644 lib/firmware/rgx.fw.36.52.104.182 \
    "${pkgdir}/usr/lib/firmware/rgx.fw.36.52.104.182"
  install -Dm644 lib/firmware/rgx.sh.36.52.104.182 \
    "${pkgdir}/usr/lib/firmware/rgx.sh.36.52.104.182"

  install -Dm755 usr/bin/hwperfbin2jsont \
    "${pkgdir}/usr/bin/hwperfbin2jsont"
  install -Dm755 usr/bin/hwperfjsonmerge.py \
    "${pkgdir}/usr/bin/hwperfjsonmerge.py"
  install -Dm755 usr/bin/ocl_extended_test \
    "${pkgdir}/usr/bin/ocl_extended_test"
  install -Dm755 usr/bin/ocl_unit_test \
    "${pkgdir}/usr/bin/ocl_unit_test"
  install -Dm755 usr/bin/pvr_memory_test \
    "${pkgdir}/usr/bin/pvr_memory_test"
  install -Dm755 usr/bin/pvr_mutex_perf_test_mx \
    "${pkgdir}/usr/bin/pvr_mutex_perf_test_mx"
  install -Dm755 usr/bin/pvrdebug \
    "${pkgdir}/usr/bin/pvrdebug"
  install -Dm755 usr/bin/pvrhtb2txt \
    "${pkgdir}/usr/bin/pvrhtb2txt"
  install -Dm755 usr/bin/pvrhtbd \
    "${pkgdir}/usr/bin/pvrhtbd"
  install -Dm755 usr/bin/pvrhwperf \
    "${pkgdir}/usr/bin/pvrhwperf"
  install -Dm755 usr/bin/pvrlogdump \
    "${pkgdir}/usr/bin/pvrlogdump"
  install -Dm755 usr/bin/pvrlogsplit \
    "${pkgdir}/usr/bin/pvrlogsplit"
  install -Dm755 usr/bin/pvrsrvctl \
    "${pkgdir}/usr/bin/pvrsrvctl"
  install -Dm755 usr/bin/pvrtld \
    "${pkgdir}/usr/bin/pvrtld"
  install -Dm755 usr/bin/rgx_blit_test \
    "${pkgdir}/usr/bin/rgx_blit_test"
  install -Dm755 usr/bin/rgx_compute_test \
    "${pkgdir}/usr/bin/rgx_compute_test"
  install -Dm755 usr/bin/rgx_kicksync_test \
    "${pkgdir}/usr/bin/rgx_kicksync_test"
  install -Dm755 usr/bin/rgx_triangle_test \
    "${pkgdir}/usr/bin/rgx_triangle_test"
  install -Dm755 usr/bin/rgx_twiddling_test \
    "${pkgdir}/usr/bin/rgx_twiddling_test"
  install -Dm755 usr/bin/rogue2d_fbctest \
    "${pkgdir}/usr/bin/rogue2d_fbctest"
  install -Dm755 usr/bin/rogue2d_unittest \
    "${pkgdir}/usr/bin/rogue2d_unittest"

  install -Dm755 usr/lib/libGLESv1_CM_PVR_MESA.so \
    "${pkgdir}/usr/lib/libGLESv1_CM_PVR_MESA.so"
  install -Dm755 usr/lib/libGLESv2_PVR_MESA.so \
    "${pkgdir}/usr/lib/libGLESv2_PVR_MESA.so"
  install -Dm755 usr/lib/libPVROCL.so \
    "${pkgdir}/usr/lib/libPVROCL.so"
  install -Dm755 usr/lib/libPVRScopeServices.so \
    "${pkgdir}/usr/lib/libPVRScopeServices.so"
  install -Dm755 usr/lib/libVK_IMG.so \
    "${pkgdir}/usr/lib/libVK_IMG.so"
  install -Dm755 usr/lib/libglslcompiler.so \
    "${pkgdir}/usr/lib/libglslcompiler.so"
  install -Dm755 usr/lib/libpvr_dri_support.so \
    "${pkgdir}/usr/lib/libpvr_dri_support.so"
  install -Dm755 usr/lib/libsrv_um.so \
    "${pkgdir}/usr/lib/libsrv_um.so"
  install -Dm755 usr/lib/libsutu_display.so \
    "${pkgdir}/usr/lib/libsutu_display.so"
  install -Dm755 usr/lib/libufwriter.so \
    "${pkgdir}/usr/lib/libufwriter.so"
  install -Dm755 usr/lib/libusc.so \
    "${pkgdir}/usr/lib/libusc.so"

  cd ${pkgdir}/usr/lib
  ln -s libPVROCL.so libPVROCL.so.1
  ln -s libVK_IMG.so libVK_IMG.so.1
}
