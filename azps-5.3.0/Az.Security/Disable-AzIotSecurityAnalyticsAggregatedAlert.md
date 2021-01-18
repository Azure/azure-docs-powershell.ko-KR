---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Disable-AzIotSecurityAnalyticsAggregatedAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
ms.openlocfilehash: 3747109d13fd4224b0f86bc5ecf2992ed4229487
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495050"
---
# <span data-ttu-id="3c621-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="3c621-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span></span>

## <span data-ttu-id="3c621-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c621-102">SYNOPSIS</span></span>
<span data-ttu-id="3c621-103">Ot 집계 경고를 해지합니다.</span><span class="sxs-lookup"><span data-stu-id="3c621-103">Dismiss Iot aggregated alert</span></span>

## <span data-ttu-id="3c621-104">구문</span><span class="sxs-lookup"><span data-stu-id="3c621-104">SYNTAX</span></span>

### <span data-ttu-id="3c621-105">SolutionLevelResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="3c621-105">SolutionLevelResource (Default)</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c621-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="3c621-106">InputObject</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -InputObject <PSIoTSecurityAggregatedAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c621-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c621-107">ResourceId</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c621-108">설명</span><span class="sxs-lookup"><span data-stu-id="3c621-108">DESCRIPTION</span></span>
<span data-ttu-id="3c621-109">이 Disable-AzIotSecurityAnalyticsAggregatedAlert cmdlet은 iot Hub의 디바이스에서 특정Ggated 경고를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="3c621-109">The Disable-AzIotSecurityAnalyticsAggregatedAlert cmdlet dismisses a specific aggragated alert on devices of iot hub.</span></span> <span data-ttu-id="3c621-110">집계된 경고의 이름은 경고 유형과 경고가 집계된 날짜를 '/'로 구분한 조합입니다.</span><span class="sxs-lookup"><span data-stu-id="3c621-110">The name of the aggregated alerts is a combination of the alert type and the alert aggragted date, separated by '/'.</span></span>

## <span data-ttu-id="3c621-111">예제</span><span class="sxs-lookup"><span data-stu-id="3c621-111">EXAMPLES</span></span>

### <span data-ttu-id="3c621-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="3c621-112">Example 1</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolutionName" -Name "IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="3c621-113">리소스 그룹 "MyResourceGroup"의 IoT 보안 솔루션 "MySolutionName"에서 집계된 경고 "IoT_SucessfulLocalLogin/2020-03-15"(경고 유형 및 집계 날짜에서 결합된 이름)를 해지합니다.</span><span class="sxs-lookup"><span data-stu-id="3c621-113">Dismiss aggregated alert "IoT_SucessfulLocalLogin/2020-03-15" (name combined from alert type and its aggregated date) from the IoT security solution "MySolutionName" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="3c621-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="3c621-114">Example 2</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="3c621-115">리소스 ID "/subscriptions/XXXXXXXX-XXXXX-XXXXXXXXXXX/resourceGroups/MyResource를 통해 집계된 경고를 해지합니다. providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"</span><span class="sxs-lookup"><span data-stu-id="3c621-115">Dismiss aggregated alert with resource Id "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"</span></span>

## <span data-ttu-id="3c621-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c621-116">PARAMETERS</span></span>

### <span data-ttu-id="3c621-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c621-117">-DefaultProfile</span></span>
<span data-ttu-id="3c621-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3c621-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c621-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c621-119">-InputObject</span></span>
<span data-ttu-id="3c621-120">입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3c621-120">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c621-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3c621-121">-Name</span></span>
<span data-ttu-id="3c621-122">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3c621-122">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c621-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c621-123">-PassThru</span></span>
<span data-ttu-id="3c621-124">작업이 성공한지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3c621-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="3c621-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c621-125">-ResourceGroupName</span></span>
<span data-ttu-id="3c621-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3c621-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c621-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c621-127">-ResourceId</span></span>
<span data-ttu-id="3c621-128">명령을 호출하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3c621-128">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c621-129">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="3c621-129">-SolutionName</span></span>
<span data-ttu-id="3c621-130">솔루션 이름</span><span class="sxs-lookup"><span data-stu-id="3c621-130">Solution name</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c621-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c621-131">-Confirm</span></span>
<span data-ttu-id="3c621-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3c621-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c621-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c621-133">-WhatIf</span></span>
<span data-ttu-id="3c621-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3c621-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c621-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3c621-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c621-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c621-136">CommonParameters</span></span>
<span data-ttu-id="3c621-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3c621-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c621-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3c621-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c621-139">입력</span><span class="sxs-lookup"><span data-stu-id="3c621-139">INPUTS</span></span>

### <span data-ttu-id="3c621-140">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="3c621-140">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span></span>

### <span data-ttu-id="3c621-141">System.String</span><span class="sxs-lookup"><span data-stu-id="3c621-141">System.String</span></span>

## <span data-ttu-id="3c621-142">출력</span><span class="sxs-lookup"><span data-stu-id="3c621-142">OUTPUTS</span></span>

### <span data-ttu-id="3c621-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3c621-143">System.Boolean</span></span>

## <span data-ttu-id="3c621-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3c621-144">NOTES</span></span>

## <span data-ttu-id="3c621-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3c621-145">RELATED LINKS</span></span>
