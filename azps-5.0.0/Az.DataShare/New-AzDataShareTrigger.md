---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
ms.openlocfilehash: e264dce6c99aaee7803881ab5eaa0ef529a53b48
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305174"
---
# <span data-ttu-id="f5999-101">New-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="f5999-101">New-AzDataShareTrigger</span></span>

## <span data-ttu-id="f5999-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5999-102">SYNOPSIS</span></span>
<span data-ttu-id="f5999-103">공유 구독에 대 한 트리거를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f5999-103">Creates a trigger for share subscription.</span></span>

## <span data-ttu-id="f5999-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f5999-104">SYNTAX</span></span>

```
New-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5999-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f5999-105">DESCRIPTION</span></span>
<span data-ttu-id="f5999-106">**AzDataShareTrigger** cmdlet은 azure data 공유 계정 아래에서 지정 된 되풀이 간격과 동기화 시간에 대 한 공유 구독에 대 한 트리거를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f5999-106">The **New-AzDataShareTrigger** cmdlet creates a trigger for share subscription for the specified recurrence interval and synchronization time under azure data share account.</span></span>

## <span data-ttu-id="f5999-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f5999-107">EXAMPLES</span></span>

### <span data-ttu-id="f5999-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f5999-108">Example 1</span></span>
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

<span data-ttu-id="f5999-109">이 명령은 일일 되풀이 간격 9 am을 사용 하 여 공유 구독 AdsShareSubscription에 대 한 새 트리거 AdsTrigger를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f5999-109">This command creates a new trigger AdsTrigger for share subscription AdsShareSubscription with a daily recurrence interval of 9 am.</span></span>

## <span data-ttu-id="f5999-110">변수</span><span class="sxs-lookup"><span data-stu-id="f5999-110">PARAMETERS</span></span>

### <span data-ttu-id="f5999-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f5999-111">-AccountName</span></span>
<span data-ttu-id="f5999-112">Azure data share 계정 이름</span><span class="sxs-lookup"><span data-stu-id="f5999-112">Azure data share account name</span></span>

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

### <span data-ttu-id="f5999-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5999-113">-AsJob</span></span>
<span data-ttu-id="f5999-114">{{AsJob 입력 기술}}</span><span class="sxs-lookup"><span data-stu-id="f5999-114">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="f5999-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5999-115">-DefaultProfile</span></span>
<span data-ttu-id="f5999-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f5999-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5999-117">-이름</span><span class="sxs-lookup"><span data-stu-id="f5999-117">-Name</span></span>
<span data-ttu-id="f5999-118">Azure data share 트리거 이름</span><span class="sxs-lookup"><span data-stu-id="f5999-118">Azure data share trigger name</span></span>

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

### <span data-ttu-id="f5999-119">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="f5999-119">-RecurrenceInterval</span></span>
<span data-ttu-id="f5999-120">트리거의 되풀이 간격 (일 또는 시간)입니다.</span><span class="sxs-lookup"><span data-stu-id="f5999-120">The recurrence interval for the trigger (Day or Hour)</span></span>

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

### <span data-ttu-id="f5999-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5999-121">-ResourceGroupName</span></span>
<span data-ttu-id="f5999-122">Azure data share 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="f5999-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="f5999-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="f5999-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="f5999-124">Azure data share 구독 이름</span><span class="sxs-lookup"><span data-stu-id="f5999-124">Azure data share subscription name</span></span>

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

### <span data-ttu-id="f5999-125">-SynchronizationTime</span><span class="sxs-lookup"><span data-stu-id="f5999-125">-SynchronizationTime</span></span>
<span data-ttu-id="f5999-126">트리거의 예약 된 동기화 시작 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="f5999-126">The start time of the scheduled synchronization for the trigger</span></span>

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

### <span data-ttu-id="f5999-127">-확인</span><span class="sxs-lookup"><span data-stu-id="f5999-127">-Confirm</span></span>
<span data-ttu-id="f5999-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5999-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5999-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5999-129">-WhatIf</span></span>
<span data-ttu-id="f5999-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f5999-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5999-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f5999-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5999-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5999-132">CommonParameters</span></span>
<span data-ttu-id="f5999-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5999-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5999-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f5999-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5999-135">입력</span><span class="sxs-lookup"><span data-stu-id="f5999-135">INPUTS</span></span>

### <span data-ttu-id="f5999-136">않아야</span><span class="sxs-lookup"><span data-stu-id="f5999-136">None</span></span>

## <span data-ttu-id="f5999-137">출력</span><span class="sxs-lookup"><span data-stu-id="f5999-137">OUTPUTS</span></span>

### <span data-ttu-id="f5999-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="f5999-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="f5999-139">상속자</span><span class="sxs-lookup"><span data-stu-id="f5999-139">NOTES</span></span>

## <span data-ttu-id="f5999-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f5999-140">RELATED LINKS</span></span>
