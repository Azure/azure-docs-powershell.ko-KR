---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 7fc023ddd5a986cc71ce86c05967f5253a39b26d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307205"
---
# <span data-ttu-id="098ed-101">Get-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="098ed-101">Get-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="098ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="098ed-102">SYNOPSIS</span></span>
<span data-ttu-id="098ed-103">CosmosDB 테이블의 처리량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="098ed-103">Gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="098ed-104">구문과</span><span class="sxs-lookup"><span data-stu-id="098ed-104">SYNTAX</span></span>

### <span data-ttu-id="098ed-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="098ed-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTableThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="098ed-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="098ed-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTableThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="098ed-107">설명은</span><span class="sxs-lookup"><span data-stu-id="098ed-107">DESCRIPTION</span></span>
<span data-ttu-id="098ed-108">**AzCosmosDBTableThroughput** Cmdlet은 CosmosDB 테이블의 처리량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="098ed-108">The **Get-AzCosmosDBTableThroughput** cmdlet gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="098ed-109">예제의</span><span class="sxs-lookup"><span data-stu-id="098ed-109">EXAMPLES</span></span>

### <span data-ttu-id="098ed-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="098ed-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTableThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="098ed-111">변수</span><span class="sxs-lookup"><span data-stu-id="098ed-111">PARAMETERS</span></span>

### <span data-ttu-id="098ed-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="098ed-112">-AccountName</span></span>
<span data-ttu-id="098ed-113">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="098ed-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="098ed-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="098ed-114">-DefaultProfile</span></span>
<span data-ttu-id="098ed-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="098ed-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="098ed-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="098ed-116">-InputObject</span></span>
<span data-ttu-id="098ed-117">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="098ed-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="098ed-118">-이름</span><span class="sxs-lookup"><span data-stu-id="098ed-118">-Name</span></span>
<span data-ttu-id="098ed-119">테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="098ed-119">Name of the Table.</span></span>

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

### <span data-ttu-id="098ed-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="098ed-120">-ResourceGroupName</span></span>
<span data-ttu-id="098ed-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="098ed-121">Name of resource group.</span></span>

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

### <span data-ttu-id="098ed-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="098ed-122">CommonParameters</span></span>
<span data-ttu-id="098ed-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="098ed-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="098ed-124">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="098ed-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="098ed-125">입력</span><span class="sxs-lookup"><span data-stu-id="098ed-125">INPUTS</span></span>

### <span data-ttu-id="098ed-126">않아야</span><span class="sxs-lookup"><span data-stu-id="098ed-126">None</span></span>

## <span data-ttu-id="098ed-127">출력</span><span class="sxs-lookup"><span data-stu-id="098ed-127">OUTPUTS</span></span>

### <span data-ttu-id="098ed-128">CosmosDB. PSThroughputSettingsGetResults/.</span><span class="sxs-lookup"><span data-stu-id="098ed-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="098ed-129">상속자</span><span class="sxs-lookup"><span data-stu-id="098ed-129">NOTES</span></span>

## <span data-ttu-id="098ed-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="098ed-130">RELATED LINKS</span></span>
