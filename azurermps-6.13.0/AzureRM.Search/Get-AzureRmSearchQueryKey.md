---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/get-azurermsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchQueryKey.md
ms.openlocfilehash: 3535e9d7723c87e0f528192e47c921d3835ff9e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528389"
---
# <span data-ttu-id="b375b-101">Get-AzureRmSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="b375b-101">Get-AzureRmSearchQueryKey</span></span>

## <span data-ttu-id="b375b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b375b-102">SYNOPSIS</span></span>
<span data-ttu-id="b375b-103">Azure Search 서비스의 쿼리 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b375b-103">Gets query key(s) of the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b375b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b375b-104">SYNTAX</span></span>

### <span data-ttu-id="b375b-105">ResourceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="b375b-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b375b-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b375b-106">ParentObjectParameterSet</span></span>
```
Get-AzureRmSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b375b-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b375b-107">ParentResourceIdParameterSet</span></span>
```
Get-AzureRmSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b375b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b375b-108">DESCRIPTION</span></span>
<span data-ttu-id="b375b-109">**AzureRmSearchQueryKey** Cmdlet은 Azure Search 서비스의 쿼리 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b375b-109">The **Get-AzureRmSearchQueryKey** cmdlet gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="b375b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b375b-110">EXAMPLES</span></span>

### <span data-ttu-id="b375b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b375b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="b375b-112">이 예제에서는 Azure Search 서비스의 모든 쿼리 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b375b-112">The example gets all query key(s) of the Azure Search Service.</span></span>

## <span data-ttu-id="b375b-113">변수</span><span class="sxs-lookup"><span data-stu-id="b375b-113">PARAMETERS</span></span>

### <span data-ttu-id="b375b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b375b-114">-DefaultProfile</span></span>
<span data-ttu-id="b375b-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b375b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b375b-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b375b-116">-ParentObject</span></span>
<span data-ttu-id="b375b-117">검색 서비스 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b375b-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="b375b-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b375b-118">-ParentResourceId</span></span>
<span data-ttu-id="b375b-119">검색 서비스 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="b375b-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="b375b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b375b-120">-ResourceGroupName</span></span>
<span data-ttu-id="b375b-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b375b-121">Resource Group name.</span></span>

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

### <span data-ttu-id="b375b-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b375b-122">-ServiceName</span></span>
<span data-ttu-id="b375b-123">검색 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b375b-123">Search Service name.</span></span>

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

### <span data-ttu-id="b375b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b375b-124">CommonParameters</span></span>
<span data-ttu-id="b375b-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b375b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b375b-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b375b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b375b-127">입력</span><span class="sxs-lookup"><span data-stu-id="b375b-127">INPUTS</span></span>

### <span data-ttu-id="b375b-128">Microsoft. Azure. PSSearchService를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="b375b-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="b375b-129">매개 변수: ParentObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b375b-129">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="b375b-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b375b-130">System.String</span></span>

## <span data-ttu-id="b375b-131">출력</span><span class="sxs-lookup"><span data-stu-id="b375b-131">OUTPUTS</span></span>

### <span data-ttu-id="b375b-132">PSSearchQueryKey를 검색 하는 경우.</span><span class="sxs-lookup"><span data-stu-id="b375b-132">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="b375b-133">상속자</span><span class="sxs-lookup"><span data-stu-id="b375b-133">NOTES</span></span>

## <span data-ttu-id="b375b-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b375b-134">RELATED LINKS</span></span>

[<span data-ttu-id="b375b-135">New-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="b375b-135">New-AzureRmSearchQueryKey.md</span></span>](./New-AzureRmSearchQueryKey.md)

[<span data-ttu-id="b375b-136">Remove-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="b375b-136">Remove-AzureRmSearchQueryKey.md</span></span>](./Remove-AzureRmSearchQueryKey.md)
