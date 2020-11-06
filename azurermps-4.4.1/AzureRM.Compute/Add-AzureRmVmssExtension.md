---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
ms.openlocfilehash: fbf9d8c38c10465c565e40a284171b3232ba2949
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534159"
---
# <span data-ttu-id="b082f-101">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="b082f-101">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="b082f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b082f-102">SYNOPSIS</span></span>
<span data-ttu-id="b082f-103">VMSS에 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b082f-103">Adds an extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b082f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b082f-104">SYNTAX</span></span>

```
Add-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b082f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b082f-105">DESCRIPTION</span></span>
<span data-ttu-id="b082f-106">**추가-AzureRmVmssExtension** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합)에 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b082f-106">The **Add-AzureRmVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="b082f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b082f-107">EXAMPLES</span></span>

### <span data-ttu-id="b082f-108">예제 1: VMSS에 확장 추가</span><span class="sxs-lookup"><span data-stu-id="b082f-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="b082f-109">이 명령은 VMMS에 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b082f-109">This command adds an extension to the VMMS.</span></span>

## <span data-ttu-id="b082f-110">변수</span><span class="sxs-lookup"><span data-stu-id="b082f-110">PARAMETERS</span></span>

### <span data-ttu-id="b082f-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="b082f-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="b082f-112">확장 버전이 새 부 버전으로 자동 업데이트 되어야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b082f-112">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="b082f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b082f-113">-DefaultProfile</span></span>
<span data-ttu-id="b082f-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b082f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b082f-115">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="b082f-115">-ForceUpdateTag</span></span>
<span data-ttu-id="b082f-116">값이 제공 되 고 이전 값과 다른 경우 확장 구성이 변경 되지 않았더라도 확장 처리기가 강제로 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b082f-116">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="b082f-117">-이름</span><span class="sxs-lookup"><span data-stu-id="b082f-117">-Name</span></span>
<span data-ttu-id="b082f-118">이 cmdlet이 추가 하는 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b082f-118">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="b082f-119">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="b082f-119">-ProtectedSetting</span></span>
<span data-ttu-id="b082f-120">확장에 대 한 개인 구성을 문자열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b082f-120">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="b082f-121">이 cmdlet은 개인 구성을 암호화 합니다.</span><span class="sxs-lookup"><span data-stu-id="b082f-121">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="b082f-122">-Publisher</span><span class="sxs-lookup"><span data-stu-id="b082f-122">-Publisher</span></span>
<span data-ttu-id="b082f-123">확장 게시자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b082f-123">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="b082f-124">게시자는 확장명을 등록할 때 이름을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="b082f-124">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="b082f-125">이는 [AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) cmdlet을 사용 하 여 게시자를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b082f-125">This can use the [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="b082f-126">-설정</span><span class="sxs-lookup"><span data-stu-id="b082f-126">-Setting</span></span>
<span data-ttu-id="b082f-127">공용 구성을 해당 확장명에 대 한 문자열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b082f-127">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="b082f-128">이 cmdlet은 공용 구성을 암호화 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b082f-128">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="b082f-129">-Type</span><span class="sxs-lookup"><span data-stu-id="b082f-129">-Type</span></span>
<span data-ttu-id="b082f-130">확장명 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b082f-130">Specifies the extension type.</span></span>
<span data-ttu-id="b082f-131">[AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) cmdlet을 사용 하 여 확장 형식을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b082f-131">You can use the [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="b082f-132">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="b082f-132">-TypeHandlerVersion</span></span>
<span data-ttu-id="b082f-133">이 가상 컴퓨터에 사용할 확장 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b082f-133">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="b082f-134">[AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet을 사용 하 여 확장 버전을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b082f-134">You can use the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="b082f-135">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b082f-135">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="b082f-136">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b082f-136">Specify the VMSS object.</span></span>
<span data-ttu-id="b082f-137">[New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) 를 사용 하 여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b082f-137">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="b082f-138">-확인</span><span class="sxs-lookup"><span data-stu-id="b082f-138">-Confirm</span></span>
<span data-ttu-id="b082f-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b082f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b082f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b082f-140">-WhatIf</span></span>
<span data-ttu-id="b082f-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b082f-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b082f-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b082f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b082f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b082f-143">CommonParameters</span></span>
<span data-ttu-id="b082f-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b082f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b082f-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b082f-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b082f-146">입력</span><span class="sxs-lookup"><span data-stu-id="b082f-146">INPUTS</span></span>

## <span data-ttu-id="b082f-147">출력</span><span class="sxs-lookup"><span data-stu-id="b082f-147">OUTPUTS</span></span>

###  
<span data-ttu-id="b082f-148">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b082f-148">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="b082f-149">상속자</span><span class="sxs-lookup"><span data-stu-id="b082f-149">NOTES</span></span>

## <span data-ttu-id="b082f-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b082f-150">RELATED LINKS</span></span>

[<span data-ttu-id="b082f-151">제거-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="b082f-151">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)

[<span data-ttu-id="b082f-152">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="b082f-152">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="b082f-153">Get-AzureRmVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="b082f-153">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="b082f-154">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="b082f-154">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="b082f-155">새로운 AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="b082f-155">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
