---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzProximityPlacementGroup.md
ms.openlocfilehash: 88cdb68da94f84dc1af977ba5b12b5bfb4d73914
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697368"
---
# <span data-ttu-id="3e188-101">New-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="3e188-101">New-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="3e188-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e188-102">SYNOPSIS</span></span>
<span data-ttu-id="3e188-103">근접 배치 그룹 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3e188-103">Create Proximity Placement Group resource.</span></span>

## <span data-ttu-id="3e188-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3e188-104">SYNTAX</span></span>

```
New-AzProximityPlacementGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-ProximityPlacementGroupType <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e188-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3e188-105">DESCRIPTION</span></span>
<span data-ttu-id="3e188-106">이 cmdlet은 근접 배치 그룹 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3e188-106">This cmdlet will create Proximity Placement Group resource.</span></span>

## <span data-ttu-id="3e188-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3e188-107">EXAMPLES</span></span>

### <span data-ttu-id="3e188-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="3e188-108">Example 1</span></span>
```
PS C:\> New-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName -Location $location -Tag @{key1 = "val1"}

ResourceGroupName           : rg0
ProximityPlacementGroupType : Standard
Id                          : /subscriptions/5393f919-a68a-43d0-9063-4b2bda6bffdf/resourceGroups/rg0/providers/Microsoft.Compute/proximityPlacementGroups/ppg0
Name                        : ppg0
Type                        : Microsoft.Compute/proximityPlacementGroups
Location                    : westcentralus
Tags                        : {"key1":"val1"}
```

<span data-ttu-id="3e188-109">이 명령은 지정 된 위치에 근접 한 장소 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3e188-109">This command creates a proximity place group in the given location.</span></span>

## <span data-ttu-id="3e188-110">변수</span><span class="sxs-lookup"><span data-stu-id="3e188-110">PARAMETERS</span></span>

### <span data-ttu-id="3e188-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e188-111">-AsJob</span></span>
<span data-ttu-id="3e188-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3e188-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e188-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e188-113">-DefaultProfile</span></span>
<span data-ttu-id="3e188-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3e188-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e188-115">-위치</span><span class="sxs-lookup"><span data-stu-id="3e188-115">-Location</span></span>
<span data-ttu-id="3e188-116">리소스 위치</span><span class="sxs-lookup"><span data-stu-id="3e188-116">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e188-117">-이름</span><span class="sxs-lookup"><span data-stu-id="3e188-117">-Name</span></span>
<span data-ttu-id="3e188-118">근접 배치 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3e188-118">The name of the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProximityPlacementGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e188-119">-ProximityPlacementGroupType</span><span class="sxs-lookup"><span data-stu-id="3e188-119">-ProximityPlacementGroupType</span></span>
<span data-ttu-id="3e188-120">근접 배치 그룹의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e188-120">Specifies the type of the proximity placement group.</span></span>  <span data-ttu-id="3e188-121">사용할 수 있는 값은 다음과 같습니다. 표준 또는 Ultra</span><span class="sxs-lookup"><span data-stu-id="3e188-121">Possible values are: Standard or Ultra</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e188-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e188-122">-ResourceGroupName</span></span>
<span data-ttu-id="3e188-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3e188-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e188-124">태그</span><span class="sxs-lookup"><span data-stu-id="3e188-124">-Tag</span></span>
<span data-ttu-id="3e188-125">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="3e188-125">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e188-126">-확인</span><span class="sxs-lookup"><span data-stu-id="3e188-126">-Confirm</span></span>
<span data-ttu-id="3e188-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e188-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e188-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e188-128">-WhatIf</span></span>
<span data-ttu-id="3e188-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3e188-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e188-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3e188-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e188-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e188-131">CommonParameters</span></span>
<span data-ttu-id="3e188-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e188-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e188-133">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3e188-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e188-134">입력</span><span class="sxs-lookup"><span data-stu-id="3e188-134">INPUTS</span></span>

### <span data-ttu-id="3e188-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3e188-135">System.String</span></span>

## <span data-ttu-id="3e188-136">출력</span><span class="sxs-lookup"><span data-stu-id="3e188-136">OUTPUTS</span></span>

### <span data-ttu-id="3e188-137">PSProximityPlacementGroup의. m a.</span><span class="sxs-lookup"><span data-stu-id="3e188-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="3e188-138">상속자</span><span class="sxs-lookup"><span data-stu-id="3e188-138">NOTES</span></span>

## <span data-ttu-id="3e188-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3e188-139">RELATED LINKS</span></span>
