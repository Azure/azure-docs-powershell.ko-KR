---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
ms.openlocfilehash: 6df8d425967133e50dc45e44b6d567aca58465a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004384"
---
# <span data-ttu-id="4b693-101">Get-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="4b693-101">Get-AzCosmosDBAccount</span></span>

## <span data-ttu-id="4b693-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b693-102">SYNOPSIS</span></span>
<span data-ttu-id="4b693-103">CosmosDB 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4b693-103">Get CosmosDB Account.</span></span>

## <span data-ttu-id="4b693-104">구문</span><span class="sxs-lookup"><span data-stu-id="4b693-104">SYNTAX</span></span>

### <span data-ttu-id="4b693-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="4b693-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4b693-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b693-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b693-107">설명</span><span class="sxs-lookup"><span data-stu-id="4b693-107">DESCRIPTION</span></span>
<span data-ttu-id="4b693-108">**Get-AzCosmosDBAccount** cmdlet은 주어진 ResourceGroupName에 대한 모든 기존 CosmosDB 계정 목록을 얻게 며, 주어진 ResourceGroupName 및 AccountName에 대한 단일 CosmosDB 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4b693-108">The **Get-AzCosmosDBAccount** cmdlet gets the list of all existing CosmosDB accounts for a given ResourceGroupName and gets a single CosmosDB account for a given ResourceGroupName and AccountName.</span></span>

## <span data-ttu-id="4b693-109">예제</span><span class="sxs-lookup"><span data-stu-id="4b693-109">EXAMPLES</span></span>

### <span data-ttu-id="4b693-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="4b693-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBAccount -ResourceGroupName {resourceGroupName} -Name {databaseAccountName}


Id                            : /subscriptions/{subscriptionid}/resourceGroups/{resourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{databaseAccountName}
Name                          : {databaseAccountName}
FailoverPolicies              : {databaseAccountName-region1}
ReadLocations                 : {databaseAccountName-region1}
WriteLocations                : {databaseAccountName-region1}
Capabilities                  : {}
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Models.ConsistencyPolicy
EnableAutomaticFailover       : False
IsVirtualNetworkFilterEnabled : False
IpRangeFilter                 :
DatabaseAccountOfferType      : Standard
DocumentEndpoint              : https://databaseAccountName.documents.azure.com:443/
ProvisioningState             : Succeeded
Kind                          : GlobalDocumentDB
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : False
NetworkAclBypass              : None
NetworkAclBypassResourceIds   : {}
```

<span data-ttu-id="4b693-111">ResourceGroup resourceGroupName에서 이름 데이터베이스AccountName을 통해 CosmosDB 데이터베이스 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4b693-111">Get CosmosDB database account with name databaseAccountName in ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="4b693-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4b693-112">PARAMETERS</span></span>

### <span data-ttu-id="4b693-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b693-113">-DefaultProfile</span></span>
<span data-ttu-id="4b693-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4b693-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b693-115">-Name</span><span class="sxs-lookup"><span data-stu-id="4b693-115">-Name</span></span>
<span data-ttu-id="4b693-116">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b693-116">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b693-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b693-117">-ResourceGroupName</span></span>
<span data-ttu-id="4b693-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b693-118">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b693-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4b693-119">-ResourceId</span></span>
<span data-ttu-id="4b693-120">리소스의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="4b693-120">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b693-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b693-121">CommonParameters</span></span>
<span data-ttu-id="4b693-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4b693-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b693-123">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b693-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b693-124">입력</span><span class="sxs-lookup"><span data-stu-id="4b693-124">INPUTS</span></span>

### <span data-ttu-id="4b693-125">없음</span><span class="sxs-lookup"><span data-stu-id="4b693-125">None</span></span>

## <span data-ttu-id="4b693-126">출력</span><span class="sxs-lookup"><span data-stu-id="4b693-126">OUTPUTS</span></span>

### <span data-ttu-id="4b693-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="4b693-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="4b693-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4b693-128">NOTES</span></span>

## <span data-ttu-id="4b693-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4b693-129">RELATED LINKS</span></span>
