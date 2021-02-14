---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchService.md
ms.openlocfilehash: e5d65cb334070cdc5e861a2f90bd95277d41fab5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176364"
---
# <span data-ttu-id="d81c8-101">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="d81c8-101">Get-AzSearchService</span></span>

## <span data-ttu-id="d81c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d81c8-102">SYNOPSIS</span></span>
<span data-ttu-id="d81c8-103">Azure Cognitive Search 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d81c8-103">Gets an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="d81c8-104">구문</span><span class="sxs-lookup"><span data-stu-id="d81c8-104">SYNTAX</span></span>

### <span data-ttu-id="d81c8-105">ResourceGroupParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d81c8-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSearchService [-ResourceGroupName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d81c8-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d81c8-106">ResourceIdParameterSet</span></span>
```
Get-AzSearchService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d81c8-107">설명</span><span class="sxs-lookup"><span data-stu-id="d81c8-107">DESCRIPTION</span></span>
<span data-ttu-id="d81c8-108">**Get-AzSearchService** cmdlet은 지정된 Azure Cognitive Search 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d81c8-108">The **Get-AzSearchService** cmdlet gets the specified Azure Cognitive Search service.</span></span>

## <span data-ttu-id="d81c8-109">예제</span><span class="sxs-lookup"><span data-stu-id="d81c8-109">EXAMPLES</span></span>

### <span data-ttu-id="d81c8-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="d81c8-110">Example 1</span></span>
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

<span data-ttu-id="d81c8-111">지정된 매개 변수를 사용하여 Azure Cognitive Search 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d81c8-111">Get an Azure Cognitive Search service with specified parameters.</span></span>

## <span data-ttu-id="d81c8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d81c8-112">PARAMETERS</span></span>

### <span data-ttu-id="d81c8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d81c8-113">-DefaultProfile</span></span>
<span data-ttu-id="d81c8-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d81c8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d81c8-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d81c8-115">-Name</span></span>
<span data-ttu-id="d81c8-116">Azure Cognitive Search 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d81c8-116">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="d81c8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d81c8-117">-ResourceGroupName</span></span>
<span data-ttu-id="d81c8-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d81c8-118">Resource Group name.</span></span>

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

### <span data-ttu-id="d81c8-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d81c8-119">-ResourceId</span></span>
<span data-ttu-id="d81c8-120">Azure Cognitive Search 서비스 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d81c8-120">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="d81c8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d81c8-121">CommonParameters</span></span>
<span data-ttu-id="d81c8-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d81c8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d81c8-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d81c8-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d81c8-124">입력</span><span class="sxs-lookup"><span data-stu-id="d81c8-124">INPUTS</span></span>

### <span data-ttu-id="d81c8-125">System.String</span><span class="sxs-lookup"><span data-stu-id="d81c8-125">System.String</span></span>

## <span data-ttu-id="d81c8-126">출력</span><span class="sxs-lookup"><span data-stu-id="d81c8-126">OUTPUTS</span></span>

### <span data-ttu-id="d81c8-127">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="d81c8-127">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="d81c8-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d81c8-128">NOTES</span></span>

## <span data-ttu-id="d81c8-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d81c8-129">RELATED LINKS</span></span>

[<span data-ttu-id="d81c8-130">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="d81c8-130">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="d81c8-131">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="d81c8-131">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="d81c8-132">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="d81c8-132">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)