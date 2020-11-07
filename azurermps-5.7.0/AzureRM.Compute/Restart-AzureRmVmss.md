---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVmss.md
ms.openlocfilehash: 1bc6b2b3ceb7ed7f991c92e4b8f8b034c78d54d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536072"
---
# <span data-ttu-id="3052d-101">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3052d-101">Restart-AzureRmVmss</span></span>

## <span data-ttu-id="3052d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3052d-102">SYNOPSIS</span></span>
<span data-ttu-id="3052d-103">Vmss 또는 VMSS 내의 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="3052d-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3052d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3052d-104">SYNTAX</span></span>

```
Restart-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3052d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3052d-105">DESCRIPTION</span></span>
<span data-ttu-id="3052d-106">**AzureRmVmss** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합)를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="3052d-106">The **Restart-AzureRmVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="3052d-107">이 cmdlet은 *InstanceId* 매개 변수를 사용 하 여 vmss 내부의 특정 가상 컴퓨터를 다시 시작 하는 데도 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3052d-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="3052d-108">예제의</span><span class="sxs-lookup"><span data-stu-id="3052d-108">EXAMPLES</span></span>

### <span data-ttu-id="3052d-109">예제 1: VMSS 다시 시작</span><span class="sxs-lookup"><span data-stu-id="3052d-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="3052d-110">이 명령은 Group001 이라는 리소스 그룹에 속하는 VMSS001 라는 VMSS를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="3052d-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="3052d-111">예제 2: VMSS 내에서 특정 가상 컴퓨터 다시 시작</span><span class="sxs-lookup"><span data-stu-id="3052d-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="3052d-112">이 명령은 Group001 이라는 리소스 그룹에 속하는 VMSS 인 VMSS001 이라는 인스턴스 ID가 1 인 가상 컴퓨터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="3052d-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="3052d-113">변수</span><span class="sxs-lookup"><span data-stu-id="3052d-113">PARAMETERS</span></span>

### <span data-ttu-id="3052d-114">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="3052d-114">-InstanceId</span></span>
<span data-ttu-id="3052d-115">다시 시작 해야 하는 인스턴스의 ID를 문자열 배열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3052d-115">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3052d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3052d-116">-ResourceGroupName</span></span>
<span data-ttu-id="3052d-117">VMSS의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3052d-117">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="3052d-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="3052d-118">-VMScaleSetName</span></span>
<span data-ttu-id="3052d-119">이 cmdlet이 다시 시작 하는 VMSS의 이름을 종류에 게 합니다.</span><span class="sxs-lookup"><span data-stu-id="3052d-119">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="3052d-120">-확인</span><span class="sxs-lookup"><span data-stu-id="3052d-120">-Confirm</span></span>
<span data-ttu-id="3052d-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3052d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3052d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3052d-122">-WhatIf</span></span>
<span data-ttu-id="3052d-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3052d-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3052d-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3052d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3052d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3052d-125">CommonParameters</span></span>
<span data-ttu-id="3052d-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3052d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3052d-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3052d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3052d-128">입력</span><span class="sxs-lookup"><span data-stu-id="3052d-128">INPUTS</span></span>

### <span data-ttu-id="3052d-129">않아야</span><span class="sxs-lookup"><span data-stu-id="3052d-129">None</span></span>
<span data-ttu-id="3052d-130">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3052d-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3052d-131">출력</span><span class="sxs-lookup"><span data-stu-id="3052d-131">OUTPUTS</span></span>

###  
<span data-ttu-id="3052d-132">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3052d-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="3052d-133">상속자</span><span class="sxs-lookup"><span data-stu-id="3052d-133">NOTES</span></span>

## <span data-ttu-id="3052d-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3052d-134">RELATED LINKS</span></span>

[<span data-ttu-id="3052d-135">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3052d-135">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="3052d-136">새로운 AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3052d-136">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="3052d-137">제거-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3052d-137">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="3052d-138">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3052d-138">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="3052d-139">시작-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3052d-139">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="3052d-140">중지-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3052d-140">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="3052d-141">업데이트-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="3052d-141">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)

