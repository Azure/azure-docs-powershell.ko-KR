---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Disable-AzIotSecurityAnalyticsAggregatedAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
ms.openlocfilehash: 3747109d13fd4224b0f86bc5ecf2992ed4229487
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214000"
---
# <span data-ttu-id="76508-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="76508-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span></span>

## <span data-ttu-id="76508-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76508-102">SYNOPSIS</span></span>
<span data-ttu-id="76508-103">Iot 집계 된 알림 해제</span><span class="sxs-lookup"><span data-stu-id="76508-103">Dismiss Iot aggregated alert</span></span>

## <span data-ttu-id="76508-104">구문과</span><span class="sxs-lookup"><span data-stu-id="76508-104">SYNTAX</span></span>

### <span data-ttu-id="76508-105">솔루션 Levelresource (기본값)</span><span class="sxs-lookup"><span data-stu-id="76508-105">SolutionLevelResource (Default)</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76508-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="76508-106">InputObject</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -InputObject <PSIoTSecurityAggregatedAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76508-107">리소스</span><span class="sxs-lookup"><span data-stu-id="76508-107">ResourceId</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76508-108">설명은</span><span class="sxs-lookup"><span data-stu-id="76508-108">DESCRIPTION</span></span>
<span data-ttu-id="76508-109">Disable-AzIotSecurityAnalyticsAggregatedAlert cmdlet은 iot hub 장치에서 특정 aggraggalert을 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="76508-109">The Disable-AzIotSecurityAnalyticsAggregatedAlert cmdlet dismisses a specific aggragated alert on devices of iot hub.</span></span> <span data-ttu-id="76508-110">집계 된 경고의 이름은 '/'로 구분 된 경고 유형 및 alert aggragted date의 조합입니다.</span><span class="sxs-lookup"><span data-stu-id="76508-110">The name of the aggregated alerts is a combination of the alert type and the alert aggragted date, separated by '/'.</span></span>

## <span data-ttu-id="76508-111">예제의</span><span class="sxs-lookup"><span data-stu-id="76508-111">EXAMPLES</span></span>

### <span data-ttu-id="76508-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="76508-112">Example 1</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolutionName" -Name "IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="76508-113">집계 된 경고 "IoT_SucessfulLocalLogin/2020-03-15" (리소스 그룹 "MyResourceGroup"의 IoT 보안 솔루션 "MySolutionName"에서 "경고 유형 및 집계 날짜 조합)"을 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="76508-113">Dismiss aggregated alert "IoT_SucessfulLocalLogin/2020-03-15" (name combined from alert type and its aggregated date) from the IoT security solution "MySolutionName" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="76508-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="76508-114">Example 2</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="76508-115">리소스 Id "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-14"를 사용 하 여 집계 된 경고 해제</span><span class="sxs-lookup"><span data-stu-id="76508-115">Dismiss aggregated alert with resource Id "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"</span></span>

## <span data-ttu-id="76508-116">변수</span><span class="sxs-lookup"><span data-stu-id="76508-116">PARAMETERS</span></span>

### <span data-ttu-id="76508-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76508-117">-DefaultProfile</span></span>
<span data-ttu-id="76508-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="76508-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76508-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76508-119">-InputObject</span></span>
<span data-ttu-id="76508-120">입력 개체</span><span class="sxs-lookup"><span data-stu-id="76508-120">Input Object.</span></span>

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

### <span data-ttu-id="76508-121">-이름</span><span class="sxs-lookup"><span data-stu-id="76508-121">-Name</span></span>
<span data-ttu-id="76508-122">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="76508-122">Resource name.</span></span>

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

### <span data-ttu-id="76508-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76508-123">-PassThru</span></span>
<span data-ttu-id="76508-124">작업이 성공적으로 수행 되었는지 여부를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="76508-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="76508-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76508-125">-ResourceGroupName</span></span>
<span data-ttu-id="76508-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="76508-126">Resource group name.</span></span>

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

### <span data-ttu-id="76508-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76508-127">-ResourceId</span></span>
<span data-ttu-id="76508-128">명령을 호출 하려는 보안 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="76508-128">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="76508-129">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="76508-129">-SolutionName</span></span>
<span data-ttu-id="76508-130">솔루션 이름</span><span class="sxs-lookup"><span data-stu-id="76508-130">Solution name</span></span>

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

### <span data-ttu-id="76508-131">-확인</span><span class="sxs-lookup"><span data-stu-id="76508-131">-Confirm</span></span>
<span data-ttu-id="76508-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="76508-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76508-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76508-133">-WhatIf</span></span>
<span data-ttu-id="76508-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="76508-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76508-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76508-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76508-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76508-136">CommonParameters</span></span>
<span data-ttu-id="76508-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="76508-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76508-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="76508-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76508-139">입력</span><span class="sxs-lookup"><span data-stu-id="76508-139">INPUTS</span></span>

### <span data-ttu-id="76508-140">Microsoft. Azure. Irootsecurity솔루션 PSIoTSecurityAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="76508-140">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span></span>

### <span data-ttu-id="76508-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="76508-141">System.String</span></span>

## <span data-ttu-id="76508-142">출력</span><span class="sxs-lookup"><span data-stu-id="76508-142">OUTPUTS</span></span>

### <span data-ttu-id="76508-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="76508-143">System.Boolean</span></span>

## <span data-ttu-id="76508-144">상속자</span><span class="sxs-lookup"><span data-stu-id="76508-144">NOTES</span></span>

## <span data-ttu-id="76508-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="76508-145">RELATED LINKS</span></span>
