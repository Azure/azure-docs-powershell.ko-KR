---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azalertstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
ms.openlocfilehash: 4ba238f75fa1e39daf2309a1ceda1aed323ff47d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327795"
---
# <span data-ttu-id="5d651-101">Update-AzAlertState</span><span class="sxs-lookup"><span data-stu-id="5d651-101">Update-AzAlertState</span></span>

## <span data-ttu-id="5d651-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d651-102">SYNOPSIS</span></span>
<span data-ttu-id="5d651-103">경고 상태 업데이트</span><span class="sxs-lookup"><span data-stu-id="5d651-103">Updates alert state</span></span>

## <span data-ttu-id="5d651-104">구문</span><span class="sxs-lookup"><span data-stu-id="5d651-104">SYNTAX</span></span>

### <span data-ttu-id="5d651-105">ByAlertId(기본값)</span><span class="sxs-lookup"><span data-stu-id="5d651-105">ByAlertId (Default)</span></span>
```
Update-AzAlertState -AlertId <String> -State <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d651-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5d651-106">ByInputObject</span></span>
```
Update-AzAlertState -State <String> -InputObject <PSAlert> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d651-107">설명</span><span class="sxs-lookup"><span data-stu-id="5d651-107">DESCRIPTION</span></span>
<span data-ttu-id="5d651-108">**Update-AzAlertState** cmdlet은 경고 상태를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5d651-108">**Update-AzAlertState** cmdlet updates alert state.</span></span>

## <span data-ttu-id="5d651-109">예제</span><span class="sxs-lookup"><span data-stu-id="5d651-109">EXAMPLES</span></span>

### <span data-ttu-id="5d651-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="5d651-110">Example 1</span></span>
```powershell
PS C:\> Update-AzAlertState -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Closed"
```

<span data-ttu-id="5d651-111">이 cmdlet은 경고 상태를 닫힌 상태로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5d651-111">This cmdlet updates the alert state to Closed.</span></span>

## <span data-ttu-id="5d651-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d651-112">PARAMETERS</span></span>

### <span data-ttu-id="5d651-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="5d651-113">-AlertId</span></span>
<span data-ttu-id="5d651-114">경고의 고유 식별자/경고의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="5d651-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAlertId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d651-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d651-115">-DefaultProfile</span></span>
<span data-ttu-id="5d651-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5d651-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d651-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d651-117">-InputObject</span></span>
<span data-ttu-id="5d651-118">파이프라인의 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="5d651-118">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d651-119">-State</span><span class="sxs-lookup"><span data-stu-id="5d651-119">-State</span></span>
<span data-ttu-id="5d651-120">업데이트된 경고 상태</span><span class="sxs-lookup"><span data-stu-id="5d651-120">Updated Alert State</span></span>

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

### <span data-ttu-id="5d651-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d651-121">-Confirm</span></span>
<span data-ttu-id="5d651-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d651-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d651-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d651-123">-WhatIf</span></span>
<span data-ttu-id="5d651-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5d651-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d651-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d651-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d651-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d651-126">CommonParameters</span></span>
<span data-ttu-id="5d651-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d651-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d651-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5d651-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d651-129">입력</span><span class="sxs-lookup"><span data-stu-id="5d651-129">INPUTS</span></span>

### <span data-ttu-id="5d651-130">없음</span><span class="sxs-lookup"><span data-stu-id="5d651-130">None</span></span>

## <span data-ttu-id="5d651-131">출력</span><span class="sxs-lookup"><span data-stu-id="5d651-131">OUTPUTS</span></span>

### <span data-ttu-id="5d651-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span><span class="sxs-lookup"><span data-stu-id="5d651-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="5d651-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5d651-133">NOTES</span></span>

## <span data-ttu-id="5d651-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5d651-134">RELATED LINKS</span></span>
