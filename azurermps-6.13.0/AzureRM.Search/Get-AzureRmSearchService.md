---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/get-azurermsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchService.md
ms.openlocfilehash: 57b09ea3267447f16ceadf4d1eae51f997c53a82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528385"
---
# <span data-ttu-id="6df4e-101">Get-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="6df4e-101">Get-AzureRmSearchService</span></span>

## <span data-ttu-id="6df4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6df4e-102">SYNOPSIS</span></span>
<span data-ttu-id="6df4e-103">Azure Search 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6df4e-103">Gets an Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6df4e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6df4e-104">SYNTAX</span></span>

### <span data-ttu-id="6df4e-105">ResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="6df4e-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmSearchService [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6df4e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6df4e-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmSearchService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6df4e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6df4e-107">DESCRIPTION</span></span>
<span data-ttu-id="6df4e-108">**AzureRmSearchService** cmdlet은 지정 된 Azure Search 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6df4e-108">The **Get-AzureRmSearchService** cmdlet gets the specified Azure Search service.</span></span>

## <span data-ttu-id="6df4e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6df4e-109">EXAMPLES</span></span>

### <span data-ttu-id="6df4e-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="6df4e-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSearchService -ResourceGroupName felixwa-01


ResourceGroupName : felixwa-01
Name              : felixwa-basic-search
Location          : West US
Sku               : Basic
ReplicaCount      : 1
PartitionCount    : 1
HostingMode       : Default
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/felixwa-01/providers/Microsoft.Search/searchServices/felixwa-basic-search
```

<span data-ttu-id="6df4e-111">지정 된 매개 변수를 사용 하 여 Azure Search 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6df4e-111">Get an Azure Search service with specified parameters.</span></span>

## <span data-ttu-id="6df4e-112">변수</span><span class="sxs-lookup"><span data-stu-id="6df4e-112">PARAMETERS</span></span>

### <span data-ttu-id="6df4e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6df4e-113">-DefaultProfile</span></span>
<span data-ttu-id="6df4e-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6df4e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6df4e-115">-이름</span><span class="sxs-lookup"><span data-stu-id="6df4e-115">-Name</span></span>
<span data-ttu-id="6df4e-116">검색 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6df4e-116">Search Service name.</span></span>

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

### <span data-ttu-id="6df4e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6df4e-117">-ResourceGroupName</span></span>
<span data-ttu-id="6df4e-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6df4e-118">Resource Group name.</span></span>

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

### <span data-ttu-id="6df4e-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6df4e-119">-ResourceId</span></span>
<span data-ttu-id="6df4e-120">검색 서비스 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="6df4e-120">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="6df4e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6df4e-121">CommonParameters</span></span>
<span data-ttu-id="6df4e-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6df4e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6df4e-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6df4e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6df4e-124">입력</span><span class="sxs-lookup"><span data-stu-id="6df4e-124">INPUTS</span></span>

### <span data-ttu-id="6df4e-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6df4e-125">System.String</span></span>

## <span data-ttu-id="6df4e-126">출력</span><span class="sxs-lookup"><span data-stu-id="6df4e-126">OUTPUTS</span></span>

### <span data-ttu-id="6df4e-127">Microsoft. Azure. PSSearchService를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="6df4e-127">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="6df4e-128">상속자</span><span class="sxs-lookup"><span data-stu-id="6df4e-128">NOTES</span></span>

## <span data-ttu-id="6df4e-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6df4e-129">RELATED LINKS</span></span>

[<span data-ttu-id="6df4e-130">새로운 AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="6df4e-130">New-AzureRmSearchService</span></span>](./New-AzureRmSearchService.md)

[<span data-ttu-id="6df4e-131">Set-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="6df4e-131">Set-AzureRmSearchService</span></span>](./Set-AzureRmSearchService.md)

[<span data-ttu-id="6df4e-132">제거-AzureRmSearchService</span><span class="sxs-lookup"><span data-stu-id="6df4e-132">Remove-AzureRmSearchService</span></span>](./Remove-AzureRmSearchService.md)
