---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
ms.openlocfilehash: e01e5e244bd34e3e18aa287e0f2f5709c5e208ec
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204371"
---
# <span data-ttu-id="77704-101">New-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="77704-101">New-AzSearchQueryKey</span></span>

## <span data-ttu-id="77704-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77704-102">SYNOPSIS</span></span>
<span data-ttu-id="77704-103">Azure Search 서비스에 대 한 새 쿼리 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="77704-103">Create a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="77704-104">구문과</span><span class="sxs-lookup"><span data-stu-id="77704-104">SYNTAX</span></span>

### <span data-ttu-id="77704-105">ResourceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="77704-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77704-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="77704-106">ParentObjectParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentObject] <PSSearchService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77704-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="77704-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77704-108">설명은</span><span class="sxs-lookup"><span data-stu-id="77704-108">DESCRIPTION</span></span>
<span data-ttu-id="77704-109">**AzSearchQueryKey** Cmdlet은 Azure Search 서비스에 대 한 새 쿼리 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="77704-109">The **New-AzSearchQueryKey** cmdlet creates a new query key for the Azure Search Service.</span></span>

## <span data-ttu-id="77704-110">예제의</span><span class="sxs-lookup"><span data-stu-id="77704-110">EXAMPLES</span></span>

### <span data-ttu-id="77704-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="77704-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -Name "NewQueryKey1" -Force

Name         Key                             
----         ---                             
NewQueryKey1 65FBCF561228C5F0E01F8F2114C80459
```

<span data-ttu-id="77704-112">이 예제에서는 Azure Search 서비스에 대 한 새 쿼리 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="77704-112">The example creates a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="77704-113">변수</span><span class="sxs-lookup"><span data-stu-id="77704-113">PARAMETERS</span></span>

### <span data-ttu-id="77704-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77704-114">-DefaultProfile</span></span>
<span data-ttu-id="77704-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="77704-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77704-116">-이름</span><span class="sxs-lookup"><span data-stu-id="77704-116">-Name</span></span>
<span data-ttu-id="77704-117">검색 서비스 쿼리 키 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="77704-117">Search Service query key name.</span></span>

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

### <span data-ttu-id="77704-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="77704-118">-ParentObject</span></span>
<span data-ttu-id="77704-119">검색 서비스 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="77704-119">Search Service Input Object.</span></span>

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

### <span data-ttu-id="77704-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="77704-120">-ParentResourceId</span></span>
<span data-ttu-id="77704-121">검색 서비스 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="77704-121">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="77704-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77704-122">-ResourceGroupName</span></span>
<span data-ttu-id="77704-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="77704-123">Resource Group name.</span></span>

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

### <span data-ttu-id="77704-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="77704-124">-ServiceName</span></span>
<span data-ttu-id="77704-125">검색 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="77704-125">Search Service name.</span></span>

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

### <span data-ttu-id="77704-126">-확인</span><span class="sxs-lookup"><span data-stu-id="77704-126">-Confirm</span></span>
<span data-ttu-id="77704-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="77704-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77704-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77704-128">-WhatIf</span></span>
<span data-ttu-id="77704-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="77704-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="77704-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="77704-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77704-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77704-131">CommonParameters</span></span>
<span data-ttu-id="77704-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="77704-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77704-133">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77704-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77704-134">입력</span><span class="sxs-lookup"><span data-stu-id="77704-134">INPUTS</span></span>

### <span data-ttu-id="77704-135">Microsoft. Azure. PSSearchService를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="77704-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="77704-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="77704-136">System.String</span></span>

## <span data-ttu-id="77704-137">출력</span><span class="sxs-lookup"><span data-stu-id="77704-137">OUTPUTS</span></span>

### <span data-ttu-id="77704-138">PSSearchQueryKey를 검색 하는 경우.</span><span class="sxs-lookup"><span data-stu-id="77704-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="77704-139">상속자</span><span class="sxs-lookup"><span data-stu-id="77704-139">NOTES</span></span>

## <span data-ttu-id="77704-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="77704-140">RELATED LINKS</span></span>

[<span data-ttu-id="77704-141">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="77704-141">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)

[<span data-ttu-id="77704-142">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="77704-142">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)
