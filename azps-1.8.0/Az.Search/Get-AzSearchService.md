---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchService.md
ms.openlocfilehash: 9acd7be782d52e9b636b0445776defa95f83c1f9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699279"
---
# <span data-ttu-id="bf67b-101">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="bf67b-101">Get-AzSearchService</span></span>

## <span data-ttu-id="bf67b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf67b-102">SYNOPSIS</span></span>
<span data-ttu-id="bf67b-103">Azure Search 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bf67b-103">Gets an Azure Search service.</span></span>

## <span data-ttu-id="bf67b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bf67b-104">SYNTAX</span></span>

### <span data-ttu-id="bf67b-105">ResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="bf67b-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSearchService [-ResourceGroupName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bf67b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf67b-106">ResourceIdParameterSet</span></span>
```
Get-AzSearchService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf67b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="bf67b-107">DESCRIPTION</span></span>
<span data-ttu-id="bf67b-108">**AzSearchService** cmdlet은 지정 된 Azure Search 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bf67b-108">The **Get-AzSearchService** cmdlet gets the specified Azure Search service.</span></span>

## <span data-ttu-id="bf67b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="bf67b-109">EXAMPLES</span></span>

### <span data-ttu-id="bf67b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="bf67b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchService -ResourceGroupName felixwa-01


ResourceGroupName : felixwa-01
Name              : felixwa-basic-search
Location          : West US
Sku               : Basic
ReplicaCount      : 1
PartitionCount    : 1
HostingMode       : Default
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/felixwa-01/providers/Microsoft.Search/searchServices/felixwa-basic-search
```

<span data-ttu-id="bf67b-111">지정 된 매개 변수를 사용 하 여 Azure Search 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bf67b-111">Get an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="bf67b-112">변수</span><span class="sxs-lookup"><span data-stu-id="bf67b-112">PARAMETERS</span></span>

### <span data-ttu-id="bf67b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf67b-113">-DefaultProfile</span></span>
<span data-ttu-id="bf67b-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bf67b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf67b-115">-이름</span><span class="sxs-lookup"><span data-stu-id="bf67b-115">-Name</span></span>
<span data-ttu-id="bf67b-116">검색 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bf67b-116">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf67b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf67b-117">-ResourceGroupName</span></span>
<span data-ttu-id="bf67b-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bf67b-118">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf67b-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf67b-119">-ResourceId</span></span>
<span data-ttu-id="bf67b-120">검색 서비스 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="bf67b-120">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf67b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf67b-121">CommonParameters</span></span>
<span data-ttu-id="bf67b-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf67b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf67b-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf67b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf67b-124">입력</span><span class="sxs-lookup"><span data-stu-id="bf67b-124">INPUTS</span></span>

### <span data-ttu-id="bf67b-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bf67b-125">System.String</span></span>

## <span data-ttu-id="bf67b-126">출력</span><span class="sxs-lookup"><span data-stu-id="bf67b-126">OUTPUTS</span></span>

### <span data-ttu-id="bf67b-127">Microsoft. Azure. PSSearchService를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf67b-127">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="bf67b-128">상속자</span><span class="sxs-lookup"><span data-stu-id="bf67b-128">NOTES</span></span>

## <span data-ttu-id="bf67b-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bf67b-129">RELATED LINKS</span></span>

[<span data-ttu-id="bf67b-130">새로운 AzSearchService</span><span class="sxs-lookup"><span data-stu-id="bf67b-130">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="bf67b-131">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="bf67b-131">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="bf67b-132">제거-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="bf67b-132">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)