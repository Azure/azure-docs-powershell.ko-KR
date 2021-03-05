---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/start-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Start-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Start-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: b2fe61d4493fea64f4ee7b07bdd14905fb7661db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966512"
---
# <span data-ttu-id="95c1f-101">Start-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="95c1f-101">Start-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="95c1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95c1f-102">SYNOPSIS</span></span>
<span data-ttu-id="95c1f-103">공유 구독에 대한 동기화를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="95c1f-103">Initiates synchronization for a share subscription.</span></span> <span data-ttu-id="95c1f-104">공유 구독은 해당 리소스 ID 또는 해당 이름을 통해 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="95c1f-104">A share subscription can be specified through its resource id or its name.</span></span>

## <span data-ttu-id="95c1f-105">구문</span><span class="sxs-lookup"><span data-stu-id="95c1f-105">SYNTAX</span></span>

### <span data-ttu-id="95c1f-106">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="95c1f-106">ByFieldsParameterSet (Default)</span></span>
```
Start-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationMode <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95c1f-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="95c1f-107">ByResourceIdParameterSet</span></span>
```
Start-AzDataShareSubscriptionSynchronization -SynchronizationMode <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95c1f-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="95c1f-108">ByObjectParameterSet</span></span>
```
Start-AzDataShareSubscriptionSynchronization -InputObject <PSDataShareSubscription> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95c1f-109">설명</span><span class="sxs-lookup"><span data-stu-id="95c1f-109">DESCRIPTION</span></span>
<span data-ttu-id="95c1f-110">**Start-AzDataShareSubscriptionSynchronization** cmdlet은 공유 구독에 대한 동기화를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="95c1f-110">The **Start-AzDataShareSubscriptionSynchronization** cmdlet initiates synchronization for a share subscription</span></span>

## <span data-ttu-id="95c1f-111">예제</span><span class="sxs-lookup"><span data-stu-id="95c1f-111">EXAMPLES</span></span>

### <span data-ttu-id="95c1f-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="95c1f-112">Example 1</span></span>
```
PS C:\> Start-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -SynchronizationMode Incremental

Confirm
AdsShareSubscription
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

durationMs        : 231869
endTime           : 7/9/2019 11:44:41 PM
message           :
startTime         : 7/9/2019 11:40:53 PM
status            : Succeeded
synchronizationId : 20a4416b-b33b-4539-a908-71dc8ef698fb
```

<span data-ttu-id="95c1f-113">이 명령은 계정 WikiAds에서 AdsShareSubscription이라는 공유 구독에 대한 동기화를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="95c1f-113">This commands initiates synchronization for a sharesubscription named AdsShareSubscription in account WikiAds.</span></span> 

## <span data-ttu-id="95c1f-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="95c1f-114">PARAMETERS</span></span>

### <span data-ttu-id="95c1f-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="95c1f-115">-AccountName</span></span>
<span data-ttu-id="95c1f-116">Azure 데이터 공유 계정 이름</span><span class="sxs-lookup"><span data-stu-id="95c1f-116">Azure data share account name</span></span>

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

### <span data-ttu-id="95c1f-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95c1f-117">-AsJob</span></span>
<span data-ttu-id="95c1f-118">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="95c1f-118">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="95c1f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95c1f-119">-DefaultProfile</span></span>
<span data-ttu-id="95c1f-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="95c1f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95c1f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95c1f-121">-InputObject</span></span>
<span data-ttu-id="95c1f-122">Azure 데이터 공유 구독 개체</span><span class="sxs-lookup"><span data-stu-id="95c1f-122">Azure data share subscription object</span></span>


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

### <span data-ttu-id="95c1f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95c1f-123">-ResourceGroupName</span></span>
<span data-ttu-id="95c1f-124">Azure 데이터 공유 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="95c1f-124">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="95c1f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="95c1f-125">-ResourceId</span></span>
<span data-ttu-id="95c1f-126">Azure Share 구독의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="95c1f-126">The resource id of the azure share subscription</span></span>

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

### <span data-ttu-id="95c1f-127">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="95c1f-127">-ShareSubscriptionName</span></span>
<span data-ttu-id="95c1f-128">Azure 데이터 공유 구독 이름</span><span class="sxs-lookup"><span data-stu-id="95c1f-128">Azure data share subscription name</span></span>

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

### <span data-ttu-id="95c1f-129">-동기화모드</span><span class="sxs-lookup"><span data-stu-id="95c1f-129">-SynchronizationMode</span></span>
<span data-ttu-id="95c1f-130">동기화 모드(FullSync 또는 증분)</span><span class="sxs-lookup"><span data-stu-id="95c1f-130">Synchronization mode (FullSync or Incremental)</span></span>

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

### <span data-ttu-id="95c1f-131">-확인</span><span class="sxs-lookup"><span data-stu-id="95c1f-131">-Confirm</span></span>
<span data-ttu-id="95c1f-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="95c1f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95c1f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95c1f-133">-WhatIf</span></span>
<span data-ttu-id="95c1f-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="95c1f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95c1f-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95c1f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95c1f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95c1f-136">CommonParameters</span></span>
<span data-ttu-id="95c1f-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="95c1f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95c1f-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95c1f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95c1f-139">입력</span><span class="sxs-lookup"><span data-stu-id="95c1f-139">INPUTS</span></span>

### <span data-ttu-id="95c1f-140">System.String</span><span class="sxs-lookup"><span data-stu-id="95c1f-140">System.String</span></span>

### <span data-ttu-id="95c1f-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="95c1f-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="95c1f-142">출력</span><span class="sxs-lookup"><span data-stu-id="95c1f-142">OUTPUTS</span></span>

### <span data-ttu-id="95c1f-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="95c1f-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="95c1f-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="95c1f-144">NOTES</span></span>

## <span data-ttu-id="95c1f-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95c1f-145">RELATED LINKS</span></span>
