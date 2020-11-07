---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/stop-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Stop-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Stop-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: 01ca3c42db57760f23e49f93fc7e4d533b4047b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696678"
---
# <span data-ttu-id="80b35-101">Stop-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="80b35-101">Stop-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="80b35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80b35-102">SYNOPSIS</span></span>
<span data-ttu-id="80b35-103">공유 구독에 대해 진행 중인 동기화를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="80b35-103">Stops ongoing synchronization for a share subscription.</span></span> <span data-ttu-id="80b35-104">공유 구독은 해당 리소스 id 또는 해당 이름을 통해 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80b35-104">A share subscription can be specified through its resource id or its name.</span></span>

## <span data-ttu-id="80b35-105">구문과</span><span class="sxs-lookup"><span data-stu-id="80b35-105">SYNTAX</span></span>

### <span data-ttu-id="80b35-106">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="80b35-106">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80b35-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="80b35-107">ByResourceIdParameterSet</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -SynchronizationId <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80b35-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="80b35-108">ByObjectParameterSet</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -InputObject <PSDataShareSubscription> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80b35-109">설명은</span><span class="sxs-lookup"><span data-stu-id="80b35-109">DESCRIPTION</span></span>
<span data-ttu-id="80b35-110">**AzDataShareSubscriptionSynchronization** cmdlet은 공유 구독에 대해 진행 중인 동기화를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="80b35-110">The **Stop-AzDataShareSubscriptionSynchronization** cmdlet stops ongoing synchronization for a share subscription</span></span>

## <span data-ttu-id="80b35-111">예제의</span><span class="sxs-lookup"><span data-stu-id="80b35-111">EXAMPLES</span></span>

### <span data-ttu-id="80b35-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="80b35-112">Example 1</span></span>
```
PS C:\> Stop-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -SynchronizationId 20a4416b-b33b-4539-a908-71dc8ef698fb

Confirm
AdsShareSubscription
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

durationMs        : 231869
endTime           : 
message           :
startTime         : 7/9/2019 11:40:53 PM
status            : Canceled
synchronizationId : 20a4416b-b33b-4539-a908-71dc8ef698fb
```

<span data-ttu-id="80b35-113">Id-20a4416b-b33b-4539-a908-71dc8ef698fb에서 식별 된 지속적인 동기화를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="80b35-113">Stops ongoing synchronization identified by id - 20a4416b-b33b-4539-a908-71dc8ef698fb</span></span>

## <span data-ttu-id="80b35-114">변수</span><span class="sxs-lookup"><span data-stu-id="80b35-114">PARAMETERS</span></span>

### <span data-ttu-id="80b35-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="80b35-115">-AccountName</span></span>
<span data-ttu-id="80b35-116">Azure data share 계정 이름</span><span class="sxs-lookup"><span data-stu-id="80b35-116">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80b35-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80b35-117">-AsJob</span></span>
<span data-ttu-id="80b35-118">{{AsJob 입력 기술}}</span><span class="sxs-lookup"><span data-stu-id="80b35-118">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="80b35-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80b35-119">-DefaultProfile</span></span>
<span data-ttu-id="80b35-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="80b35-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80b35-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80b35-121">-InputObject</span></span>
<span data-ttu-id="80b35-122">Azure data share 구독 개체</span><span class="sxs-lookup"><span data-stu-id="80b35-122">Azure data share subscription object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80b35-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80b35-123">-ResourceGroupName</span></span>
<span data-ttu-id="80b35-124">Azure data share 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="80b35-124">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80b35-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80b35-125">-ResourceId</span></span>
<span data-ttu-id="80b35-126">Azure 공유 구독의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="80b35-126">The resource id of the azure share subscription</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80b35-127">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="80b35-127">-ShareSubscriptionName</span></span>
<span data-ttu-id="80b35-128">Azure data share 구독 이름</span><span class="sxs-lookup"><span data-stu-id="80b35-128">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80b35-129">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="80b35-129">-SynchronizationId</span></span>
<span data-ttu-id="80b35-130">중지 해야 하는 동기화 id</span><span class="sxs-lookup"><span data-stu-id="80b35-130">Synchronization id that needs to be stopped</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80b35-131">-확인</span><span class="sxs-lookup"><span data-stu-id="80b35-131">-Confirm</span></span>
<span data-ttu-id="80b35-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="80b35-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80b35-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80b35-133">-WhatIf</span></span>
<span data-ttu-id="80b35-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="80b35-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80b35-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="80b35-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80b35-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80b35-136">CommonParameters</span></span>
<span data-ttu-id="80b35-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="80b35-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80b35-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80b35-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80b35-139">입력</span><span class="sxs-lookup"><span data-stu-id="80b35-139">INPUTS</span></span>

### <span data-ttu-id="80b35-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="80b35-140">System.String</span></span>

### <span data-ttu-id="80b35-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="80b35-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="80b35-142">출력</span><span class="sxs-lookup"><span data-stu-id="80b35-142">OUTPUTS</span></span>

### <span data-ttu-id="80b35-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="80b35-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="80b35-144">상속자</span><span class="sxs-lookup"><span data-stu-id="80b35-144">NOTES</span></span>

## <span data-ttu-id="80b35-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="80b35-145">RELATED LINKS</span></span>
