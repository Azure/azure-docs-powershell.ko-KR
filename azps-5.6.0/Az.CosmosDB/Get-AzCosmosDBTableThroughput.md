---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 7b48190a9ef01d468e762d93d7bc63a96e831de8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986874"
---
# <span data-ttu-id="0ba5e-101">Get-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="0ba5e-101">Get-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="0ba5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ba5e-102">SYNOPSIS</span></span>
<span data-ttu-id="0ba5e-103">CosmosDB 테이블의 진행을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0ba5e-103">Gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="0ba5e-104">구문</span><span class="sxs-lookup"><span data-stu-id="0ba5e-104">SYNTAX</span></span>

### <span data-ttu-id="0ba5e-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="0ba5e-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTableThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ba5e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ba5e-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTableThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ba5e-107">설명</span><span class="sxs-lookup"><span data-stu-id="0ba5e-107">DESCRIPTION</span></span>
<span data-ttu-id="0ba5e-108">**Get-AzCosmosDBTableThroughput** cmdlet은 CosmosDB 테이블의 프로비전을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0ba5e-108">The **Get-AzCosmosDBTableThroughput** cmdlet gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="0ba5e-109">예제</span><span class="sxs-lookup"><span data-stu-id="0ba5e-109">EXAMPLES</span></span>

### <span data-ttu-id="0ba5e-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="0ba5e-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTableThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="0ba5e-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0ba5e-111">PARAMETERS</span></span>

### <span data-ttu-id="0ba5e-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0ba5e-112">-AccountName</span></span>
<span data-ttu-id="0ba5e-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ba5e-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0ba5e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ba5e-114">-DefaultProfile</span></span>
<span data-ttu-id="0ba5e-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0ba5e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ba5e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ba5e-116">-InputObject</span></span>
<span data-ttu-id="0ba5e-117">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="0ba5e-117">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ba5e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="0ba5e-118">-Name</span></span>
<span data-ttu-id="0ba5e-119">표의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ba5e-119">Name of the Table.</span></span>

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

### <span data-ttu-id="0ba5e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ba5e-120">-ResourceGroupName</span></span>
<span data-ttu-id="0ba5e-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ba5e-121">Name of resource group.</span></span>

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

### <span data-ttu-id="0ba5e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ba5e-122">CommonParameters</span></span>
<span data-ttu-id="0ba5e-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0ba5e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ba5e-124">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ba5e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ba5e-125">입력</span><span class="sxs-lookup"><span data-stu-id="0ba5e-125">INPUTS</span></span>

### <span data-ttu-id="0ba5e-126">없음</span><span class="sxs-lookup"><span data-stu-id="0ba5e-126">None</span></span>

## <span data-ttu-id="0ba5e-127">출력</span><span class="sxs-lookup"><span data-stu-id="0ba5e-127">OUTPUTS</span></span>

### <span data-ttu-id="0ba5e-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="0ba5e-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="0ba5e-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0ba5e-129">NOTES</span></span>

## <span data-ttu-id="0ba5e-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ba5e-130">RELATED LINKS</span></span>
