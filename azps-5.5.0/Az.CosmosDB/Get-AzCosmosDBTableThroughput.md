---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 7fc023ddd5a986cc71ce86c05967f5253a39b26d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181345"
---
# <span data-ttu-id="bc54d-101">Get-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="bc54d-101">Get-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="bc54d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc54d-102">SYNOPSIS</span></span>
<span data-ttu-id="bc54d-103">CosmosDB 테이블의 진행을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bc54d-103">Gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="bc54d-104">구문</span><span class="sxs-lookup"><span data-stu-id="bc54d-104">SYNTAX</span></span>

### <span data-ttu-id="bc54d-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="bc54d-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTableThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc54d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc54d-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTableThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc54d-107">설명</span><span class="sxs-lookup"><span data-stu-id="bc54d-107">DESCRIPTION</span></span>
<span data-ttu-id="bc54d-108">**Get-AzCosmosDBTableThroughput** cmdlet은 CosmosDB 테이블의 프로비전을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bc54d-108">The **Get-AzCosmosDBTableThroughput** cmdlet gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="bc54d-109">예제</span><span class="sxs-lookup"><span data-stu-id="bc54d-109">EXAMPLES</span></span>

### <span data-ttu-id="bc54d-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="bc54d-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTableThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="bc54d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc54d-111">PARAMETERS</span></span>

### <span data-ttu-id="bc54d-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bc54d-112">-AccountName</span></span>
<span data-ttu-id="bc54d-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc54d-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="bc54d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc54d-114">-DefaultProfile</span></span>
<span data-ttu-id="bc54d-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bc54d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc54d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc54d-116">-InputObject</span></span>
<span data-ttu-id="bc54d-117">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="bc54d-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="bc54d-118">-Name</span><span class="sxs-lookup"><span data-stu-id="bc54d-118">-Name</span></span>
<span data-ttu-id="bc54d-119">테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc54d-119">Name of the Table.</span></span>

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

### <span data-ttu-id="bc54d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc54d-120">-ResourceGroupName</span></span>
<span data-ttu-id="bc54d-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc54d-121">Name of resource group.</span></span>

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

### <span data-ttu-id="bc54d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc54d-122">CommonParameters</span></span>
<span data-ttu-id="bc54d-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bc54d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc54d-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bc54d-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc54d-125">입력</span><span class="sxs-lookup"><span data-stu-id="bc54d-125">INPUTS</span></span>

### <span data-ttu-id="bc54d-126">없음</span><span class="sxs-lookup"><span data-stu-id="bc54d-126">None</span></span>

## <span data-ttu-id="bc54d-127">출력</span><span class="sxs-lookup"><span data-stu-id="bc54d-127">OUTPUTS</span></span>

### <span data-ttu-id="bc54d-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="bc54d-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="bc54d-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bc54d-129">NOTES</span></span>

## <span data-ttu-id="bc54d-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bc54d-130">RELATED LINKS</span></span>
