---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/stop-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Stop-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Stop-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: e865098b0c85227baf1f537fb22c40ee351902fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204317"
---
# <span data-ttu-id="bcf9f-101">Stop-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="bcf9f-101">Stop-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="bcf9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcf9f-102">SYNOPSIS</span></span>
<span data-ttu-id="bcf9f-103">공유 구독에 대한 지속적인 동기화를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="bcf9f-103">Stops ongoing synchronization for a share subscription.</span></span> <span data-ttu-id="bcf9f-104">공유 구독은 해당 리소스 ID 또는 해당 이름을 통해 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bcf9f-104">A share subscription can be specified through its resource id or its name.</span></span>

## <span data-ttu-id="bcf9f-105">구문</span><span class="sxs-lookup"><span data-stu-id="bcf9f-105">SYNTAX</span></span>

### <span data-ttu-id="bcf9f-106">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="bcf9f-106">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcf9f-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcf9f-107">ByResourceIdParameterSet</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -SynchronizationId <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcf9f-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcf9f-108">ByObjectParameterSet</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -InputObject <PSDataShareSubscription> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcf9f-109">설명</span><span class="sxs-lookup"><span data-stu-id="bcf9f-109">DESCRIPTION</span></span>
<span data-ttu-id="bcf9f-110">**Stop-AzDataShareSubscriptionSynchronization** cmdlet은 공유 구독에 대한 지속적인 동기화를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="bcf9f-110">The **Stop-AzDataShareSubscriptionSynchronization** cmdlet stops ongoing synchronization for a share subscription</span></span>

## <span data-ttu-id="bcf9f-111">예제</span><span class="sxs-lookup"><span data-stu-id="bcf9f-111">EXAMPLES</span></span>

### <span data-ttu-id="bcf9f-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="bcf9f-112">Example 1</span></span>
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

<span data-ttu-id="bcf9f-113">ID로 식별된 지속적인 동기화 중지 - 20a4416b-b33b-4539-a908-71dc8ef698fb</span><span class="sxs-lookup"><span data-stu-id="bcf9f-113">Stops ongoing synchronization identified by id - 20a4416b-b33b-4539-a908-71dc8ef698fb</span></span>

## <span data-ttu-id="bcf9f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bcf9f-114">PARAMETERS</span></span>

### <span data-ttu-id="bcf9f-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bcf9f-115">-AccountName</span></span>
<span data-ttu-id="bcf9f-116">Azure 데이터 공유 계정 이름</span><span class="sxs-lookup"><span data-stu-id="bcf9f-116">Azure data share account name</span></span>

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

### <span data-ttu-id="bcf9f-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bcf9f-117">-AsJob</span></span>
<span data-ttu-id="bcf9f-118">{{AsJob 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="bcf9f-118">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="bcf9f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcf9f-119">-DefaultProfile</span></span>
<span data-ttu-id="bcf9f-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bcf9f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcf9f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bcf9f-121">-InputObject</span></span>
<span data-ttu-id="bcf9f-122">Azure 데이터 공유 구독 개체</span><span class="sxs-lookup"><span data-stu-id="bcf9f-122">Azure data share subscription object</span></span>


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

### <span data-ttu-id="bcf9f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcf9f-123">-ResourceGroupName</span></span>
<span data-ttu-id="bcf9f-124">Azure 데이터 공유 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="bcf9f-124">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="bcf9f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bcf9f-125">-ResourceId</span></span>
<span data-ttu-id="bcf9f-126">Azure 공유 구독의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="bcf9f-126">The resource id of the azure share subscription</span></span>

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

### <span data-ttu-id="bcf9f-127">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="bcf9f-127">-ShareSubscriptionName</span></span>
<span data-ttu-id="bcf9f-128">Azure 데이터 공유 구독 이름</span><span class="sxs-lookup"><span data-stu-id="bcf9f-128">Azure data share subscription name</span></span>

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

### <span data-ttu-id="bcf9f-129">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="bcf9f-129">-SynchronizationId</span></span>
<span data-ttu-id="bcf9f-130">중지해야 하는 동기화 ID</span><span class="sxs-lookup"><span data-stu-id="bcf9f-130">Synchronization id that needs to be stopped</span></span>

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

### <span data-ttu-id="bcf9f-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bcf9f-131">-Confirm</span></span>
<span data-ttu-id="bcf9f-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bcf9f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcf9f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcf9f-133">-WhatIf</span></span>
<span data-ttu-id="bcf9f-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="bcf9f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcf9f-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bcf9f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcf9f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcf9f-136">CommonParameters</span></span>
<span data-ttu-id="bcf9f-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bcf9f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcf9f-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bcf9f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcf9f-139">입력</span><span class="sxs-lookup"><span data-stu-id="bcf9f-139">INPUTS</span></span>

### <span data-ttu-id="bcf9f-140">System.String</span><span class="sxs-lookup"><span data-stu-id="bcf9f-140">System.String</span></span>

### <span data-ttu-id="bcf9f-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="bcf9f-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="bcf9f-142">출력</span><span class="sxs-lookup"><span data-stu-id="bcf9f-142">OUTPUTS</span></span>

### <span data-ttu-id="bcf9f-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="bcf9f-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="bcf9f-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bcf9f-144">NOTES</span></span>

## <span data-ttu-id="bcf9f-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bcf9f-145">RELATED LINKS</span></span>
