---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
ms.openlocfilehash: efc177e5255f4325fc2ecbfe88e94bb32708c45a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372884"
---
# <span data-ttu-id="1b06f-101">Update-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="1b06f-101">Update-AzCosmosDBTable</span></span>

## <span data-ttu-id="1b06f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b06f-102">SYNOPSIS</span></span>
<span data-ttu-id="1b06f-103">CosmosDB 테이블을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1b06f-103">Updates the CosmosDB Table.</span></span> <span data-ttu-id="1b06f-104">기존 테이블을 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b06f-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="1b06f-105">구문</span><span class="sxs-lookup"><span data-stu-id="1b06f-105">SYNTAX</span></span>

### <span data-ttu-id="1b06f-106">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="1b06f-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1b06f-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b06f-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1b06f-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b06f-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1b06f-109">설명</span><span class="sxs-lookup"><span data-stu-id="1b06f-109">DESCRIPTION</span></span>
<span data-ttu-id="1b06f-110">CosmosDB 테이블을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1b06f-110">Updates the CosmosDB Table.</span></span> <span data-ttu-id="1b06f-111">기존 테이블을 읽어 클라이언트 쪽 패치 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b06f-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="1b06f-112">예제</span><span class="sxs-lookup"><span data-stu-id="1b06f-112">EXAMPLES</span></span>

### <span data-ttu-id="1b06f-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="1b06f-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName Throughput 800

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="1b06f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b06f-114">PARAMETERS</span></span>

### <span data-ttu-id="1b06f-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1b06f-115">-AccountName</span></span>
<span data-ttu-id="1b06f-116">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1b06f-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1b06f-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="1b06f-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="1b06f-118">자동 조정을 사용하도록 설정한 경우 최대 사용량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="1b06f-118">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b06f-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b06f-119">-Confirm</span></span>
<span data-ttu-id="1b06f-120">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b06f-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b06f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b06f-121">-DefaultProfile</span></span>
<span data-ttu-id="1b06f-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1b06f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b06f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b06f-123">-InputObject</span></span>
<span data-ttu-id="1b06f-124">테이블 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="1b06f-124">Table Object.</span></span>

```yaml
Type: PSTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b06f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="1b06f-125">-Name</span></span>
<span data-ttu-id="1b06f-126">테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1b06f-126">Name of the Table.</span></span>

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

### <span data-ttu-id="1b06f-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1b06f-127">-ParentObject</span></span>
<span data-ttu-id="1b06f-128">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="1b06f-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="1b06f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b06f-129">-ResourceGroupName</span></span>
<span data-ttu-id="1b06f-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1b06f-130">Name of resource group.</span></span>

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

### <span data-ttu-id="1b06f-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="1b06f-131">-Throughput</span></span>
<span data-ttu-id="1b06f-132">테이블의 경우(RU/s)</span><span class="sxs-lookup"><span data-stu-id="1b06f-132">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="1b06f-133">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="1b06f-133">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b06f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b06f-134">-WhatIf</span></span>
<span data-ttu-id="1b06f-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1b06f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b06f-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1b06f-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b06f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b06f-137">CommonParameters</span></span>
<span data-ttu-id="1b06f-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1b06f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b06f-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1b06f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b06f-140">입력</span><span class="sxs-lookup"><span data-stu-id="1b06f-140">INPUTS</span></span>

### <span data-ttu-id="1b06f-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="1b06f-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="1b06f-142">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="1b06f-142">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="1b06f-143">출력</span><span class="sxs-lookup"><span data-stu-id="1b06f-143">OUTPUTS</span></span>

### <span data-ttu-id="1b06f-144">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="1b06f-144">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="1b06f-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="1b06f-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="1b06f-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1b06f-146">NOTES</span></span>

## <span data-ttu-id="1b06f-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1b06f-147">RELATED LINKS</span></span>
