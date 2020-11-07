---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssextension
schema: 2.0.0
ms.openlocfilehash: f69b8901b2bc2c07bdf158da4c92deba0330109d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880573"
---
# <span data-ttu-id="f3417-101">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="f3417-101">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="f3417-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3417-102">SYNOPSIS</span></span>
<span data-ttu-id="f3417-103">VMSS에 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3417-103">Adds an extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3417-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f3417-104">SYNTAX</span></span>

```
Add-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f3417-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f3417-105">DESCRIPTION</span></span>
<span data-ttu-id="f3417-106">**추가-AzureRmVmssExtension** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합)에 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3417-106">The **Add-AzureRmVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="f3417-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f3417-107">EXAMPLES</span></span>

### <span data-ttu-id="f3417-108">예제 1: VMSS에 확장 추가</span><span class="sxs-lookup"><span data-stu-id="f3417-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="f3417-109">이 명령은 VMMS에 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3417-109">This command adds an extension to the VMMS.</span></span>

## <span data-ttu-id="f3417-110">변수</span><span class="sxs-lookup"><span data-stu-id="f3417-110">PARAMETERS</span></span>

### <span data-ttu-id="f3417-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="f3417-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="f3417-112">확장 버전이 새 부 버전으로 자동 업데이트 되어야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f3417-112">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="f3417-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3417-113">-DefaultProfile</span></span>
<span data-ttu-id="f3417-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f3417-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3417-115">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="f3417-115">-ForceUpdateTag</span></span>
<span data-ttu-id="f3417-116">값이 제공 되 고 이전 값과 다른 경우 확장 구성이 변경 되지 않았더라도 확장 처리기가 강제로 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f3417-116">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="f3417-117">-이름</span><span class="sxs-lookup"><span data-stu-id="f3417-117">-Name</span></span>
<span data-ttu-id="f3417-118">이 cmdlet이 추가 하는 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3417-118">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="f3417-119">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="f3417-119">-ProtectedSetting</span></span>
<span data-ttu-id="f3417-120">확장에 대 한 개인 구성을 문자열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3417-120">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="f3417-121">이 cmdlet은 개인 구성을 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3417-121">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="f3417-122">-Publisher</span><span class="sxs-lookup"><span data-stu-id="f3417-122">-Publisher</span></span>
<span data-ttu-id="f3417-123">확장 게시자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3417-123">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="f3417-124">게시자는 확장명을 등록할 때 이름을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3417-124">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="f3417-125">이는 [AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) cmdlet을 사용 하 여 게시자를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3417-125">This can use the [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="f3417-126">-설정</span><span class="sxs-lookup"><span data-stu-id="f3417-126">-Setting</span></span>
<span data-ttu-id="f3417-127">공용 구성을 해당 확장명에 대 한 문자열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3417-127">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="f3417-128">이 cmdlet은 공용 구성을 암호화 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f3417-128">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="f3417-129">-Type</span><span class="sxs-lookup"><span data-stu-id="f3417-129">-Type</span></span>
<span data-ttu-id="f3417-130">확장명 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3417-130">Specifies the extension type.</span></span>
<span data-ttu-id="f3417-131">[AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) cmdlet을 사용 하 여 확장 형식을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3417-131">You can use the [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="f3417-132">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="f3417-132">-TypeHandlerVersion</span></span>
<span data-ttu-id="f3417-133">이 가상 컴퓨터에 사용할 확장 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3417-133">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="f3417-134">[AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet을 사용 하 여 확장 버전을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3417-134">You can use the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="f3417-135">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f3417-135">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="f3417-136">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3417-136">Specify the VMSS object.</span></span>
<span data-ttu-id="f3417-137">[New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) 를 사용 하 여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3417-137">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="f3417-138">-확인</span><span class="sxs-lookup"><span data-stu-id="f3417-138">-Confirm</span></span>
<span data-ttu-id="f3417-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3417-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3417-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3417-140">-WhatIf</span></span>
<span data-ttu-id="f3417-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f3417-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3417-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f3417-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3417-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3417-143">CommonParameters</span></span>
<span data-ttu-id="f3417-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3417-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3417-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3417-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3417-146">입력</span><span class="sxs-lookup"><span data-stu-id="f3417-146">INPUTS</span></span>

### <span data-ttu-id="f3417-147">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f3417-147">VirtualMachineScaleSet</span></span>
<span data-ttu-id="f3417-148">' VirtualMachineScaleSet ' 매개 변수는 파이프라인에서 ' VirtualMachineScaleSet ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3417-148">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="f3417-149">출력</span><span class="sxs-lookup"><span data-stu-id="f3417-149">OUTPUTS</span></span>

###  
<span data-ttu-id="f3417-150">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f3417-150">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="f3417-151">상속자</span><span class="sxs-lookup"><span data-stu-id="f3417-151">NOTES</span></span>

## <span data-ttu-id="f3417-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f3417-152">RELATED LINKS</span></span>

[<span data-ttu-id="f3417-153">제거-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="f3417-153">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)

[<span data-ttu-id="f3417-154">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="f3417-154">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="f3417-155">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="f3417-155">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="f3417-156">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="f3417-156">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="f3417-157">새로운 AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="f3417-157">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
