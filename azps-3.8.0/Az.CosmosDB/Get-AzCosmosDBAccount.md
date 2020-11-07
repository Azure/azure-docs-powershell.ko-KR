---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccount.md
ms.openlocfilehash: 5c6dffe65022fa0282ab53bb04efe651ec123c2d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877882"
---
# <span data-ttu-id="926b3-101">Get-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="926b3-101">Get-AzCosmosDBAccount</span></span>

## <span data-ttu-id="926b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="926b3-102">SYNOPSIS</span></span>
<span data-ttu-id="926b3-103">CosmosDB 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="926b3-103">Get CosmosDB Account.</span></span>

## <span data-ttu-id="926b3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="926b3-104">SYNTAX</span></span>

### <span data-ttu-id="926b3-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="926b3-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="926b3-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="926b3-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="926b3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="926b3-107">DESCRIPTION</span></span>
<span data-ttu-id="926b3-108">**AzCosmosDBAccount** cmdlet은 지정 된 ResourceGroupName에 대 한 모든 기존 CosmosDB 계정 목록을 가져오고 지정 된 ResourceGroupName 및 AccountName에 대 한 단일 CosmosDB 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="926b3-108">The **Get-AzCosmosDBAccount** cmdlet gets the list of all existing CosmosDB accounts for a given ResourceGroupName and gets a single CosmosDB account for a given ResourceGroupName and AccountName.</span></span>

## <span data-ttu-id="926b3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="926b3-109">EXAMPLES</span></span>

### <span data-ttu-id="926b3-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="926b3-110">Example 1</span></span>
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
```

<span data-ttu-id="926b3-111">ResourceGroup resourceGroupName에 name databaseAccountName을 사용 하 여 CosmosDB 데이터베이스 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="926b3-111">Get CosmosDB database account with name databaseAccountName in ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="926b3-112">변수</span><span class="sxs-lookup"><span data-stu-id="926b3-112">PARAMETERS</span></span>

### <span data-ttu-id="926b3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="926b3-113">-DefaultProfile</span></span>
<span data-ttu-id="926b3-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="926b3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="926b3-115">-이름</span><span class="sxs-lookup"><span data-stu-id="926b3-115">-Name</span></span>
<span data-ttu-id="926b3-116">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="926b3-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="926b3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="926b3-117">-ResourceGroupName</span></span>
<span data-ttu-id="926b3-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="926b3-118">Name of resource group.</span></span>

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

### <span data-ttu-id="926b3-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="926b3-119">-ResourceId</span></span>
<span data-ttu-id="926b3-120">리소스의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="926b3-120">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="926b3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="926b3-121">CommonParameters</span></span>
<span data-ttu-id="926b3-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="926b3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="926b3-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="926b3-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="926b3-124">입력</span><span class="sxs-lookup"><span data-stu-id="926b3-124">INPUTS</span></span>

### <span data-ttu-id="926b3-125">않아야</span><span class="sxs-lookup"><span data-stu-id="926b3-125">None</span></span>

## <span data-ttu-id="926b3-126">출력</span><span class="sxs-lookup"><span data-stu-id="926b3-126">OUTPUTS</span></span>

### <span data-ttu-id="926b3-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="926b3-127">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="926b3-128">상속자</span><span class="sxs-lookup"><span data-stu-id="926b3-128">NOTES</span></span>

## <span data-ttu-id="926b3-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="926b3-129">RELATED LINKS</span></span>
