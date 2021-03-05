---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/get-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchService.md
ms.openlocfilehash: f4f360cc7fd9151735f131878565a09933f1be54
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963680"
---
# <span data-ttu-id="e36c5-101">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="e36c5-101">Get-AzSearchService</span></span>

## <span data-ttu-id="e36c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e36c5-102">SYNOPSIS</span></span>
<span data-ttu-id="e36c5-103">Azure Cognitive Search 서비스를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="e36c5-103">Gets an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="e36c5-104">구문</span><span class="sxs-lookup"><span data-stu-id="e36c5-104">SYNTAX</span></span>

### <span data-ttu-id="e36c5-105">ResourceGroupParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e36c5-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzSearchService [-ResourceGroupName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e36c5-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e36c5-106">ResourceIdParameterSet</span></span>
```
Get-AzSearchService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e36c5-107">설명</span><span class="sxs-lookup"><span data-stu-id="e36c5-107">DESCRIPTION</span></span>
<span data-ttu-id="e36c5-108">**Get-AzSearchService** cmdlet은 지정된 Azure Cognitive Search 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e36c5-108">The **Get-AzSearchService** cmdlet gets the specified Azure Cognitive Search service.</span></span>

## <span data-ttu-id="e36c5-109">예제</span><span class="sxs-lookup"><span data-stu-id="e36c5-109">EXAMPLES</span></span>

### <span data-ttu-id="e36c5-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e36c5-110">Example 1</span></span>
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

<span data-ttu-id="e36c5-111">지정된 매개 변수를 사용하여 Azure Cognitive Search 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e36c5-111">Get an Azure Cognitive Search service with specified parameters.</span></span>

## <span data-ttu-id="e36c5-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e36c5-112">PARAMETERS</span></span>

### <span data-ttu-id="e36c5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e36c5-113">-DefaultProfile</span></span>
<span data-ttu-id="e36c5-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e36c5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e36c5-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e36c5-115">-Name</span></span>
<span data-ttu-id="e36c5-116">Azure Cognitive Search Service 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e36c5-116">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="e36c5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e36c5-117">-ResourceGroupName</span></span>
<span data-ttu-id="e36c5-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e36c5-118">Resource Group name.</span></span>

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

### <span data-ttu-id="e36c5-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e36c5-119">-ResourceId</span></span>
<span data-ttu-id="e36c5-120">Azure Cognitive Search 서비스 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e36c5-120">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="e36c5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e36c5-121">CommonParameters</span></span>
<span data-ttu-id="e36c5-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e36c5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e36c5-123">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e36c5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e36c5-124">입력</span><span class="sxs-lookup"><span data-stu-id="e36c5-124">INPUTS</span></span>

### <span data-ttu-id="e36c5-125">System.String</span><span class="sxs-lookup"><span data-stu-id="e36c5-125">System.String</span></span>

## <span data-ttu-id="e36c5-126">출력</span><span class="sxs-lookup"><span data-stu-id="e36c5-126">OUTPUTS</span></span>

### <span data-ttu-id="e36c5-127">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="e36c5-127">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="e36c5-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e36c5-128">NOTES</span></span>

## <span data-ttu-id="e36c5-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e36c5-129">RELATED LINKS</span></span>

[<span data-ttu-id="e36c5-130">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="e36c5-130">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="e36c5-131">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="e36c5-131">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="e36c5-132">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="e36c5-132">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)