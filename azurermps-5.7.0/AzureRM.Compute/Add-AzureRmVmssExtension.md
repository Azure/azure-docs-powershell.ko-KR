---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
ms.openlocfilehash: 20446fc7c93000b29680689001d9e3c40c4862e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525344"
---
# <span data-ttu-id="c25a9-101">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="c25a9-101">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="c25a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c25a9-102">SYNOPSIS</span></span>
<span data-ttu-id="c25a9-103">VMSS에 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c25a9-103">Adds an extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c25a9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c25a9-104">SYNTAX</span></span>

```
Add-AzureRmVmssExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c25a9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c25a9-105">DESCRIPTION</span></span>
<span data-ttu-id="c25a9-106">**추가-AzureRmVmssExtension** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합)에 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c25a9-106">The **Add-AzureRmVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="c25a9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c25a9-107">EXAMPLES</span></span>

### <span data-ttu-id="c25a9-108">예제 1: VMSS에 확장 추가</span><span class="sxs-lookup"><span data-stu-id="c25a9-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="c25a9-109">이 명령은 VMMS에 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c25a9-109">This command adds an extension to the VMMS.</span></span>

## <span data-ttu-id="c25a9-110">변수</span><span class="sxs-lookup"><span data-stu-id="c25a9-110">PARAMETERS</span></span>

### <span data-ttu-id="c25a9-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="c25a9-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="c25a9-112">확장 버전이 새 부 버전으로 자동 업데이트 되어야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c25a9-112">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="c25a9-113">-이름</span><span class="sxs-lookup"><span data-stu-id="c25a9-113">-Name</span></span>
<span data-ttu-id="c25a9-114">이 cmdlet이 추가 하는 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c25a9-114">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="c25a9-115">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="c25a9-115">-ProtectedSetting</span></span>
<span data-ttu-id="c25a9-116">확장에 대 한 개인 구성을 문자열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c25a9-116">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="c25a9-117">이 cmdlet은 개인 구성을 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="c25a9-117">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="c25a9-118">-Publisher</span><span class="sxs-lookup"><span data-stu-id="c25a9-118">-Publisher</span></span>
<span data-ttu-id="c25a9-119">확장 게시자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c25a9-119">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="c25a9-120">게시자는 확장명을 등록할 때 이름을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="c25a9-120">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="c25a9-121">이는 [AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) cmdlet을 사용 하 여 게시자를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c25a9-121">This can use the [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="c25a9-122">-설정</span><span class="sxs-lookup"><span data-stu-id="c25a9-122">-Setting</span></span>
<span data-ttu-id="c25a9-123">공용 구성을 해당 확장명에 대 한 문자열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c25a9-123">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="c25a9-124">이 cmdlet은 공용 구성을 암호화 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c25a9-124">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="c25a9-125">-Type</span><span class="sxs-lookup"><span data-stu-id="c25a9-125">-Type</span></span>
<span data-ttu-id="c25a9-126">확장명 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c25a9-126">Specifies the extension type.</span></span>
<span data-ttu-id="c25a9-127">[AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) cmdlet을 사용 하 여 확장 형식을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c25a9-127">You can use the [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="c25a9-128">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="c25a9-128">-TypeHandlerVersion</span></span>
<span data-ttu-id="c25a9-129">이 가상 컴퓨터에 사용할 확장 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c25a9-129">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="c25a9-130">[AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet을 사용 하 여 확장 버전을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c25a9-130">You can use the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="c25a9-131">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c25a9-131">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="c25a9-132">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c25a9-132">Specify the VMSS object.</span></span>
<span data-ttu-id="c25a9-133">[New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) 를 사용 하 여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c25a9-133">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c25a9-134">-확인</span><span class="sxs-lookup"><span data-stu-id="c25a9-134">-Confirm</span></span>
<span data-ttu-id="c25a9-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c25a9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c25a9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c25a9-136">-WhatIf</span></span>
<span data-ttu-id="c25a9-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c25a9-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c25a9-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c25a9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c25a9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c25a9-139">CommonParameters</span></span>
<span data-ttu-id="c25a9-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c25a9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c25a9-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c25a9-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c25a9-142">입력</span><span class="sxs-lookup"><span data-stu-id="c25a9-142">INPUTS</span></span>

### <span data-ttu-id="c25a9-143">않아야</span><span class="sxs-lookup"><span data-stu-id="c25a9-143">None</span></span>
<span data-ttu-id="c25a9-144">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c25a9-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c25a9-145">출력</span><span class="sxs-lookup"><span data-stu-id="c25a9-145">OUTPUTS</span></span>

###  
<span data-ttu-id="c25a9-146">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c25a9-146">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="c25a9-147">상속자</span><span class="sxs-lookup"><span data-stu-id="c25a9-147">NOTES</span></span>

## <span data-ttu-id="c25a9-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c25a9-148">RELATED LINKS</span></span>

[<span data-ttu-id="c25a9-149">제거-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="c25a9-149">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)

[<span data-ttu-id="c25a9-150">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="c25a9-150">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="c25a9-151">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="c25a9-151">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="c25a9-152">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="c25a9-152">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="c25a9-153">새로운 AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="c25a9-153">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
