---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
ms.openlocfilehash: 87ea9af1980948f28477a9f483b3c6429df98d12
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370777"
---
# <span data-ttu-id="af10a-101">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="af10a-101">Add-AzVmssExtension</span></span>

## <span data-ttu-id="af10a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af10a-102">SYNOPSIS</span></span>
<span data-ttu-id="af10a-103">VMSS에 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="af10a-103">Adds an extension to the VMSS.</span></span>

## <span data-ttu-id="af10a-104">구문</span><span class="sxs-lookup"><span data-stu-id="af10a-104">SYNTAX</span></span>

```
Add-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-ProvisionAfterExtension <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af10a-105">설명</span><span class="sxs-lookup"><span data-stu-id="af10a-105">DESCRIPTION</span></span>
<span data-ttu-id="af10a-106">**Add-AzVmssExtension** cmdlet은 VMSS(Virtual Machine Scale Set)에 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="af10a-106">The **Add-AzVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="af10a-107">예제</span><span class="sxs-lookup"><span data-stu-id="af10a-107">EXAMPLES</span></span>

### <span data-ttu-id="af10a-108">예제 1: VMSS에 확장 추가</span><span class="sxs-lookup"><span data-stu-id="af10a-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="af10a-109">이 명령은 VMSS에 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="af10a-109">This command adds an extension to the VMSS.</span></span>

### <span data-ttu-id="af10a-110">예제 2: 설정 및 보호된 설정을 사용하여 VMSS에 확장 추가</span><span class="sxs-lookup"><span data-stu-id="af10a-110">Example 2: Add an extension to the VMSS with settings and protected settings</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};

PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName -Publisher $vmssPublisher  `
  -Type $vmssExtensionType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True  `
  -Setting $Settings -ProtectedSetting $ProtectedSettings
```

<span data-ttu-id="af10a-111">이 명령은 Blob Storage에서 샘플 bash 스크립트를 사용하여 VMSS에 확장을 추가하고, 보호된 설정에서 설정 및 보안 액세스에서 Blob Storage 및 실행 파일 명령의 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af10a-111">This command adds an extension to the VMSS with a sample bash script on a blob storage, specify the url of blob storage and executable command in settings and security access in protected settings.</span></span> 

## <span data-ttu-id="af10a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af10a-112">PARAMETERS</span></span>

### <span data-ttu-id="af10a-113">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="af10a-113">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="af10a-114">확장 버전을 최신 부 버전으로 자동으로 업데이트해야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="af10a-114">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="af10a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af10a-115">-DefaultProfile</span></span>
<span data-ttu-id="af10a-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="af10a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af10a-117">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="af10a-117">-ForceUpdateTag</span></span>
<span data-ttu-id="af10a-118">값이 제공되고 이전 값과 다른 경우 확장 구성이 변경되지 않은 경우에도 확장 처리기에서 강제로 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="af10a-118">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="af10a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="af10a-119">-Name</span></span>
<span data-ttu-id="af10a-120">이 cmdlet이 추가하는 확장의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af10a-120">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="af10a-121">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="af10a-121">-ProtectedSetting</span></span>
<span data-ttu-id="af10a-122">확장에 대한 개인 구성을 문자열로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af10a-122">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="af10a-123">이 cmdlet은 개인 구성을 암호화합니다.</span><span class="sxs-lookup"><span data-stu-id="af10a-123">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="af10a-124">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="af10a-124">-ProvisionAfterExtension</span></span>
<span data-ttu-id="af10a-125">이 확장을 프로비전해야 하는 확장 이름의 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="af10a-125">Collection of extension names after which this extension needs to be provisioned.</span></span>

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

### <span data-ttu-id="af10a-126">-Publisher</span><span class="sxs-lookup"><span data-stu-id="af10a-126">-Publisher</span></span>
<span data-ttu-id="af10a-127">확장 게시자의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af10a-127">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="af10a-128">게시자는 확장을 등록할 때 이름을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="af10a-128">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="af10a-129">[Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet을 사용하여 게시자를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af10a-129">This can use the [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="af10a-130">-Setting</span><span class="sxs-lookup"><span data-stu-id="af10a-130">-Setting</span></span>
<span data-ttu-id="af10a-131">확장에 대한 공용 구성을 문자열로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af10a-131">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="af10a-132">이 cmdlet은 공용 구성을 암호화하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="af10a-132">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="af10a-133">-Type</span><span class="sxs-lookup"><span data-stu-id="af10a-133">-Type</span></span>
<span data-ttu-id="af10a-134">확장 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af10a-134">Specifies the extension type.</span></span>
<span data-ttu-id="af10a-135">[Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet을 사용하여 확장 형식을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af10a-135">You can use the [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="af10a-136">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="af10a-136">-TypeHandlerVersion</span></span>
<span data-ttu-id="af10a-137">이 가상 머신에 사용할 확장의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af10a-137">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="af10a-138">[Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet을 사용하여 확장 버전을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af10a-138">You can use the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="af10a-139">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="af10a-139">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="af10a-140">VMSS 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="af10a-140">Specify the VMSS object.</span></span>
<span data-ttu-id="af10a-141">[New-AzVmssConfig를](./New-AzVmssConfig.md) 사용하여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af10a-141">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="af10a-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af10a-142">-Confirm</span></span>
<span data-ttu-id="af10a-143">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="af10a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af10a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af10a-144">-WhatIf</span></span>
<span data-ttu-id="af10a-145">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="af10a-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="af10a-146">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="af10a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af10a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af10a-147">CommonParameters</span></span>
<span data-ttu-id="af10a-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="af10a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af10a-149">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="af10a-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af10a-150">입력</span><span class="sxs-lookup"><span data-stu-id="af10a-150">INPUTS</span></span>

### <span data-ttu-id="af10a-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="af10a-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="af10a-152">System.String</span><span class="sxs-lookup"><span data-stu-id="af10a-152">System.String</span></span>

### <span data-ttu-id="af10a-153">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="af10a-153">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="af10a-154">System.Object</span><span class="sxs-lookup"><span data-stu-id="af10a-154">System.Object</span></span>

## <span data-ttu-id="af10a-155">출력</span><span class="sxs-lookup"><span data-stu-id="af10a-155">OUTPUTS</span></span>

### <span data-ttu-id="af10a-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="af10a-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="af10a-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="af10a-157">NOTES</span></span>

## <span data-ttu-id="af10a-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="af10a-158">RELATED LINKS</span></span>

[<span data-ttu-id="af10a-159">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="af10a-159">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)

[<span data-ttu-id="af10a-160">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="af10a-160">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="af10a-161">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="af10a-161">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="af10a-162">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="af10a-162">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="af10a-163">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="af10a-163">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
