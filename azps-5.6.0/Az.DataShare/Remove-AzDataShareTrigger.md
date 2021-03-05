---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
ms.openlocfilehash: 9ee4c8c25f6a9575283c8e5f077be7107756f701
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966528"
---
# <span data-ttu-id="cb068-101">Remove-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="cb068-101">Remove-AzDataShareTrigger</span></span>

## <span data-ttu-id="cb068-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb068-102">SYNOPSIS</span></span>
<span data-ttu-id="cb068-103">트리거를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="cb068-103">removes a trigger</span></span>

## <span data-ttu-id="cb068-104">구문</span><span class="sxs-lookup"><span data-stu-id="cb068-104">SYNTAX</span></span>

### <span data-ttu-id="cb068-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="cb068-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb068-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb068-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareTrigger -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb068-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb068-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareTrigger -InputObject <PSDataShareTrigger> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb068-108">설명</span><span class="sxs-lookup"><span data-stu-id="cb068-108">DESCRIPTION</span></span>
<span data-ttu-id="cb068-109">**Remove-AzDataShareTrigger** cmdlet은 데이터 공유 트리거를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="cb068-109">The **Remove-AzDataShareTrigger** cmdlet removes a datashare trigger</span></span>

## <span data-ttu-id="cb068-110">예제</span><span class="sxs-lookup"><span data-stu-id="cb068-110">EXAMPLES</span></span>

### <span data-ttu-id="cb068-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="cb068-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger"

Are you sure you want to remove trigger "AdsTrigger"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="cb068-112">이 명령은 공유 구독 AdsShareSubscription에서 AdsTrigger라는 트리거를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="cb068-112">This commands removes a trigger named AdsTrigger from share subscription AdsShareSubscription.</span></span> 

## <span data-ttu-id="cb068-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="cb068-113">PARAMETERS</span></span>

### <span data-ttu-id="cb068-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cb068-114">-AccountName</span></span>
<span data-ttu-id="cb068-115">Azure 데이터 공유 계정 이름</span><span class="sxs-lookup"><span data-stu-id="cb068-115">Azure data share account name</span></span>

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

### <span data-ttu-id="cb068-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb068-116">-AsJob</span></span>
<span data-ttu-id="cb068-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="cb068-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="cb068-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb068-118">-DefaultProfile</span></span>
<span data-ttu-id="cb068-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cb068-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb068-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb068-120">-InputObject</span></span>
<span data-ttu-id="cb068-121">Azure 데이터 공유 트리거 개체</span><span class="sxs-lookup"><span data-stu-id="cb068-121">Azure data share trigger object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb068-122">-Name</span><span class="sxs-lookup"><span data-stu-id="cb068-122">-Name</span></span>
<span data-ttu-id="cb068-123">Azure 데이터 공유 트리거 이름</span><span class="sxs-lookup"><span data-stu-id="cb068-123">Azure data share trigger name</span></span>

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

### <span data-ttu-id="cb068-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb068-124">-PassThru</span></span>
<span data-ttu-id="cb068-125">개체를 반환합니다(지정된 경우).</span><span class="sxs-lookup"><span data-stu-id="cb068-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="cb068-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb068-126">-ResourceGroupName</span></span>
<span data-ttu-id="cb068-127">Azure 데이터 공유 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="cb068-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="cb068-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb068-128">-ResourceId</span></span>
<span data-ttu-id="cb068-129">Azure 데이터 공유 트리거의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="cb068-129">The resource id of azure data share trigger</span></span>

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

### <span data-ttu-id="cb068-130">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="cb068-130">-ShareSubscriptionName</span></span>
<span data-ttu-id="cb068-131">Azure 데이터 공유 구독 이름</span><span class="sxs-lookup"><span data-stu-id="cb068-131">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb068-132">-확인</span><span class="sxs-lookup"><span data-stu-id="cb068-132">-Confirm</span></span>
<span data-ttu-id="cb068-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cb068-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb068-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb068-134">-WhatIf</span></span>
<span data-ttu-id="cb068-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="cb068-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb068-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cb068-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb068-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb068-137">CommonParameters</span></span>
<span data-ttu-id="cb068-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cb068-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb068-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb068-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb068-140">입력</span><span class="sxs-lookup"><span data-stu-id="cb068-140">INPUTS</span></span>

### <span data-ttu-id="cb068-141">System.String</span><span class="sxs-lookup"><span data-stu-id="cb068-141">System.String</span></span>

### <span data-ttu-id="cb068-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="cb068-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="cb068-143">출력</span><span class="sxs-lookup"><span data-stu-id="cb068-143">OUTPUTS</span></span>

### <span data-ttu-id="cb068-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cb068-144">System.Boolean</span></span>

## <span data-ttu-id="cb068-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cb068-145">NOTES</span></span>

## <span data-ttu-id="cb068-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cb068-146">RELATED LINKS</span></span>
