---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
ms.openlocfilehash: 87ea9af1980948f28477a9f483b3c6429df98d12
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212892"
---
# <span data-ttu-id="ac8b4-101">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="ac8b4-101">Add-AzVmssExtension</span></span>

## <span data-ttu-id="ac8b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac8b4-102">SYNOPSIS</span></span>
<span data-ttu-id="ac8b4-103">VMSS에 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac8b4-103">Adds an extension to the VMSS.</span></span>

## <span data-ttu-id="ac8b4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ac8b4-104">SYNTAX</span></span>

```
Add-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-ProvisionAfterExtension <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac8b4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ac8b4-105">DESCRIPTION</span></span>
<span data-ttu-id="ac8b4-106">**추가-AzVmssExtension** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합)에 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac8b4-106">The **Add-AzVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="ac8b4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ac8b4-107">EXAMPLES</span></span>

### <span data-ttu-id="ac8b4-108">예제 1: VMSS에 확장 추가</span><span class="sxs-lookup"><span data-stu-id="ac8b4-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="ac8b4-109">이 명령은 VMSS에 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac8b4-109">This command adds an extension to the VMSS.</span></span>

### <span data-ttu-id="ac8b4-110">예제 2: 설정 및 보호 된 설정을 사용 하 여 VMSS에 확장 추가</span><span class="sxs-lookup"><span data-stu-id="ac8b4-110">Example 2: Add an extension to the VMSS with settings and protected settings</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};

PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName -Publisher $vmssPublisher  `
  -Type $vmssExtensionType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True  `
  -Setting $Settings -ProtectedSetting $ProtectedSettings
```

<span data-ttu-id="ac8b4-111">이 명령은 blob 저장소에 샘플 bash 스크립트를 사용 하 여 VMSS에 확장을 추가 하 고, 보호 된 설정의 설정 및 보안 액세스에서 blob 저장소 및 실행 명령의 url을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac8b4-111">This command adds an extension to the VMSS with a sample bash script on a blob storage, specify the url of blob storage and executable command in settings and security access in protected settings.</span></span> 

## <span data-ttu-id="ac8b4-112">변수</span><span class="sxs-lookup"><span data-stu-id="ac8b4-112">PARAMETERS</span></span>

### <span data-ttu-id="ac8b4-113">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="ac8b4-113">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="ac8b4-114">확장 버전이 새 부 버전으로 자동 업데이트 되어야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ac8b4-114">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="ac8b4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac8b4-115">-DefaultProfile</span></span>
<span data-ttu-id="ac8b4-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ac8b4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac8b4-117">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="ac8b4-117">-ForceUpdateTag</span></span>
<span data-ttu-id="ac8b4-118">값이 제공 되 고 이전 값과 다른 경우 확장 구성이 변경 되지 않았더라도 확장 처리기가 강제로 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ac8b4-118">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="ac8b4-119">-이름</span><span class="sxs-lookup"><span data-stu-id="ac8b4-119">-Name</span></span>
<span data-ttu-id="ac8b4-120">이 cmdlet이 추가 하는 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac8b4-120">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="ac8b4-121">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="ac8b4-121">-ProtectedSetting</span></span>
<span data-ttu-id="ac8b4-122">확장에 대 한 개인 구성을 문자열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac8b4-122">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="ac8b4-123">이 cmdlet은 개인 구성을 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac8b4-123">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="ac8b4-124">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="ac8b4-124">-ProvisionAfterExtension</span></span>
<span data-ttu-id="ac8b4-125">이 확장을 프로 비전 해야 하는 확장명 이름 컬렉션입니다.</span><span class="sxs-lookup"><span data-stu-id="ac8b4-125">Collection of extension names after which this extension needs to be provisioned.</span></span>

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

### <span data-ttu-id="ac8b4-126">-Publisher</span><span class="sxs-lookup"><span data-stu-id="ac8b4-126">-Publisher</span></span>
<span data-ttu-id="ac8b4-127">확장 게시자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac8b4-127">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="ac8b4-128">게시자는 확장명을 등록할 때 이름을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac8b4-128">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="ac8b4-129">이는 [AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet을 사용 하 여 게시자를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac8b4-129">This can use the [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="ac8b4-130">-설정</span><span class="sxs-lookup"><span data-stu-id="ac8b4-130">-Setting</span></span>
<span data-ttu-id="ac8b4-131">공용 구성을 해당 확장명에 대 한 문자열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac8b4-131">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="ac8b4-132">이 cmdlet은 공용 구성을 암호화 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ac8b4-132">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="ac8b4-133">-Type</span><span class="sxs-lookup"><span data-stu-id="ac8b4-133">-Type</span></span>
<span data-ttu-id="ac8b4-134">확장명 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac8b4-134">Specifies the extension type.</span></span>
<span data-ttu-id="ac8b4-135">[AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet을 사용 하 여 확장 형식을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac8b4-135">You can use the [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="ac8b4-136">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="ac8b4-136">-TypeHandlerVersion</span></span>
<span data-ttu-id="ac8b4-137">이 가상 컴퓨터에 사용할 확장 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac8b4-137">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="ac8b4-138">[AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet을 사용 하 여 확장 버전을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac8b4-138">You can use the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="ac8b4-139">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ac8b4-139">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="ac8b4-140">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac8b4-140">Specify the VMSS object.</span></span>
<span data-ttu-id="ac8b4-141">[New-AzVmssConfig](./New-AzVmssConfig.md) 를 사용 하 여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac8b4-141">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="ac8b4-142">-확인</span><span class="sxs-lookup"><span data-stu-id="ac8b4-142">-Confirm</span></span>
<span data-ttu-id="ac8b4-143">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac8b4-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac8b4-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac8b4-144">-WhatIf</span></span>
<span data-ttu-id="ac8b4-145">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ac8b4-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ac8b4-146">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ac8b4-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac8b4-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac8b4-147">CommonParameters</span></span>
<span data-ttu-id="ac8b4-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac8b4-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac8b4-149">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ac8b4-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac8b4-150">입력</span><span class="sxs-lookup"><span data-stu-id="ac8b4-150">INPUTS</span></span>

### <span data-ttu-id="ac8b4-151">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="ac8b4-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="ac8b4-152">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ac8b4-152">System.String</span></span>

### <span data-ttu-id="ac8b4-153">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ac8b4-153">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ac8b4-154">System. 개체</span><span class="sxs-lookup"><span data-stu-id="ac8b4-154">System.Object</span></span>

## <span data-ttu-id="ac8b4-155">출력</span><span class="sxs-lookup"><span data-stu-id="ac8b4-155">OUTPUTS</span></span>

### <span data-ttu-id="ac8b4-156">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="ac8b4-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="ac8b4-157">상속자</span><span class="sxs-lookup"><span data-stu-id="ac8b4-157">NOTES</span></span>

## <span data-ttu-id="ac8b4-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ac8b4-158">RELATED LINKS</span></span>

[<span data-ttu-id="ac8b4-159">제거-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="ac8b4-159">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)

[<span data-ttu-id="ac8b4-160">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="ac8b4-160">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="ac8b4-161">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="ac8b4-161">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="ac8b4-162">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="ac8b4-162">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="ac8b4-163">새로운 AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="ac8b4-163">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
