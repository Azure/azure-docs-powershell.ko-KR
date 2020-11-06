---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssExtension.md
ms.openlocfilehash: ad87e4e556263889de23640abad391ee28d7b397
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532472"
---
# <span data-ttu-id="388eb-101">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="388eb-101">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="388eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="388eb-102">SYNOPSIS</span></span>
<span data-ttu-id="388eb-103">VMSS에 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="388eb-103">Adds an extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="388eb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="388eb-104">SYNTAX</span></span>

```
Add-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="388eb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="388eb-105">DESCRIPTION</span></span>
<span data-ttu-id="388eb-106">**추가-AzureRmVmssExtension** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합)에 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="388eb-106">The **Add-AzureRmVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="388eb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="388eb-107">EXAMPLES</span></span>

### <span data-ttu-id="388eb-108">예제 1: VMSS에 확장 추가</span><span class="sxs-lookup"><span data-stu-id="388eb-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="388eb-109">이 명령은 VMSS에 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="388eb-109">This command adds an extension to the VMSS.</span></span>

### <span data-ttu-id="388eb-110">예제 2: 설정 및 보호 된 설정을 사용 하 여 VMSS에 확장 추가</span><span class="sxs-lookup"><span data-stu-id="388eb-110">Example 2: Add an extension to the VMSS with settings and protected settings</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};

PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName -Publisher $vmssPublisher  `
  -Type $vmssExtensionType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True  `
  -Setting $Settings -ProtectedSetting $ProtectedSettings
```

<span data-ttu-id="388eb-111">이 명령은 blob 저장소에 샘플 bash 스크립트를 사용 하 여 VMSS에 확장을 추가 하 고, 보호 된 설정의 설정 및 보안 액세스에서 blob 저장소 및 실행 명령의 url을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="388eb-111">This command adds an extension to the VMSS with a sample bash script on a blob storage, specify the url of blob storage and executable command in settings and security access in protected settings.</span></span> 

## <span data-ttu-id="388eb-112">변수</span><span class="sxs-lookup"><span data-stu-id="388eb-112">PARAMETERS</span></span>

### <span data-ttu-id="388eb-113">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="388eb-113">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="388eb-114">확장 버전이 새 부 버전으로 자동 업데이트 되어야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="388eb-114">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="388eb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="388eb-115">-DefaultProfile</span></span>
<span data-ttu-id="388eb-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="388eb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="388eb-117">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="388eb-117">-ForceUpdateTag</span></span>
<span data-ttu-id="388eb-118">값이 제공 되 고 이전 값과 다른 경우 확장 구성이 변경 되지 않았더라도 확장 처리기가 강제로 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="388eb-118">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="388eb-119">-이름</span><span class="sxs-lookup"><span data-stu-id="388eb-119">-Name</span></span>
<span data-ttu-id="388eb-120">이 cmdlet이 추가 하는 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="388eb-120">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="388eb-121">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="388eb-121">-ProtectedSetting</span></span>
<span data-ttu-id="388eb-122">확장에 대 한 개인 구성을 문자열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="388eb-122">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="388eb-123">이 cmdlet은 개인 구성을 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="388eb-123">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="388eb-124">-Publisher</span><span class="sxs-lookup"><span data-stu-id="388eb-124">-Publisher</span></span>
<span data-ttu-id="388eb-125">확장 게시자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="388eb-125">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="388eb-126">게시자는 확장명을 등록할 때 이름을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="388eb-126">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="388eb-127">이는 [AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) cmdlet을 사용 하 여 게시자를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="388eb-127">This can use the [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="388eb-128">-설정</span><span class="sxs-lookup"><span data-stu-id="388eb-128">-Setting</span></span>
<span data-ttu-id="388eb-129">공용 구성을 해당 확장명에 대 한 문자열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="388eb-129">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="388eb-130">이 cmdlet은 공용 구성을 암호화 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="388eb-130">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="388eb-131">-Type</span><span class="sxs-lookup"><span data-stu-id="388eb-131">-Type</span></span>
<span data-ttu-id="388eb-132">확장명 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="388eb-132">Specifies the extension type.</span></span>
<span data-ttu-id="388eb-133">[AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) cmdlet을 사용 하 여 확장 형식을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="388eb-133">You can use the [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="388eb-134">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="388eb-134">-TypeHandlerVersion</span></span>
<span data-ttu-id="388eb-135">이 가상 컴퓨터에 사용할 확장 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="388eb-135">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="388eb-136">[AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet을 사용 하 여 확장 버전을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="388eb-136">You can use the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="388eb-137">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="388eb-137">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="388eb-138">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="388eb-138">Specify the VMSS object.</span></span>
<span data-ttu-id="388eb-139">[New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) 를 사용 하 여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="388eb-139">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="388eb-140">-확인</span><span class="sxs-lookup"><span data-stu-id="388eb-140">-Confirm</span></span>
<span data-ttu-id="388eb-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="388eb-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="388eb-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="388eb-142">-WhatIf</span></span>
<span data-ttu-id="388eb-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="388eb-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="388eb-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="388eb-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="388eb-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="388eb-145">CommonParameters</span></span>
<span data-ttu-id="388eb-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="388eb-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="388eb-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="388eb-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="388eb-148">입력</span><span class="sxs-lookup"><span data-stu-id="388eb-148">INPUTS</span></span>

### <span data-ttu-id="388eb-149">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="388eb-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="388eb-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="388eb-150">System.String</span></span>

### <span data-ttu-id="388eb-151">시스템 Null 허용 ' 1 [[b77a5c561934e089] [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="388eb-151">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="388eb-152">System. 개체</span><span class="sxs-lookup"><span data-stu-id="388eb-152">System.Object</span></span>

## <span data-ttu-id="388eb-153">출력</span><span class="sxs-lookup"><span data-stu-id="388eb-153">OUTPUTS</span></span>

### <span data-ttu-id="388eb-154">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="388eb-154">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="388eb-155">상속자</span><span class="sxs-lookup"><span data-stu-id="388eb-155">NOTES</span></span>

## <span data-ttu-id="388eb-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="388eb-156">RELATED LINKS</span></span>

[<span data-ttu-id="388eb-157">제거-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="388eb-157">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)

[<span data-ttu-id="388eb-158">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="388eb-158">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="388eb-159">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="388eb-159">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="388eb-160">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="388eb-160">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="388eb-161">새로운 AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="388eb-161">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
