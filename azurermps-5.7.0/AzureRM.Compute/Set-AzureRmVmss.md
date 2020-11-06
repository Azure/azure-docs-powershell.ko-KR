---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmss.md
ms.openlocfilehash: e3b053d4e8e9ccf9c68d8eb5fabe479f7f58ced1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531090"
---
# <span data-ttu-id="e9397-101">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e9397-101">Set-AzureRmVmss</span></span>

## <span data-ttu-id="e9397-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9397-102">SYNOPSIS</span></span>
<span data-ttu-id="e9397-103">지정 된 VMSS에 대 한 특정 작업을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9397-103">Sets specific actions on a specified VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9397-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e9397-104">SYNTAX</span></span>

### <span data-ttu-id="e9397-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="e9397-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Reimage] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e9397-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="e9397-106">FriendMethod</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-ReimageAll] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e9397-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e9397-107">DESCRIPTION</span></span>
<span data-ttu-id="e9397-108">**AzureRmVmss** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합)에 대 한 특정 작업을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9397-108">The **Set-AzureRmVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="e9397-109">이 cmdlet이 지 원하는 유일한 작업은 이미지로 서,</span><span class="sxs-lookup"><span data-stu-id="e9397-109">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="e9397-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e9397-110">EXAMPLES</span></span>

### <span data-ttu-id="e9397-111">예제 1: VMSS를 이미지로</span><span class="sxs-lookup"><span data-stu-id="e9397-111">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzureRmVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="e9397-112">이 명령은 ContosoGroup 이라는 리소스 그룹에 속하는 ContosoVMSS 이라는 VMSS를 다시 이미지로 이미지 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9397-112">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="e9397-113">변수</span><span class="sxs-lookup"><span data-stu-id="e9397-113">PARAMETERS</span></span>

### <span data-ttu-id="e9397-114">-이미지로</span><span class="sxs-lookup"><span data-stu-id="e9397-114">-Reimage</span></span>
<span data-ttu-id="e9397-115">Cmdlet이 VMSS를 다시 이미지로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9397-115">Indicates that the cmdlet reimages the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9397-116">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="e9397-116">-ReimageAll</span></span>
<span data-ttu-id="e9397-117">Cmdlet이 VMSS의 모든 디스크를 다시 이미지로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9397-117">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9397-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9397-118">-ResourceGroupName</span></span>
<span data-ttu-id="e9397-119">VMSS의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9397-119">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9397-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e9397-120">-VMScaleSetName</span></span>
<span data-ttu-id="e9397-121">이 cmdlet이 동작을 설정 하는 VMSS의 이름을 종류에 따라 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9397-121">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9397-122">-확인</span><span class="sxs-lookup"><span data-stu-id="e9397-122">-Confirm</span></span>
<span data-ttu-id="e9397-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9397-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9397-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9397-124">-WhatIf</span></span>
<span data-ttu-id="e9397-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e9397-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e9397-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e9397-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9397-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9397-127">CommonParameters</span></span>
<span data-ttu-id="e9397-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e9397-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9397-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9397-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9397-130">입력</span><span class="sxs-lookup"><span data-stu-id="e9397-130">INPUTS</span></span>

### <span data-ttu-id="e9397-131">않아야</span><span class="sxs-lookup"><span data-stu-id="e9397-131">None</span></span>
<span data-ttu-id="e9397-132">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e9397-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e9397-133">출력</span><span class="sxs-lookup"><span data-stu-id="e9397-133">OUTPUTS</span></span>

### <span data-ttu-id="e9397-134">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e9397-134">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="e9397-135">상속자</span><span class="sxs-lookup"><span data-stu-id="e9397-135">NOTES</span></span>

## <span data-ttu-id="e9397-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e9397-136">RELATED LINKS</span></span>

[<span data-ttu-id="e9397-137">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e9397-137">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="e9397-138">새로운 AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e9397-138">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="e9397-139">제거-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e9397-139">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="e9397-140">다시 시작-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e9397-140">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="e9397-141">시작-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e9397-141">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="e9397-142">중지-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e9397-142">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="e9397-143">업데이트-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e9397-143">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


