---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
ms.openlocfilehash: e7a74fcc6d5e1a80282cfb365070df1b339aea45
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353685"
---
# <span data-ttu-id="7dcb0-101">Remove-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="7dcb0-101">Remove-AzSearchQueryKey</span></span>

## <span data-ttu-id="7dcb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7dcb0-102">SYNOPSIS</span></span>
<span data-ttu-id="7dcb0-103">Azure Search 서비스에서 쿼리 키를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7dcb0-103">Remove the query key from the Azure Search service.</span></span>

## <span data-ttu-id="7dcb0-104">구문</span><span class="sxs-lookup"><span data-stu-id="7dcb0-104">SYNTAX</span></span>

### <span data-ttu-id="7dcb0-105">ResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="7dcb0-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyValue <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7dcb0-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7dcb0-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentObject] <PSSearchService> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7dcb0-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7dcb0-107">ParentResourceIdParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentResourceId] <String> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7dcb0-108">설명</span><span class="sxs-lookup"><span data-stu-id="7dcb0-108">DESCRIPTION</span></span>
<span data-ttu-id="7dcb0-109">**Remove-AzSearchQueryKey** cmdlet은 Azure Search 서비스에서 쿼리 키를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7dcb0-109">The **Remove-AzSearchQueryKey** cmdlet removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="7dcb0-110">예제</span><span class="sxs-lookup"><span data-stu-id="7dcb0-110">EXAMPLES</span></span>

### <span data-ttu-id="7dcb0-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7dcb0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name         Key                             
----         ---                             
             D260F448EA192EBC19D59F7E5670E8BB
NewQueryKey1 B4C13E3F6FA76100D3488673CFDCD438

PS C:\> Remove-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyValue B4C13E3F6FA76100D3488673CFDCD438

Confirm
Are you sure you want to remove query key 'B4C13E3F6FA76100D3488673CFDCD438'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="7dcb0-112">이 예제에서는 Azure Search 서비스에서 쿼리 키를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7dcb0-112">The example removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="7dcb0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7dcb0-113">PARAMETERS</span></span>

### <span data-ttu-id="7dcb0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dcb0-114">-DefaultProfile</span></span>
<span data-ttu-id="7dcb0-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7dcb0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7dcb0-116">-Force</span><span class="sxs-lookup"><span data-stu-id="7dcb0-116">-Force</span></span>
<span data-ttu-id="7dcb0-117">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7dcb0-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7dcb0-118">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="7dcb0-118">-KeyValue</span></span>
<span data-ttu-id="7dcb0-119">Search 서비스 쿼리 키 값입니다.</span><span class="sxs-lookup"><span data-stu-id="7dcb0-119">Search Service query key value.</span></span>

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

### <span data-ttu-id="7dcb0-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7dcb0-120">-ParentObject</span></span>
<span data-ttu-id="7dcb0-121">Search 서비스 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7dcb0-121">Search Service Input Object.</span></span>

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

### <span data-ttu-id="7dcb0-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="7dcb0-122">-ParentResourceId</span></span>
<span data-ttu-id="7dcb0-123">Search 서비스 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7dcb0-123">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="7dcb0-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7dcb0-124">-PassThru</span></span>
<span data-ttu-id="7dcb0-125">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7dcb0-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="7dcb0-126">이 스위치를 지정하면 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7dcb0-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="7dcb0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7dcb0-127">-ResourceGroupName</span></span>
<span data-ttu-id="7dcb0-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7dcb0-128">Resource Group name.</span></span>

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

### <span data-ttu-id="7dcb0-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7dcb0-129">-ServiceName</span></span>
<span data-ttu-id="7dcb0-130">검색 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7dcb0-130">Search Service name.</span></span>

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

### <span data-ttu-id="7dcb0-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7dcb0-131">-Confirm</span></span>
<span data-ttu-id="7dcb0-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7dcb0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7dcb0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7dcb0-133">-WhatIf</span></span>
<span data-ttu-id="7dcb0-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7dcb0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7dcb0-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7dcb0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7dcb0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dcb0-136">CommonParameters</span></span>
<span data-ttu-id="7dcb0-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7dcb0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dcb0-138">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7dcb0-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dcb0-139">입력</span><span class="sxs-lookup"><span data-stu-id="7dcb0-139">INPUTS</span></span>

### <span data-ttu-id="7dcb0-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="7dcb0-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="7dcb0-141">System.String</span><span class="sxs-lookup"><span data-stu-id="7dcb0-141">System.String</span></span>

## <span data-ttu-id="7dcb0-142">출력</span><span class="sxs-lookup"><span data-stu-id="7dcb0-142">OUTPUTS</span></span>

### <span data-ttu-id="7dcb0-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7dcb0-143">System.Boolean</span></span>

## <span data-ttu-id="7dcb0-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7dcb0-144">NOTES</span></span>

## <span data-ttu-id="7dcb0-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7dcb0-145">RELATED LINKS</span></span>

[<span data-ttu-id="7dcb0-146">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="7dcb0-146">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="7dcb0-147">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="7dcb0-147">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)
