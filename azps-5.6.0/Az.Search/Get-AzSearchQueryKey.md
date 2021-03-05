---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/get-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
ms.openlocfilehash: 9bd662c5164660f6bc330e3b2ee2eced2893dbce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988848"
---
# <span data-ttu-id="6ef85-101">Get-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="6ef85-101">Get-AzSearchQueryKey</span></span>

## <span data-ttu-id="6ef85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ef85-102">SYNOPSIS</span></span>
<span data-ttu-id="6ef85-103">Azure Cognitive Search 서비스의 쿼리 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6ef85-103">Gets query key(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="6ef85-104">구문</span><span class="sxs-lookup"><span data-stu-id="6ef85-104">SYNTAX</span></span>

### <span data-ttu-id="6ef85-105">ResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6ef85-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ef85-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ef85-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6ef85-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ef85-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6ef85-108">설명</span><span class="sxs-lookup"><span data-stu-id="6ef85-108">DESCRIPTION</span></span>
<span data-ttu-id="6ef85-109">**Get-AzSearchQueryKey** cmdlet은 Azure Cognitive Search 서비스의 쿼리 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6ef85-109">The **Get-AzSearchQueryKey** cmdlet gets query key(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="6ef85-110">예제</span><span class="sxs-lookup"><span data-stu-id="6ef85-110">EXAMPLES</span></span>

### <span data-ttu-id="6ef85-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6ef85-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="6ef85-112">이 예제에서는 Azure Cognitive Search 서비스의 모든 쿼리 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6ef85-112">The example gets all query key(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="6ef85-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6ef85-113">PARAMETERS</span></span>

### <span data-ttu-id="6ef85-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ef85-114">-DefaultProfile</span></span>
<span data-ttu-id="6ef85-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6ef85-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ef85-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6ef85-116">-ParentObject</span></span>
<span data-ttu-id="6ef85-117">Azure Cognitive Search Service 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6ef85-117">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="6ef85-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6ef85-118">-ParentResourceId</span></span>
<span data-ttu-id="6ef85-119">Azure Cognitive Search 서비스 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6ef85-119">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="6ef85-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ef85-120">-ResourceGroupName</span></span>
<span data-ttu-id="6ef85-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ef85-121">Resource Group name.</span></span>

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

### <span data-ttu-id="6ef85-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6ef85-122">-ServiceName</span></span>
<span data-ttu-id="6ef85-123">Azure Cognitive Search Service 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ef85-123">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="6ef85-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ef85-124">CommonParameters</span></span>
<span data-ttu-id="6ef85-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6ef85-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ef85-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6ef85-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ef85-127">입력</span><span class="sxs-lookup"><span data-stu-id="6ef85-127">INPUTS</span></span>

### <span data-ttu-id="6ef85-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="6ef85-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="6ef85-129">System.String</span><span class="sxs-lookup"><span data-stu-id="6ef85-129">System.String</span></span>

## <span data-ttu-id="6ef85-130">출력</span><span class="sxs-lookup"><span data-stu-id="6ef85-130">OUTPUTS</span></span>

### <span data-ttu-id="6ef85-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="6ef85-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="6ef85-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6ef85-132">NOTES</span></span>

## <span data-ttu-id="6ef85-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6ef85-133">RELATED LINKS</span></span>

[<span data-ttu-id="6ef85-134">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="6ef85-134">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="6ef85-135">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="6ef85-135">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)