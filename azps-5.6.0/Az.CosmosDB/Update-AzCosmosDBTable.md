---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
ms.openlocfilehash: 3463a07219375db06495bd5d50a2fe3b5916e173
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009680"
---
# <span data-ttu-id="66e93-101">Update-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="66e93-101">Update-AzCosmosDBTable</span></span>

## <span data-ttu-id="66e93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66e93-102">SYNOPSIS</span></span>
<span data-ttu-id="66e93-103">CosmosDB 테이블을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="66e93-103">Updates the CosmosDB Table.</span></span> <span data-ttu-id="66e93-104">기존 테이블을 읽어 클라이언트 쪽 패치 작업을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="66e93-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="66e93-105">구문</span><span class="sxs-lookup"><span data-stu-id="66e93-105">SYNTAX</span></span>

### <span data-ttu-id="66e93-106">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="66e93-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66e93-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66e93-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66e93-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66e93-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="66e93-109">설명</span><span class="sxs-lookup"><span data-stu-id="66e93-109">DESCRIPTION</span></span>
<span data-ttu-id="66e93-110">CosmosDB 테이블을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="66e93-110">Updates the CosmosDB Table.</span></span> <span data-ttu-id="66e93-111">기존 테이블을 읽어 클라이언트 쪽 패치 작업을 수행합니다.</span><span class="sxs-lookup"><span data-stu-id="66e93-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="66e93-112">예제</span><span class="sxs-lookup"><span data-stu-id="66e93-112">EXAMPLES</span></span>

### <span data-ttu-id="66e93-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="66e93-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName Throughput 800

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="66e93-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="66e93-114">PARAMETERS</span></span>

### <span data-ttu-id="66e93-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="66e93-115">-AccountName</span></span>
<span data-ttu-id="66e93-116">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="66e93-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="66e93-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="66e93-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="66e93-118">자동 조정을 사용하도록 설정한 경우 최대 진행량 값입니다.</span><span class="sxs-lookup"><span data-stu-id="66e93-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="66e93-119">-확인</span><span class="sxs-lookup"><span data-stu-id="66e93-119">-Confirm</span></span>
<span data-ttu-id="66e93-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="66e93-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66e93-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66e93-121">-DefaultProfile</span></span>
<span data-ttu-id="66e93-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="66e93-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66e93-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66e93-123">-InputObject</span></span>
<span data-ttu-id="66e93-124">테이블 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="66e93-124">Table Object.</span></span>

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

### <span data-ttu-id="66e93-125">-Name</span><span class="sxs-lookup"><span data-stu-id="66e93-125">-Name</span></span>
<span data-ttu-id="66e93-126">표의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="66e93-126">Name of the Table.</span></span>

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

### <span data-ttu-id="66e93-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="66e93-127">-ParentObject</span></span>
<span data-ttu-id="66e93-128">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="66e93-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="66e93-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66e93-129">-ResourceGroupName</span></span>
<span data-ttu-id="66e93-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="66e93-130">Name of resource group.</span></span>

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

### <span data-ttu-id="66e93-131">-Throughput</span><span class="sxs-lookup"><span data-stu-id="66e93-131">-Throughput</span></span>
<span data-ttu-id="66e93-132">테이블(RU/s)의 스루미트입니다.</span><span class="sxs-lookup"><span data-stu-id="66e93-132">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="66e93-133">기본값은 400입니다.</span><span class="sxs-lookup"><span data-stu-id="66e93-133">Default value is 400.</span></span>

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

### <span data-ttu-id="66e93-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66e93-134">-WhatIf</span></span>
<span data-ttu-id="66e93-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="66e93-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66e93-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="66e93-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66e93-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66e93-137">CommonParameters</span></span>
<span data-ttu-id="66e93-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="66e93-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66e93-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66e93-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66e93-140">입력</span><span class="sxs-lookup"><span data-stu-id="66e93-140">INPUTS</span></span>

### <span data-ttu-id="66e93-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="66e93-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="66e93-142">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="66e93-142">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="66e93-143">출력</span><span class="sxs-lookup"><span data-stu-id="66e93-143">OUTPUTS</span></span>

### <span data-ttu-id="66e93-144">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="66e93-144">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="66e93-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="66e93-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="66e93-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="66e93-146">NOTES</span></span>

## <span data-ttu-id="66e93-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="66e93-147">RELATED LINKS</span></span>
