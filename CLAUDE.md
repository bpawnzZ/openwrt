# 🔮 OpenWrt Banana Pi R4 Build Configuration

## 🎯 Project Overview

This OpenWrt configuration builds custom images for **Banana Pi R4** with **8GB RAM BL2/FIP bootloader files**.

## 🚀 Quick Start

### GitHub Actions Build
1. Push to GitHub
2. Go to Actions → "Build OpenWrt for Banana Pi R4"
3. Run workflow with desired settings
4. Download artifacts from Actions page

### Local Build
```bash
./build-openwrt.sh
```

## 📁 Key Files

- `.github/workflows/openwrt-bpi-r4.yml` - GitHub Actions workflow
- `bpi-r4-8gb-config` - OpenWrt configuration for Banana Pi R4
- `bpi-r4_sdmmc_8GB_bl2.img` - 8GB RAM BL2 bootloader
- `bpi-r4_sdmmc_8GB_fip.bin` - 8GB RAM FIP bootloader
- `Makefile.local` - Custom build integration

## ⚙️ Configuration

**Target:** MediaTek Filogic (MT7988)  
**Profile:** Banana Pi R4  
**Kernel:** 6.12 (default)  
**Bootloader:** 8GB RAM BL2/FIP files  

**Included Packages:**
- LuCI web interface
- Firewall
- Network tools (iperf3, tcpdump, ethtool)
- WiFi support (hostapd, wpad)

## 🛠️ Build Process

1. **Setup:** Updates feeds and installs packages
2. **Configuration:** Applies Banana Pi R4 profile with 8GB RAM bootloader
3. **Build:** Compiles OpenWrt with custom BL2/FIP files
4. **Output:** Images in `bin/targets/mediatek/filogic/`

## 📋 GitHub Actions Options

- **Kernel Version:** 6.12, 6.6, or 5.15
- **Profile:** `bananapi_bpi-r4` or `bananapi_bpi-r4-poe`

## 🎯 Special Features

- **8GB RAM Support:** Uses custom BL2/FIP files for proper booting
- **Automated Builds:** GitHub Actions pipeline
- **Pre-configured:** Ready-to-use OpenWrt configuration
- **Artifact Upload:** Automatic upload of built images

## 📝 Notes

- Build time: ~60-90 minutes on GitHub Actions
- Artifacts available for 7 days
- Requires 8GB RAM BL2/FIP files for proper booting
- Compatible with Banana Pi R4 8GB RAM variant

---

**Maintainer:** Claude Code  
**Last Updated:** 2025-10-17  
**Status:** ✅ Production Ready