---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
ms.openlocfilehash: eb2b7f1e22ff3d2fccdff0d84a77f5c68ca8e70d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333045"
---
# <span data-ttu-id="6eb77-101">Remove-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="6eb77-101">Remove-AzDataShareSubscription</span></span>

## <span data-ttu-id="6eb77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6eb77-102">SYNOPSIS</span></span>
<span data-ttu-id="6eb77-103">공유 구독을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb77-103">removes a share subscription</span></span>

## <span data-ttu-id="6eb77-104">구문</span><span class="sxs-lookup"><span data-stu-id="6eb77-104">SYNTAX</span></span>

### <span data-ttu-id="6eb77-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6eb77-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6eb77-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6eb77-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSubscription -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6eb77-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6eb77-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSubscription -InputObject <PSDataShareSubscription> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6eb77-108">설명</span><span class="sxs-lookup"><span data-stu-id="6eb77-108">DESCRIPTION</span></span>
<span data-ttu-id="6eb77-109">**Remove-AzDataShareSubscription** cmdlet은 공유 구독을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb77-109">The **Remove-AzDataShareSubscription** cmdlet removes a share subscription</span></span>

## <span data-ttu-id="6eb77-110">예제</span><span class="sxs-lookup"><span data-stu-id="6eb77-110">EXAMPLES</span></span>

### <span data-ttu-id="6eb77-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6eb77-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"
Are you sure you want to remove sharesubscription "AdsShareSubscription"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="6eb77-112">이 명령은 계정 WikiAds에서 AdsShareSubscription이라는 공유 구독을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb77-112">This commands removes a sharesubscription named AdsShareSubscription from account WikiAds.</span></span> 

## <span data-ttu-id="6eb77-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6eb77-113">PARAMETERS</span></span>

### <span data-ttu-id="6eb77-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6eb77-114">-AccountName</span></span>
<span data-ttu-id="6eb77-115">Azure 데이터 공유 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6eb77-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="6eb77-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6eb77-116">-AsJob</span></span>
<span data-ttu-id="6eb77-117">{{AsJob 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="6eb77-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="6eb77-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eb77-118">-DefaultProfile</span></span>
<span data-ttu-id="6eb77-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6eb77-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6eb77-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6eb77-120">-InputObject</span></span>
<span data-ttu-id="6eb77-121">Azure 데이터 공유 구독 개체</span><span class="sxs-lookup"><span data-stu-id="6eb77-121">Azure data share subscription object</span></span>


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

### <span data-ttu-id="6eb77-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6eb77-122">-Name</span></span>
<span data-ttu-id="6eb77-123">Azure 데이터 공유 구독 이름</span><span class="sxs-lookup"><span data-stu-id="6eb77-123">Azure data share subscription name</span></span>

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

### <span data-ttu-id="6eb77-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6eb77-124">-PassThru</span></span>
<span data-ttu-id="6eb77-125">개체를 반환합니다(지정된 경우).</span><span class="sxs-lookup"><span data-stu-id="6eb77-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="6eb77-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6eb77-126">-ResourceGroupName</span></span>
<span data-ttu-id="6eb77-127">Azure 데이터 공유 계정의 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="6eb77-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="6eb77-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6eb77-128">-ResourceId</span></span>
<span data-ttu-id="6eb77-129">Azure 데이터 공유 구독의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="6eb77-129">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="6eb77-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6eb77-130">-Confirm</span></span>
<span data-ttu-id="6eb77-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6eb77-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6eb77-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6eb77-132">-WhatIf</span></span>
<span data-ttu-id="6eb77-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6eb77-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6eb77-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6eb77-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6eb77-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eb77-135">CommonParameters</span></span>
<span data-ttu-id="6eb77-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6eb77-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eb77-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6eb77-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eb77-138">입력</span><span class="sxs-lookup"><span data-stu-id="6eb77-138">INPUTS</span></span>

### <span data-ttu-id="6eb77-139">System.String</span><span class="sxs-lookup"><span data-stu-id="6eb77-139">System.String</span></span>

### <span data-ttu-id="6eb77-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="6eb77-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="6eb77-141">출력</span><span class="sxs-lookup"><span data-stu-id="6eb77-141">OUTPUTS</span></span>

### <span data-ttu-id="6eb77-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6eb77-142">System.Boolean</span></span>

## <span data-ttu-id="6eb77-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6eb77-143">NOTES</span></span>

## <span data-ttu-id="6eb77-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6eb77-144">RELATED LINKS</span></span>