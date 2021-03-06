# Copyright (C) Microsoft Corporation. All rights reserved.
# This file is distributed under the University of Illinois Open Source License. See LICENSE.TXT for details.
add_llvm_library(LLVMHLSL
  ComputeViewIdState.cpp
  ComputeViewIdStateBuilder.cpp
  ControlDependence.cpp
  DxilCondenseResources.cpp
  DxilContainerReflection.cpp
  DxilConvergent.cpp
  DxilEliminateOutputDynamicIndexing.cpp
  DxilExpandTrigIntrinsics.cpp
  DxilGenerationPass.cpp
  DxilLegalizeSampleOffsetPass.cpp
  DxilLinker.cpp
  DxilPreparePasses.cpp
  DxilPackSignatureElement.cpp
  DxilPatchShaderRecordBindings.cpp
  DxilPreserveAllOutputs.cpp
  DxilSimpleGVNHoist.cpp
  DxilSignatureValidation.cpp
  DxilTargetLowering.cpp
  DxilTargetTransformInfo.cpp
  DxilExportMap.cpp
  DxilValidation.cpp
  DxcOptimizer.cpp
  HLMatrixBitcastLowerPass.cpp
  HLMatrixLowerPass.cpp
  HLMatrixSubscriptUseReplacer.cpp
  HLMatrixType.cpp
  HLModule.cpp
  HLOperations.cpp
  HLOperationLower.cpp
  HLOperationLowerExtension.cpp
  HLPreprocess.cpp
  HLResource.cpp
  HLSignatureLower.cpp
  PauseResumePasses.cpp
  WaveSensitivityAnalysis.cpp

  ADDITIONAL_HEADER_DIRS
  ${LLVM_MAIN_INCLUDE_DIR}/llvm/IR
)

add_dependencies(LLVMHLSL intrinsics_gen)
