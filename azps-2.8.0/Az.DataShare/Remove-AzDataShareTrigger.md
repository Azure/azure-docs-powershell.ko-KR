---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
ms.openlocfilehash: a1ec489b91d2d510c16709fa0923117bbbaa804a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696684"
---
# <span data-ttu-id="9aa42-101">Remove-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="9aa42-101">Remove-AzDataShareTrigger</span></span>

## <span data-ttu-id="9aa42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9aa42-102">SYNOPSIS</span></span>
<span data-ttu-id="9aa42-103">트리거 제거</span><span class="sxs-lookup"><span data-stu-id="9aa42-103">removes a trigger</span></span>

## <span data-ttu-id="9aa42-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9aa42-104">SYNTAX</span></span>

### <span data-ttu-id="9aa42-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="9aa42-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9aa42-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9aa42-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareTrigger -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9aa42-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9aa42-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareTrigger -InputObject <PSDataShareTrigger> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9aa42-108">설명은</span><span class="sxs-lookup"><span data-stu-id="9aa42-108">DESCRIPTION</span></span>
<span data-ttu-id="9aa42-109">**AzDataShareTrigger** cmdlet은 datashare 트리거를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9aa42-109">The **Remove-AzDataShareTrigger** cmdlet removes a datashare trigger</span></span>

## <span data-ttu-id="9aa42-110">예제의</span><span class="sxs-lookup"><span data-stu-id="9aa42-110">EXAMPLES</span></span>

### <span data-ttu-id="9aa42-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="9aa42-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger"

Are you sure you want to remove trigger "AdsTrigger"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="9aa42-112">이 명령은 공유 구독 AdsShareSubscription에서 AdsTrigger 이라는 트리거를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9aa42-112">This commands removes a trigger named AdsTrigger from share subscription AdsShareSubscription.</span></span> 

## <span data-ttu-id="9aa42-113">변수</span><span class="sxs-lookup"><span data-stu-id="9aa42-113">PARAMETERS</span></span>

### <span data-ttu-id="9aa42-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9aa42-114">-AccountName</span></span>
<span data-ttu-id="9aa42-115">Azure data share 계정 이름</span><span class="sxs-lookup"><span data-stu-id="9aa42-115">Azure data share account name</span></span>

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

### <span data-ttu-id="9aa42-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9aa42-116">-AsJob</span></span>
<span data-ttu-id="9aa42-117">{{AsJob 입력 기술}}</span><span class="sxs-lookup"><span data-stu-id="9aa42-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="9aa42-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9aa42-118">-DefaultProfile</span></span>
<span data-ttu-id="9aa42-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9aa42-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9aa42-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9aa42-120">-InputObject</span></span>
<span data-ttu-id="9aa42-121">Azure data share 트리거 개체</span><span class="sxs-lookup"><span data-stu-id="9aa42-121">Azure data share trigger object</span></span>


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

### <span data-ttu-id="9aa42-122">-이름</span><span class="sxs-lookup"><span data-stu-id="9aa42-122">-Name</span></span>
<span data-ttu-id="9aa42-123">Azure data share 트리거 이름</span><span class="sxs-lookup"><span data-stu-id="9aa42-123">Azure data share trigger name</span></span>

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

### <span data-ttu-id="9aa42-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9aa42-124">-PassThru</span></span>
<span data-ttu-id="9aa42-125">Object (지정 된 경우)를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9aa42-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="9aa42-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9aa42-126">-ResourceGroupName</span></span>
<span data-ttu-id="9aa42-127">Azure data share 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="9aa42-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="9aa42-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9aa42-128">-ResourceId</span></span>
<span data-ttu-id="9aa42-129">Azure data share 트리거의 리소스 id</span><span class="sxs-lookup"><span data-stu-id="9aa42-129">The resource id of azure data share trigger</span></span>

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

### <span data-ttu-id="9aa42-130">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="9aa42-130">-ShareSubscriptionName</span></span>
<span data-ttu-id="9aa42-131">Azure data share 구독 이름</span><span class="sxs-lookup"><span data-stu-id="9aa42-131">Azure data share subscription name</span></span>

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

### <span data-ttu-id="9aa42-132">-확인</span><span class="sxs-lookup"><span data-stu-id="9aa42-132">-Confirm</span></span>
<span data-ttu-id="9aa42-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9aa42-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9aa42-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9aa42-134">-WhatIf</span></span>
<span data-ttu-id="9aa42-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9aa42-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9aa42-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9aa42-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9aa42-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aa42-137">CommonParameters</span></span>
<span data-ttu-id="9aa42-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9aa42-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aa42-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9aa42-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aa42-140">입력</span><span class="sxs-lookup"><span data-stu-id="9aa42-140">INPUTS</span></span>

### <span data-ttu-id="9aa42-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9aa42-141">System.String</span></span>

### <span data-ttu-id="9aa42-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="9aa42-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="9aa42-143">출력</span><span class="sxs-lookup"><span data-stu-id="9aa42-143">OUTPUTS</span></span>

### <span data-ttu-id="9aa42-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="9aa42-144">System.Boolean</span></span>

## <span data-ttu-id="9aa42-145">상속자</span><span class="sxs-lookup"><span data-stu-id="9aa42-145">NOTES</span></span>

## <span data-ttu-id="9aa42-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9aa42-146">RELATED LINKS</span></span>
