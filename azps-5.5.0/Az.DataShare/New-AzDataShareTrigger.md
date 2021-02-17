---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
ms.openlocfilehash: e264dce6c99aaee7803881ab5eaa0ef529a53b48
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186092"
---
# <span data-ttu-id="758e9-101">New-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="758e9-101">New-AzDataShareTrigger</span></span>

## <span data-ttu-id="758e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="758e9-102">SYNOPSIS</span></span>
<span data-ttu-id="758e9-103">공유 구독에 대한 트리거를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="758e9-103">Creates a trigger for share subscription.</span></span>

## <span data-ttu-id="758e9-104">구문</span><span class="sxs-lookup"><span data-stu-id="758e9-104">SYNTAX</span></span>

```
New-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="758e9-105">설명</span><span class="sxs-lookup"><span data-stu-id="758e9-105">DESCRIPTION</span></span>
<span data-ttu-id="758e9-106">**New-AzDataShareTrigger** cmdlet은 Azure 데이터 공유 계정에서 지정된 반복 간격 및 동기화 시간의 공유 구독에 대한 트리거를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="758e9-106">The **New-AzDataShareTrigger** cmdlet creates a trigger for share subscription for the specified recurrence interval and synchronization time under azure data share account.</span></span>

## <span data-ttu-id="758e9-107">예제</span><span class="sxs-lookup"><span data-stu-id="758e9-107">EXAMPLES</span></span>

### <span data-ttu-id="758e9-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="758e9-108">Example 1</span></span>
```
PS C:\> New-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger" -RecurrenceInterval "Day" -SynchronizationTime "9:00"
CreatedAt           : 7/10/2019 12:16:34 AM
CreatedBy           : Ads test
ProvisioningState   : Succeeded
RecurrenceInterval  : Day
SynchronizationMode : Incremental
SynchronizationTime : 7/9/2019 9:00:00 AM
TriggerStatus       : Active
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/triggers/AdsTrigger
Name                : AdsTrigger
Type                : Microsoft.DataShare/Triggers
```

<span data-ttu-id="758e9-109">이 명령은 매일 recurrence 간격이 오전 9시인 공유 구독 AdsShareSubscription에 대한 새 트리거 AdsTrigger를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="758e9-109">This command creates a new trigger AdsTrigger for share subscription AdsShareSubscription with a daily recurrence interval of 9 am.</span></span>

## <span data-ttu-id="758e9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="758e9-110">PARAMETERS</span></span>

### <span data-ttu-id="758e9-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="758e9-111">-AccountName</span></span>
<span data-ttu-id="758e9-112">Azure 데이터 공유 계정 이름</span><span class="sxs-lookup"><span data-stu-id="758e9-112">Azure data share account name</span></span>

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

### <span data-ttu-id="758e9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="758e9-113">-AsJob</span></span>
<span data-ttu-id="758e9-114">{{AsJob 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="758e9-114">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="758e9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="758e9-115">-DefaultProfile</span></span>
<span data-ttu-id="758e9-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="758e9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="758e9-117">-Name</span><span class="sxs-lookup"><span data-stu-id="758e9-117">-Name</span></span>
<span data-ttu-id="758e9-118">Azure 데이터 공유 트리거 이름</span><span class="sxs-lookup"><span data-stu-id="758e9-118">Azure data share trigger name</span></span>

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

### <span data-ttu-id="758e9-119">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="758e9-119">-RecurrenceInterval</span></span>
<span data-ttu-id="758e9-120">트리거에 대한 반복 간격(일 또는 시간)</span><span class="sxs-lookup"><span data-stu-id="758e9-120">The recurrence interval for the trigger (Day or Hour)</span></span>

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

### <span data-ttu-id="758e9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="758e9-121">-ResourceGroupName</span></span>
<span data-ttu-id="758e9-122">Azure 데이터 공유 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="758e9-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="758e9-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="758e9-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="758e9-124">Azure 데이터 공유 구독 이름</span><span class="sxs-lookup"><span data-stu-id="758e9-124">Azure data share subscription name</span></span>

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

### <span data-ttu-id="758e9-125">-SynchronizationTime</span><span class="sxs-lookup"><span data-stu-id="758e9-125">-SynchronizationTime</span></span>
<span data-ttu-id="758e9-126">트리거에 대해 예약된 동기화의 시작 시간</span><span class="sxs-lookup"><span data-stu-id="758e9-126">The start time of the scheduled synchronization for the trigger</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="758e9-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="758e9-127">-Confirm</span></span>
<span data-ttu-id="758e9-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="758e9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="758e9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="758e9-129">-WhatIf</span></span>
<span data-ttu-id="758e9-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="758e9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="758e9-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="758e9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="758e9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="758e9-132">CommonParameters</span></span>
<span data-ttu-id="758e9-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="758e9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="758e9-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="758e9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="758e9-135">입력</span><span class="sxs-lookup"><span data-stu-id="758e9-135">INPUTS</span></span>

### <span data-ttu-id="758e9-136">없음</span><span class="sxs-lookup"><span data-stu-id="758e9-136">None</span></span>

## <span data-ttu-id="758e9-137">출력</span><span class="sxs-lookup"><span data-stu-id="758e9-137">OUTPUTS</span></span>

### <span data-ttu-id="758e9-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="758e9-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="758e9-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="758e9-139">NOTES</span></span>

## <span data-ttu-id="758e9-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="758e9-140">RELATED LINKS</span></span>
