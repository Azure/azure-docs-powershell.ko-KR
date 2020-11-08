---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: f3f38feff8b6d855121a6772cfb56ef0b57cebfd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034198"
---
# <span data-ttu-id="3ca54-101">Remove-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="3ca54-101">Remove-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="3ca54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ca54-102">SYNOPSIS</span></span>
<span data-ttu-id="3ca54-103">대역폭 일정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca54-103">Removes a Bandwidth Schedule.</span></span>

## <span data-ttu-id="3ca54-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3ca54-104">SYNTAX</span></span>

### <span data-ttu-id="3ca54-105">DeleteByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="3ca54-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ca54-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ca54-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeBandwidthSchedule -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ca54-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ca54-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ca54-108">설명은</span><span class="sxs-lookup"><span data-stu-id="3ca54-108">DESCRIPTION</span></span>
<span data-ttu-id="3ca54-109">**AzStackEdgeBandwidthSchedule** Cmdlet은 스택 경계 장치에 대 한 대역폭 일정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca54-109">The **Remove-AzStackEdgeBandwidthSchedule** cmdlet removes the Bandwidth schedule for a Stack Edge device.</span></span> 

## <span data-ttu-id="3ca54-110">예제의</span><span class="sxs-lookup"><span data-stu-id="3ca54-110">EXAMPLES</span></span>

### <span data-ttu-id="3ca54-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="3ca54-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule
```

## <span data-ttu-id="3ca54-112">변수</span><span class="sxs-lookup"><span data-stu-id="3ca54-112">PARAMETERS</span></span>

### <span data-ttu-id="3ca54-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ca54-113">-AsJob</span></span>
<span data-ttu-id="3ca54-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3ca54-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3ca54-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ca54-115">-DefaultProfile</span></span>
<span data-ttu-id="3ca54-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3ca54-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ca54-117">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="3ca54-117">-DeviceName</span></span>
<span data-ttu-id="3ca54-118">장치 이름</span><span class="sxs-lookup"><span data-stu-id="3ca54-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ca54-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ca54-119">-InputObject</span></span>
<span data-ttu-id="3ca54-120">입력 개체</span><span class="sxs-lookup"><span data-stu-id="3ca54-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: BandwidthSchedule

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ca54-121">-이름</span><span class="sxs-lookup"><span data-stu-id="3ca54-121">-Name</span></span>
<span data-ttu-id="3ca54-122">자원 이름</span><span class="sxs-lookup"><span data-stu-id="3ca54-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ca54-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ca54-123">-PassThru</span></span>
<span data-ttu-id="3ca54-124">성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca54-124">returns true if successful</span></span>

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

### <span data-ttu-id="3ca54-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ca54-125">-ResourceGroupName</span></span>
<span data-ttu-id="3ca54-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="3ca54-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ca54-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ca54-127">-ResourceId</span></span>
<span data-ttu-id="3ca54-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ca54-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ca54-129">-확인</span><span class="sxs-lookup"><span data-stu-id="3ca54-129">-Confirm</span></span>
<span data-ttu-id="3ca54-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca54-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ca54-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ca54-131">-WhatIf</span></span>
<span data-ttu-id="3ca54-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3ca54-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3ca54-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3ca54-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ca54-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ca54-134">CommonParameters</span></span>
<span data-ttu-id="3ca54-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ca54-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ca54-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3ca54-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ca54-137">입력</span><span class="sxs-lookup"><span data-stu-id="3ca54-137">INPUTS</span></span>

### <span data-ttu-id="3ca54-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3ca54-138">System.String</span></span>

### <span data-ttu-id="3ca54-139">StackEdge. PSStackEdgeBandWidthSchedule에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="3ca54-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="3ca54-140">출력</span><span class="sxs-lookup"><span data-stu-id="3ca54-140">OUTPUTS</span></span>

### <span data-ttu-id="3ca54-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="3ca54-141">System.Boolean</span></span>

## <span data-ttu-id="3ca54-142">상속자</span><span class="sxs-lookup"><span data-stu-id="3ca54-142">NOTES</span></span>

## <span data-ttu-id="3ca54-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3ca54-143">RELATED LINKS</span></span>
