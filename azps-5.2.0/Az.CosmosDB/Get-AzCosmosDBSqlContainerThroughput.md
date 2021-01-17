---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainerthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
ms.openlocfilehash: f4e830cbcaab74b3cc70b201fd0f7f0557f2e840
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351170"
---
# <span data-ttu-id="d1814-101">Get-AzCosmosDBSqlContainerThroughput</span><span class="sxs-lookup"><span data-stu-id="d1814-101">Get-AzCosmosDBSqlContainerThroughput</span></span>

## <span data-ttu-id="d1814-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1814-102">SYNOPSIS</span></span>
<span data-ttu-id="d1814-103">CosmosDB Sql 컨테이너에 해당하는 처리 데이터 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d1814-103">Gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span>

## <span data-ttu-id="d1814-104">구문</span><span class="sxs-lookup"><span data-stu-id="d1814-104">SYNTAX</span></span>

### <span data-ttu-id="d1814-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d1814-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainerThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1814-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1814-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainerThroughput [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1814-107">설명</span><span class="sxs-lookup"><span data-stu-id="d1814-107">DESCRIPTION</span></span>
<span data-ttu-id="d1814-108">**Get-AzCosmosDBSqlContainerThroughput** cmdlet은 CosmosDB Sql 컨테이너에 해당하는 처리 데이터 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d1814-108">The **Get-AzCosmosDBSqlContainerThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span> 

## <span data-ttu-id="d1814-109">예제</span><span class="sxs-lookup"><span data-stu-id="d1814-109">EXAMPLES</span></span>

### <span data-ttu-id="d1814-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="d1814-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainerThroughput  -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {containerName}

Throughput          : {throughputValue}
MinimumThroughput   :
OfferReplacePending :
Id                  : 
Name                : {Name}
Type                : Microsoft.DocumentDB/databaseAccounts/sqlDatabases/containers/throughputSettings
Location            :
Tags                :
```

## <span data-ttu-id="d1814-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1814-111">PARAMETERS</span></span>

### <span data-ttu-id="d1814-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d1814-112">-AccountName</span></span>
<span data-ttu-id="d1814-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d1814-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d1814-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d1814-114">-DatabaseName</span></span>
<span data-ttu-id="d1814-115">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d1814-115">Database name.</span></span>

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

### <span data-ttu-id="d1814-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1814-116">-DefaultProfile</span></span>
<span data-ttu-id="d1814-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d1814-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1814-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1814-118">-InputObject</span></span>
<span data-ttu-id="d1814-119">Sql Container 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d1814-119">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1814-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d1814-120">-Name</span></span>
<span data-ttu-id="d1814-121">컨테이너 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d1814-121">Container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1814-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1814-122">-ResourceGroupName</span></span>
<span data-ttu-id="d1814-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d1814-123">Name of resource group.</span></span>

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

### <span data-ttu-id="d1814-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1814-124">CommonParameters</span></span>
<span data-ttu-id="d1814-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d1814-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1814-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d1814-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1814-127">입력</span><span class="sxs-lookup"><span data-stu-id="d1814-127">INPUTS</span></span>

### <span data-ttu-id="d1814-128">없음</span><span class="sxs-lookup"><span data-stu-id="d1814-128">None</span></span>

## <span data-ttu-id="d1814-129">출력</span><span class="sxs-lookup"><span data-stu-id="d1814-129">OUTPUTS</span></span>

### <span data-ttu-id="d1814-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="d1814-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="d1814-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d1814-131">NOTES</span></span>

## <span data-ttu-id="d1814-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1814-132">RELATED LINKS</span></span>