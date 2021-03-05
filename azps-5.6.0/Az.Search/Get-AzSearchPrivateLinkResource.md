---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/get-AzSearchPrivateLinkResource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchPrivateLinkResource.md
ms.openlocfilehash: a04af740a320d2550eb3fb4668689328bbe60857
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963728"
---
# <span data-ttu-id="3723f-101">Get-AzSearchPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="3723f-101">Get-AzSearchPrivateLinkResource</span></span>

## <span data-ttu-id="3723f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3723f-102">SYNOPSIS</span></span>
<span data-ttu-id="3723f-103">Azure Cognitive Search 서비스에 대한 개인 링크 리소스 세부 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3723f-103">Gets private link resource details for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="3723f-104">구문</span><span class="sxs-lookup"><span data-stu-id="3723f-104">SYNTAX</span></span>

### <span data-ttu-id="3723f-105">ResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="3723f-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchPrivateLinkResource [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3723f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3723f-106">ResourceIdParameterSet</span></span>
```
Get-AzSearchPrivateLinkResource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3723f-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3723f-107">InputObjectParameterSet</span></span>
```
Get-AzSearchPrivateLinkResource [-InputObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3723f-108">설명</span><span class="sxs-lookup"><span data-stu-id="3723f-108">DESCRIPTION</span></span>
<span data-ttu-id="3723f-109">**Get-AzSearchPrivateLinkResource** cmdlet은 Azure Cognitive Search 서비스에 대한 개인 링크 리소스 세부 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="3723f-109">The **Get-AzSearchPrivateLinkResource** cmdlet gets private link resource details for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="3723f-110">예제</span><span class="sxs-lookup"><span data-stu-id="3723f-110">EXAMPLES</span></span>

### <span data-ttu-id="3723f-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="3723f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchPrivateLinkResource -ResourceGroupName arjagann -Name arjagann-test-cuseuap | ConvertTo-Json

  "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/privateLinkResources/searchService",
  "Type": "Microsoft.Search/searchServices/privateLinkResources",
  "GroupId": "searchService",
  "RequiredMembers": [
    "searchService"
  ],
  "RequiredZoneNames": [
    "privatelink.search-dogfood.windows-int.net"
  ],
  "ShareablePrivateLinkResourceTypes": [
    {
      "Name": "blob",
      "Description": "Azure Cognitive Search indexers can connect to blobs in Azure Storage for reading data (data source), for writing intermediate results of indexer execution (annotation cache, preview) or for storing any knowledge store projections (preview)",
      "Type": "Microsoft.Storage/storageAccounts",
      "GroupId": "blob"
    },
    {
      "Name": "table",
      "Description": "Azure Cognitive Search indexers can connect to tables in Azure Storage for reading data (data source), for writing book-keeping information about intermediate results of indexer execution (annotation cache, preview) or for storing any knowledge store projections (preview)",
      "Type": "Microsoft.Storage/storageAccounts",
      "GroupId": "table"
    },
    {
      "Name": "Sql",
      "Description": "Azure Cognitive Search indexers can connect to CosmosDB using the SQL head for reading data (data source).",
      "Type": "Microsoft.DocumentDB/databaseAccounts",
      "GroupId": "Sql"
    },
    {
      "Name": "plr",
      "Description": "Azure Cognitive Search indexers can connect to AzureSQL databases in a SQL server for reading data (data source).",
      "Type": "Microsoft.Sql/servers",
      "GroupId": "sqlServer"
    },
    {
      "Name": "vault",
      "Description": "Azure Cognitive Search can access keys in Azure Key Vault to encrypt search index and synonym map data",
      "Type": "Microsoft.KeyVault/vaults",
      "GroupId": "vault"
    }
  ]
}
```

<span data-ttu-id="3723f-112">이 예제에서는 Azure Cognitive Search 서비스에 대한 개인 링크 리소스 세부 정보(편의를 위해 JSON 양식)를 제공하는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="3723f-112">The example shows how to get the private link resource details (in JSON form for convenience) for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="3723f-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3723f-113">PARAMETERS</span></span>

### <span data-ttu-id="3723f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3723f-114">-DefaultProfile</span></span>
<span data-ttu-id="3723f-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3723f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3723f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3723f-116">-InputObject</span></span>
<span data-ttu-id="3723f-117">Azure Cognitive Search Service 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3723f-117">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3723f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="3723f-118">-Name</span></span>
<span data-ttu-id="3723f-119">Azure Cognitive Search Service 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3723f-119">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="3723f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3723f-120">-ResourceGroupName</span></span>
<span data-ttu-id="3723f-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3723f-121">Resource Group name.</span></span>

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

### <span data-ttu-id="3723f-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3723f-122">-ResourceId</span></span>
<span data-ttu-id="3723f-123">Azure Cognitive Search 서비스 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3723f-123">Azure Cognitive Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3723f-124">-확인</span><span class="sxs-lookup"><span data-stu-id="3723f-124">-Confirm</span></span>
<span data-ttu-id="3723f-125">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3723f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3723f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3723f-126">-WhatIf</span></span>
<span data-ttu-id="3723f-127">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="3723f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3723f-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3723f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3723f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3723f-129">CommonParameters</span></span>
<span data-ttu-id="3723f-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3723f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3723f-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3723f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3723f-132">입력</span><span class="sxs-lookup"><span data-stu-id="3723f-132">INPUTS</span></span>

### <span data-ttu-id="3723f-133">없음</span><span class="sxs-lookup"><span data-stu-id="3723f-133">None</span></span>

## <span data-ttu-id="3723f-134">출력</span><span class="sxs-lookup"><span data-stu-id="3723f-134">OUTPUTS</span></span>

### <span data-ttu-id="3723f-135">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="3723f-135">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="3723f-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3723f-136">NOTES</span></span>

## <span data-ttu-id="3723f-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3723f-137">RELATED LINKS</span></span>

[<span data-ttu-id="3723f-138">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="3723f-138">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="3723f-139">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="3723f-139">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="3723f-140">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="3723f-140">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="3723f-141">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="3723f-141">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)