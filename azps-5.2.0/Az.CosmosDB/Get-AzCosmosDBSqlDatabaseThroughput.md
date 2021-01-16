---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: 7c3dea3fc8f7fd6bf4870e68e242917421647661
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333722"
---
# <span data-ttu-id="f692e-101">Get-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="f692e-101">Get-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="f692e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f692e-102">SYNOPSIS</span></span>
<span data-ttu-id="f692e-103">CosmosDB Sql Database에 해당하는 처리 데이터 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f692e-103">Gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="f692e-104">구문</span><span class="sxs-lookup"><span data-stu-id="f692e-104">SYNTAX</span></span>

### <span data-ttu-id="f692e-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f692e-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f692e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f692e-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f692e-107">설명</span><span class="sxs-lookup"><span data-stu-id="f692e-107">DESCRIPTION</span></span>
<span data-ttu-id="f692e-108">**Get-AzCosmosDBSqlDatabaseThroughput** cmdlet은 CosmosDB Sql Database에 해당하는 처리 데이터 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f692e-108">The **Get-AzCosmosDBSqlDatabaseThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="f692e-109">예제</span><span class="sxs-lookup"><span data-stu-id="f692e-109">EXAMPLES</span></span>

### <span data-ttu-id="f692e-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="f692e-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabaseThroughput -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                : {throughputResourceName}
Id                  : {throughputId}
Throughput          : 0
MinimumThroughput   :
OfferReplacePending :
```

## <span data-ttu-id="f692e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f692e-111">PARAMETERS</span></span>

### <span data-ttu-id="f692e-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f692e-112">-AccountName</span></span>
<span data-ttu-id="f692e-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f692e-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f692e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f692e-114">-DefaultProfile</span></span>
<span data-ttu-id="f692e-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f692e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f692e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f692e-116">-InputObject</span></span>
<span data-ttu-id="f692e-117">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="f692e-117">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f692e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f692e-118">-Name</span></span>
<span data-ttu-id="f692e-119">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f692e-119">Database name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f692e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f692e-120">-ResourceGroupName</span></span>
<span data-ttu-id="f692e-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f692e-121">Name of resource group.</span></span>

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

### <span data-ttu-id="f692e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f692e-122">CommonParameters</span></span>
<span data-ttu-id="f692e-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f692e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f692e-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f692e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f692e-125">입력</span><span class="sxs-lookup"><span data-stu-id="f692e-125">INPUTS</span></span>

### <span data-ttu-id="f692e-126">없음</span><span class="sxs-lookup"><span data-stu-id="f692e-126">None</span></span>

## <span data-ttu-id="f692e-127">출력</span><span class="sxs-lookup"><span data-stu-id="f692e-127">OUTPUTS</span></span>

### <span data-ttu-id="f692e-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="f692e-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="f692e-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f692e-129">NOTES</span></span>

## <span data-ttu-id="f692e-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f692e-130">RELATED LINKS</span></span>
