---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
ms.openlocfilehash: e7a74fcc6d5e1a80282cfb365070df1b339aea45
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204860"
---
# <span data-ttu-id="8e890-101">Remove-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="8e890-101">Remove-AzSearchQueryKey</span></span>

## <span data-ttu-id="8e890-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e890-102">SYNOPSIS</span></span>
<span data-ttu-id="8e890-103">Azure Search 서비스에서 쿼리 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e890-103">Remove the query key from the Azure Search service.</span></span>

## <span data-ttu-id="8e890-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8e890-104">SYNTAX</span></span>

### <span data-ttu-id="8e890-105">ResourceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8e890-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyValue <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e890-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e890-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentObject] <PSSearchService> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e890-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e890-107">ParentResourceIdParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentResourceId] <String> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e890-108">설명은</span><span class="sxs-lookup"><span data-stu-id="8e890-108">DESCRIPTION</span></span>
<span data-ttu-id="8e890-109">**AzSearchQueryKey** Cmdlet은 Azure Search 서비스에서 쿼리 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e890-109">The **Remove-AzSearchQueryKey** cmdlet removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="8e890-110">예제의</span><span class="sxs-lookup"><span data-stu-id="8e890-110">EXAMPLES</span></span>

### <span data-ttu-id="8e890-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="8e890-111">Example 1</span></span>
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

<span data-ttu-id="8e890-112">이 예제에서는 Azure Search 서비스에서 쿼리 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e890-112">The example removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="8e890-113">변수</span><span class="sxs-lookup"><span data-stu-id="8e890-113">PARAMETERS</span></span>

### <span data-ttu-id="8e890-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e890-114">-DefaultProfile</span></span>
<span data-ttu-id="8e890-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8e890-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e890-116">-Force</span><span class="sxs-lookup"><span data-stu-id="8e890-116">-Force</span></span>
<span data-ttu-id="8e890-117">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8e890-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8e890-118">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="8e890-118">-KeyValue</span></span>
<span data-ttu-id="8e890-119">검색 서비스 쿼리 키 값입니다.</span><span class="sxs-lookup"><span data-stu-id="8e890-119">Search Service query key value.</span></span>

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

### <span data-ttu-id="8e890-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8e890-120">-ParentObject</span></span>
<span data-ttu-id="8e890-121">검색 서비스 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8e890-121">Search Service Input Object.</span></span>

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

### <span data-ttu-id="8e890-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8e890-122">-ParentResourceId</span></span>
<span data-ttu-id="8e890-123">검색 서비스 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="8e890-123">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="8e890-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e890-124">-PassThru</span></span>
<span data-ttu-id="8e890-125">이 Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8e890-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="8e890-126">이 스위치를 지정 하면 성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e890-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="8e890-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e890-127">-ResourceGroupName</span></span>
<span data-ttu-id="8e890-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e890-128">Resource Group name.</span></span>

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

### <span data-ttu-id="8e890-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8e890-129">-ServiceName</span></span>
<span data-ttu-id="8e890-130">검색 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e890-130">Search Service name.</span></span>

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

### <span data-ttu-id="8e890-131">-확인</span><span class="sxs-lookup"><span data-stu-id="8e890-131">-Confirm</span></span>
<span data-ttu-id="8e890-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e890-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e890-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e890-133">-WhatIf</span></span>
<span data-ttu-id="8e890-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8e890-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e890-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8e890-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e890-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e890-136">CommonParameters</span></span>
<span data-ttu-id="8e890-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e890-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e890-138">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e890-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e890-139">입력</span><span class="sxs-lookup"><span data-stu-id="8e890-139">INPUTS</span></span>

### <span data-ttu-id="8e890-140">Microsoft. Azure. PSSearchService를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e890-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="8e890-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8e890-141">System.String</span></span>

## <span data-ttu-id="8e890-142">출력</span><span class="sxs-lookup"><span data-stu-id="8e890-142">OUTPUTS</span></span>

### <span data-ttu-id="8e890-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="8e890-143">System.Boolean</span></span>

## <span data-ttu-id="8e890-144">상속자</span><span class="sxs-lookup"><span data-stu-id="8e890-144">NOTES</span></span>

## <span data-ttu-id="8e890-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e890-145">RELATED LINKS</span></span>

[<span data-ttu-id="8e890-146">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="8e890-146">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="8e890-147">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="8e890-147">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)
