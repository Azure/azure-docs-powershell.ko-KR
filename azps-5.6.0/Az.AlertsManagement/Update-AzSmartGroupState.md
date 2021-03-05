---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/update-azsmartgroupstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
ms.openlocfilehash: 5f7e0f26461780b30dbe2b80c79bad8231590e7d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015579"
---
# <span data-ttu-id="ad9bc-101">Update-AzSmartGroupState</span><span class="sxs-lookup"><span data-stu-id="ad9bc-101">Update-AzSmartGroupState</span></span>

## <span data-ttu-id="ad9bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad9bc-102">SYNOPSIS</span></span>
<span data-ttu-id="ad9bc-103">스마트 그룹 상태 업데이트</span><span class="sxs-lookup"><span data-stu-id="ad9bc-103">Updates smart group state</span></span>

## <span data-ttu-id="ad9bc-104">구문</span><span class="sxs-lookup"><span data-stu-id="ad9bc-104">SYNTAX</span></span>

### <span data-ttu-id="ad9bc-105">BySmartGroupId(기본값)</span><span class="sxs-lookup"><span data-stu-id="ad9bc-105">BySmartGroupId (Default)</span></span>
```
Update-AzSmartGroupState -SmartGroupId <String> -State <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad9bc-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ad9bc-106">ByInputObject</span></span>
```
Update-AzSmartGroupState -State <String> -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad9bc-107">설명</span><span class="sxs-lookup"><span data-stu-id="ad9bc-107">DESCRIPTION</span></span>
<span data-ttu-id="ad9bc-108">**Update-AzSmartGroupState** cmdlet은 스마트 그룹 상태를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ad9bc-108">**Update-AzSmartGroupState** cmdlet updates smart group state.</span></span>

## <span data-ttu-id="ad9bc-109">예제</span><span class="sxs-lookup"><span data-stu-id="ad9bc-109">EXAMPLES</span></span>

### <span data-ttu-id="ad9bc-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="ad9bc-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSmartGroupState -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Acknowledged"
```

<span data-ttu-id="ad9bc-111">이 cmdlet은 스마트 그룹 상태를 Acknowleged로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ad9bc-111">This cmdlet updates the smart group state to Acknowleged.</span></span>

## <span data-ttu-id="ad9bc-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ad9bc-112">PARAMETERS</span></span>

### <span data-ttu-id="ad9bc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad9bc-113">-DefaultProfile</span></span>
<span data-ttu-id="ad9bc-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ad9bc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad9bc-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad9bc-115">-InputObject</span></span>
<span data-ttu-id="ad9bc-116">파이프라인의 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ad9bc-116">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad9bc-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="ad9bc-117">-SmartGroupId</span></span>
<span data-ttu-id="ad9bc-118">스마트 그룹의 고유 식별자/ 스마트 그룹의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="ad9bc-118">Unique Identifier of Smart Group / ResourceId of smart group.</span></span>

```yaml
Type: System.String
Parameter Sets: BySmartGroupId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad9bc-119">-State</span><span class="sxs-lookup"><span data-stu-id="ad9bc-119">-State</span></span>
<span data-ttu-id="ad9bc-120">업데이트된 스마트 그룹 상태</span><span class="sxs-lookup"><span data-stu-id="ad9bc-120">Updated Smart group State</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad9bc-121">-확인</span><span class="sxs-lookup"><span data-stu-id="ad9bc-121">-Confirm</span></span>
<span data-ttu-id="ad9bc-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ad9bc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad9bc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad9bc-123">-WhatIf</span></span>
<span data-ttu-id="ad9bc-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ad9bc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad9bc-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ad9bc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad9bc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad9bc-126">CommonParameters</span></span>
<span data-ttu-id="ad9bc-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ad9bc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad9bc-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad9bc-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad9bc-129">입력</span><span class="sxs-lookup"><span data-stu-id="ad9bc-129">INPUTS</span></span>

### <span data-ttu-id="ad9bc-130">없음</span><span class="sxs-lookup"><span data-stu-id="ad9bc-130">None</span></span>

## <span data-ttu-id="ad9bc-131">출력</span><span class="sxs-lookup"><span data-stu-id="ad9bc-131">OUTPUTS</span></span>

### <span data-ttu-id="ad9bc-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="ad9bc-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="ad9bc-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ad9bc-133">NOTES</span></span>

## <span data-ttu-id="ad9bc-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ad9bc-134">RELATED LINKS</span></span>
