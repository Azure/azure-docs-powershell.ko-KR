---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchService.md
ms.openlocfilehash: e4751232969c407484b978d495d348dc61810715
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048762"
---
# <span data-ttu-id="4d650-101">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="4d650-101">Get-AzSearchService</span></span>

## <span data-ttu-id="4d650-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d650-102">SYNOPSIS</span></span>
<span data-ttu-id="4d650-103">Azure Search 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4d650-103">Gets an Azure Search service.</span></span>

## <span data-ttu-id="4d650-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4d650-104">SYNTAX</span></span>

### <span data-ttu-id="4d650-105">ResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="4d650-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSearchService [-ResourceGroupName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4d650-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d650-106">ResourceIdParameterSet</span></span>
```
Get-AzSearchService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d650-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4d650-107">DESCRIPTION</span></span>
<span data-ttu-id="4d650-108">**AzSearchService** cmdlet은 지정 된 Azure Search 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4d650-108">The **Get-AzSearchService** cmdlet gets the specified Azure Search service.</span></span>

## <span data-ttu-id="4d650-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4d650-109">EXAMPLES</span></span>

### <span data-ttu-id="4d650-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="4d650-110">Example 1</span></span>
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

<span data-ttu-id="4d650-111">지정 된 매개 변수를 사용 하 여 Azure Search 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4d650-111">Get an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="4d650-112">변수</span><span class="sxs-lookup"><span data-stu-id="4d650-112">PARAMETERS</span></span>

### <span data-ttu-id="4d650-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d650-113">-DefaultProfile</span></span>
<span data-ttu-id="4d650-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4d650-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d650-115">-이름</span><span class="sxs-lookup"><span data-stu-id="4d650-115">-Name</span></span>
<span data-ttu-id="4d650-116">검색 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d650-116">Search Service name.</span></span>

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

### <span data-ttu-id="4d650-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d650-117">-ResourceGroupName</span></span>
<span data-ttu-id="4d650-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d650-118">Resource Group name.</span></span>

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

### <span data-ttu-id="4d650-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d650-119">-ResourceId</span></span>
<span data-ttu-id="4d650-120">검색 서비스 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="4d650-120">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="4d650-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d650-121">CommonParameters</span></span>
<span data-ttu-id="4d650-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d650-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d650-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d650-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d650-124">입력</span><span class="sxs-lookup"><span data-stu-id="4d650-124">INPUTS</span></span>

### <span data-ttu-id="4d650-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4d650-125">System.String</span></span>

## <span data-ttu-id="4d650-126">출력</span><span class="sxs-lookup"><span data-stu-id="4d650-126">OUTPUTS</span></span>

### <span data-ttu-id="4d650-127">Microsoft. Azure. PSSearchService를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d650-127">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="4d650-128">상속자</span><span class="sxs-lookup"><span data-stu-id="4d650-128">NOTES</span></span>

## <span data-ttu-id="4d650-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4d650-129">RELATED LINKS</span></span>

[<span data-ttu-id="4d650-130">새로운 AzSearchService</span><span class="sxs-lookup"><span data-stu-id="4d650-130">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="4d650-131">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="4d650-131">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="4d650-132">제거-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="4d650-132">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)