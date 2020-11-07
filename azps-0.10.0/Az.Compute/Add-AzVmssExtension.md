---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssExtension.md
ms.openlocfilehash: 97c8824bca395ddd8fb23ebb4750ab35931c5d51
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877118"
---
# <span data-ttu-id="e94a1-101">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="e94a1-101">Add-AzVmssExtension</span></span>

## <span data-ttu-id="e94a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e94a1-102">SYNOPSIS</span></span>
<span data-ttu-id="e94a1-103">VMSS에 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e94a1-103">Adds an extension to the VMSS.</span></span>

## <span data-ttu-id="e94a1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e94a1-104">SYNTAX</span></span>

```
Add-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e94a1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e94a1-105">DESCRIPTION</span></span>
<span data-ttu-id="e94a1-106">**추가-AzVmssExtension** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합)에 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e94a1-106">The **Add-AzVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="e94a1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e94a1-107">EXAMPLES</span></span>

### <span data-ttu-id="e94a1-108">예제 1: VMSS에 확장 추가</span><span class="sxs-lookup"><span data-stu-id="e94a1-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="e94a1-109">이 명령은 VMMS에 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e94a1-109">This command adds an extension to the VMMS.</span></span>

## <span data-ttu-id="e94a1-110">변수</span><span class="sxs-lookup"><span data-stu-id="e94a1-110">PARAMETERS</span></span>

### <span data-ttu-id="e94a1-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="e94a1-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="e94a1-112">확장 버전이 새 부 버전으로 자동 업데이트 되어야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e94a1-112">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e94a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e94a1-113">-DefaultProfile</span></span>
<span data-ttu-id="e94a1-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e94a1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94a1-115">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="e94a1-115">-ForceUpdateTag</span></span>
<span data-ttu-id="e94a1-116">값이 제공 되 고 이전 값과 다른 경우 확장 구성이 변경 되지 않았더라도 확장 처리기가 강제로 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e94a1-116">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e94a1-117">-이름</span><span class="sxs-lookup"><span data-stu-id="e94a1-117">-Name</span></span>
<span data-ttu-id="e94a1-118">이 cmdlet이 추가 하는 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e94a1-118">Specifies the name of the extension that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e94a1-119">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="e94a1-119">-ProtectedSetting</span></span>
<span data-ttu-id="e94a1-120">확장에 대 한 개인 구성을 문자열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e94a1-120">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="e94a1-121">이 cmdlet은 개인 구성을 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="e94a1-121">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e94a1-122">-Publisher</span><span class="sxs-lookup"><span data-stu-id="e94a1-122">-Publisher</span></span>
<span data-ttu-id="e94a1-123">확장 게시자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e94a1-123">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="e94a1-124">게시자는 확장명을 등록할 때 이름을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="e94a1-124">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="e94a1-125">이는 [AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet을 사용 하 여 게시자를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e94a1-125">This can use the [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet to get the publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e94a1-126">-설정</span><span class="sxs-lookup"><span data-stu-id="e94a1-126">-Setting</span></span>
<span data-ttu-id="e94a1-127">공용 구성을 해당 확장명에 대 한 문자열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e94a1-127">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="e94a1-128">이 cmdlet은 공용 구성을 암호화 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e94a1-128">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e94a1-129">-Type</span><span class="sxs-lookup"><span data-stu-id="e94a1-129">-Type</span></span>
<span data-ttu-id="e94a1-130">확장명 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e94a1-130">Specifies the extension type.</span></span>
<span data-ttu-id="e94a1-131">[AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet을 사용 하 여 확장 형식을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e94a1-131">You can use the [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e94a1-132">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="e94a1-132">-TypeHandlerVersion</span></span>
<span data-ttu-id="e94a1-133">이 가상 컴퓨터에 사용할 확장 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e94a1-133">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="e94a1-134">[AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet을 사용 하 여 확장 버전을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e94a1-134">You can use the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e94a1-135">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e94a1-135">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="e94a1-136">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e94a1-136">Specify the VMSS object.</span></span>
<span data-ttu-id="e94a1-137">[New-AzVmssConfig](./New-AzVmssConfig.md) 를 사용 하 여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e94a1-137">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e94a1-138">-확인</span><span class="sxs-lookup"><span data-stu-id="e94a1-138">-Confirm</span></span>
<span data-ttu-id="e94a1-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e94a1-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94a1-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e94a1-140">-WhatIf</span></span>
<span data-ttu-id="e94a1-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e94a1-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e94a1-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e94a1-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e94a1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e94a1-143">CommonParameters</span></span>
<span data-ttu-id="e94a1-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e94a1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e94a1-145">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e94a1-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e94a1-146">입력</span><span class="sxs-lookup"><span data-stu-id="e94a1-146">INPUTS</span></span>

### <span data-ttu-id="e94a1-147">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e94a1-147">VirtualMachineScaleSet</span></span>
<span data-ttu-id="e94a1-148">' VirtualMachineScaleSet ' 매개 변수는 파이프라인에서 ' VirtualMachineScaleSet ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e94a1-148">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="e94a1-149">출력</span><span class="sxs-lookup"><span data-stu-id="e94a1-149">OUTPUTS</span></span>

###  
<span data-ttu-id="e94a1-150">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e94a1-150">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="e94a1-151">상속자</span><span class="sxs-lookup"><span data-stu-id="e94a1-151">NOTES</span></span>

## <span data-ttu-id="e94a1-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e94a1-152">RELATED LINKS</span></span>

[<span data-ttu-id="e94a1-153">제거-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="e94a1-153">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)

[<span data-ttu-id="e94a1-154">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="e94a1-154">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="e94a1-155">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="e94a1-155">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="e94a1-156">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="e94a1-156">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="e94a1-157">새로운 AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="e94a1-157">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
