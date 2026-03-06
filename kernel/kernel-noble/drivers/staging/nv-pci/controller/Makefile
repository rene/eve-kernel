# SPDX-License-Identifier: GPL-2.0
# Copyright (c) 2022-2025, NVIDIA CORPORATION.  All rights reserved.

obj-$(CONFIG_NVIDIA_PCIE_TEGRA264_ST) += tegra-pcie-edma.o
obj-$(CONFIG_NVIDIA_PCIE_TEGRA264_ST) += pcie-tegra-vf.o

# Set config when build as OOT module.
ifdef CONFIG_NVIDIA_PCIE_TEGRA264_ST

obj-$(CONFIG_PCIE_TEGRA264) += pcie-tegra264.o
obj-$(CONFIG_PCIE_TEGRA264_EP) += pcie-tegra264-ep.o

obj-y += tegra-pcie-dma-lib.o

tegra-pcie-dma-lib-objs:= tegra-pcie-dma.o \
			  tegra234-pcie-edma.o \
			  tegra264-pcie-xdma.o
else
obj-m += pcie-tegra264.o
pcie-tegra264-objs := pcie-tegra-soc-dummy.o
endif
