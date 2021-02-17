---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
ms.openlocfilehash: 7edca2e338c4972550d44cc6409187dbc53ab40b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192700"
---
# <span data-ttu-id="e6308-101">New-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="e6308-101">New-AzSearchQueryKey</span></span>

## <span data-ttu-id="e6308-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6308-102">SYNOPSIS</span></span>
<span data-ttu-id="e6308-103">Azure Cognitive Search 서비스에 대한 새 쿼리 키를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e6308-103">Create a new query key for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="e6308-104">구문</span><span class="sxs-lookup"><span data-stu-id="e6308-104">SYNTAX</span></span>

### <span data-ttu-id="e6308-105">ResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e6308-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6308-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6308-106">ParentObjectParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentObject] <PSSearchService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6308-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6308-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6308-108">설명</span><span class="sxs-lookup"><span data-stu-id="e6308-108">DESCRIPTION</span></span>
<span data-ttu-id="e6308-109">**New-AzSearchQueryKey** cmdlet은 Azure Cognitive Search 서비스에 대한 새 쿼리 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e6308-109">The **New-AzSearchQueryKey** cmdlet creates a new query key for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="e6308-110">예제</span><span class="sxs-lookup"><span data-stu-id="e6308-110">EXAMPLES</span></span>

### <span data-ttu-id="e6308-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e6308-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -Name "NewQueryKey1" -Force

Name         Key                             
----         ---                             
NewQueryKey1 65FBCF561228C5F0E01F8F2114C80459
```

<span data-ttu-id="e6308-112">이 예제에서는 Azure Cognitive Search 서비스에 대한 새 쿼리 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e6308-112">The example creates a new query key for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="e6308-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6308-113">PARAMETERS</span></span>

### <span data-ttu-id="e6308-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6308-114">-DefaultProfile</span></span>
<span data-ttu-id="e6308-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e6308-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6308-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e6308-116">-Name</span></span>
<span data-ttu-id="e6308-117">Azure Cognitive Search 서비스 쿼리 키 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e6308-117">Azure Cognitive Search Service query key name.</span></span>

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

### <span data-ttu-id="e6308-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e6308-118">-ParentObject</span></span>
<span data-ttu-id="e6308-119">Azure Cognitive Search 서비스 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e6308-119">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6308-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e6308-120">-ParentResourceId</span></span>
<span data-ttu-id="e6308-121">Azure Cognitive Search 서비스 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e6308-121">Azure Cognitive Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6308-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6308-122">-ResourceGroupName</span></span>
<span data-ttu-id="e6308-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e6308-123">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6308-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e6308-124">-ServiceName</span></span>
<span data-ttu-id="e6308-125">Azure Cognitive Search 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e6308-125">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6308-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6308-126">-Confirm</span></span>
<span data-ttu-id="e6308-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e6308-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6308-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6308-128">-WhatIf</span></span>
<span data-ttu-id="e6308-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e6308-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6308-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e6308-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6308-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6308-131">CommonParameters</span></span>
<span data-ttu-id="e6308-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e6308-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6308-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e6308-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6308-134">입력</span><span class="sxs-lookup"><span data-stu-id="e6308-134">INPUTS</span></span>

### <span data-ttu-id="e6308-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="e6308-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="e6308-136">System.String</span><span class="sxs-lookup"><span data-stu-id="e6308-136">System.String</span></span>

## <span data-ttu-id="e6308-137">출력</span><span class="sxs-lookup"><span data-stu-id="e6308-137">OUTPUTS</span></span>

### <span data-ttu-id="e6308-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="e6308-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="e6308-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e6308-139">NOTES</span></span>

## <span data-ttu-id="e6308-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e6308-140">RELATED LINKS</span></span>

[<span data-ttu-id="e6308-141">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="e6308-141">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)

[<span data-ttu-id="e6308-142">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="e6308-142">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)
