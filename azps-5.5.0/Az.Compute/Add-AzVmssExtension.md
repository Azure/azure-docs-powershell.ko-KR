---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
ms.openlocfilehash: 152d6e861d7622e262279c1f665565347e0ab2cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204976"
---
# <span data-ttu-id="8d4d7-101">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="8d4d7-101">Add-AzVmssExtension</span></span>

## <span data-ttu-id="8d4d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d4d7-102">SYNOPSIS</span></span>
<span data-ttu-id="8d4d7-103">VMSS에 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="8d4d7-103">Adds an extension to the VMSS.</span></span>

## <span data-ttu-id="8d4d7-104">구문</span><span class="sxs-lookup"><span data-stu-id="8d4d7-104">SYNTAX</span></span>

```
Add-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-EnableAutomaticUpgrade <Boolean>] [-ForceUpdateTag <String>] [-ProvisionAfterExtension <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d4d7-105">설명</span><span class="sxs-lookup"><span data-stu-id="8d4d7-105">DESCRIPTION</span></span>
<span data-ttu-id="8d4d7-106">**Add-AzVmssExtension** cmdlet은 VMSS(Virtual Machine Scale Set)에 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="8d4d7-106">The **Add-AzVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="8d4d7-107">예제</span><span class="sxs-lookup"><span data-stu-id="8d4d7-107">EXAMPLES</span></span>

### <span data-ttu-id="8d4d7-108">예제 1: VMSS에 확장 추가</span><span class="sxs-lookup"><span data-stu-id="8d4d7-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="8d4d7-109">이 명령은 VMSS에 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="8d4d7-109">This command adds an extension to the VMSS.</span></span>

### <span data-ttu-id="8d4d7-110">예제 2: 설정 및 보호된 설정을 사용하여 VMSS에 확장 추가</span><span class="sxs-lookup"><span data-stu-id="8d4d7-110">Example 2: Add an extension to the VMSS with settings and protected settings</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};

PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName -Publisher $vmssPublisher  `
  -Type $vmssExtensionType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True  `
  -Setting $Settings -ProtectedSetting $ProtectedSettings
```

<span data-ttu-id="8d4d7-111">이 명령은 Blob Storage에서 샘플 bash 스크립트를 사용하여 VMSS에 확장을 추가하고, 보호된 설정에서 설정 및 보안 액세스에서 Blob Storage 및 실행 파일 명령의 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8d4d7-111">This command adds an extension to the VMSS with a sample bash script on a blob storage, specify the url of blob storage and executable command in settings and security access in protected settings.</span></span> 

## <span data-ttu-id="8d4d7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d4d7-112">PARAMETERS</span></span>

### <span data-ttu-id="8d4d7-113">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="8d4d7-113">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="8d4d7-114">확장 버전을 최신 부 버전으로 자동으로 업데이트해야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8d4d7-114">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d4d7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d4d7-115">-DefaultProfile</span></span>
<span data-ttu-id="8d4d7-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8d4d7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d4d7-117">-EnableAutomaticUpgrade</span><span class="sxs-lookup"><span data-stu-id="8d4d7-117">-EnableAutomaticUpgrade</span></span>
<span data-ttu-id="8d4d7-118">사용 가능한 확장의 최신 버전이 있는 경우 플랫폼에서 확장을 자동으로 업그레이드해야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8d4d7-118">Indicates whether the extension should be automatically upgraded by the platform if there is a newer version of the extension available.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d4d7-119">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="8d4d7-119">-ForceUpdateTag</span></span>
<span data-ttu-id="8d4d7-120">값이 제공되고 이전 값과 다른 경우 확장 구성이 변경되지 않은 경우에도 확장 처리기에서 강제로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d4d7-120">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d4d7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8d4d7-121">-Name</span></span>
<span data-ttu-id="8d4d7-122">이 cmdlet이 추가하는 확장의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8d4d7-122">Specifies the name of the extension that this cmdlet adds.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d4d7-123">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="8d4d7-123">-ProtectedSetting</span></span>
<span data-ttu-id="8d4d7-124">확장에 대한 개인 구성을 문자열로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8d4d7-124">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="8d4d7-125">이 cmdlet은 개인 구성을 암호화합니다.</span><span class="sxs-lookup"><span data-stu-id="8d4d7-125">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d4d7-126">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="8d4d7-126">-ProvisionAfterExtension</span></span>
<span data-ttu-id="8d4d7-127">이 확장을 프로비전해야 하는 확장 이름의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="8d4d7-127">Collection of extension names after which this extension needs to be provisioned.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d4d7-128">-Publisher</span><span class="sxs-lookup"><span data-stu-id="8d4d7-128">-Publisher</span></span>
<span data-ttu-id="8d4d7-129">확장 게시자의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8d4d7-129">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="8d4d7-130">게시자는 확장을 등록할 때 이름을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="8d4d7-130">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="8d4d7-131">[Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet을 사용하여 게시자를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d4d7-131">This can use the [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet to get the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d4d7-132">-Setting</span><span class="sxs-lookup"><span data-stu-id="8d4d7-132">-Setting</span></span>
<span data-ttu-id="8d4d7-133">확장에 대한 공용 구성을 문자열로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8d4d7-133">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="8d4d7-134">이 cmdlet은 공용 구성을 암호화하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8d4d7-134">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d4d7-135">-Type</span><span class="sxs-lookup"><span data-stu-id="8d4d7-135">-Type</span></span>
<span data-ttu-id="8d4d7-136">확장 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8d4d7-136">Specifies the extension type.</span></span>
<span data-ttu-id="8d4d7-137">[Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet을 사용하여 확장 형식을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d4d7-137">You can use the [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d4d7-138">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="8d4d7-138">-TypeHandlerVersion</span></span>
<span data-ttu-id="8d4d7-139">이 가상 머신에 사용할 확장의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8d4d7-139">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="8d4d7-140">[Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet을 사용하여 확장 버전을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d4d7-140">You can use the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d4d7-141">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8d4d7-141">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="8d4d7-142">VMSS 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8d4d7-142">Specify the VMSS object.</span></span>
<span data-ttu-id="8d4d7-143">[New-AzVmssConfig를](./New-AzVmssConfig.md) 사용하여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8d4d7-143">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d4d7-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d4d7-144">-Confirm</span></span>
<span data-ttu-id="8d4d7-145">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d4d7-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d4d7-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d4d7-146">-WhatIf</span></span>
<span data-ttu-id="8d4d7-147">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="8d4d7-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8d4d7-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8d4d7-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d4d7-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d4d7-149">CommonParameters</span></span>
<span data-ttu-id="8d4d7-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8d4d7-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d4d7-151">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8d4d7-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d4d7-152">입력</span><span class="sxs-lookup"><span data-stu-id="8d4d7-152">INPUTS</span></span>

### <span data-ttu-id="8d4d7-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8d4d7-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="8d4d7-154">System.String</span><span class="sxs-lookup"><span data-stu-id="8d4d7-154">System.String</span></span>

### <span data-ttu-id="8d4d7-155">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8d4d7-155">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8d4d7-156">System.Object</span><span class="sxs-lookup"><span data-stu-id="8d4d7-156">System.Object</span></span>

## <span data-ttu-id="8d4d7-157">출력</span><span class="sxs-lookup"><span data-stu-id="8d4d7-157">OUTPUTS</span></span>

### <span data-ttu-id="8d4d7-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8d4d7-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="8d4d7-159">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8d4d7-159">NOTES</span></span>

## <span data-ttu-id="8d4d7-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8d4d7-160">RELATED LINKS</span></span>

[<span data-ttu-id="8d4d7-161">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="8d4d7-161">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)

[<span data-ttu-id="8d4d7-162">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="8d4d7-162">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="8d4d7-163">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="8d4d7-163">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="8d4d7-164">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="8d4d7-164">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="8d4d7-165">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="8d4d7-165">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
