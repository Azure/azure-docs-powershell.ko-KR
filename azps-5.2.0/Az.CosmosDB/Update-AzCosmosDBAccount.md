---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
ms.openlocfilehash: e88deadc0a46aa5d89bd513a4aba1b93e22fbb5a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356952"
---
# <span data-ttu-id="0c76c-101">Update-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="0c76c-101">Update-AzCosmosDBAccount</span></span>

## <span data-ttu-id="0c76c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c76c-102">SYNOPSIS</span></span>
<span data-ttu-id="0c76c-103">CosmosDB 계정 특성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0c76c-103">Update a CosmosDB account attributes.</span></span>

## <span data-ttu-id="0c76c-104">구문</span><span class="sxs-lookup"><span data-stu-id="0c76c-104">SYNTAX</span></span>

### <span data-ttu-id="0c76c-105">ByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="0c76c-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccount [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-DisableKeyBasedMetadataWriteAccess <Boolean>] -ResourceGroupName <String>
 -Name <String> [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c76c-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c76c-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccount -ResourceId <String> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c76c-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c76c-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c76c-108">설명</span><span class="sxs-lookup"><span data-stu-id="0c76c-108">DESCRIPTION</span></span>
<span data-ttu-id="0c76c-109">CosmosDB 계정의 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0c76c-109">Update the properties of a CosmosDB account.</span></span> <span data-ttu-id="0c76c-110">다른 속성으로 계정 지역을 시뮬레이션하여 업데이트할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0c76c-110">Cannot update Account Regions simulataneously with other properties.</span></span>

## <span data-ttu-id="0c76c-111">예제</span><span class="sxs-lookup"><span data-stu-id="0c76c-111">EXAMPLES</span></span>

### <span data-ttu-id="0c76c-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="0c76c-112">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccount -ResourceGroupName resourceGroupName -Name accountName -DefaultConsistencyLevel "Strong" -EnableAutomaticFailover 1 -EnableMultipleWriteLocations 1 -EnableVirtualNetwork 1

Kind                          : GlobalDocumentDB
ProvisioningState             : Initializing
DocumentEndpoint              :
DatabaseAccountOfferType      : Standard
IpRangeFilter                 :
IsVirtualNetworkFilterEnabled : True
EnableAutomaticFailover       : True
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Fluent.Models.ConsistencyPolicy
Capabilities                  : {}
WriteLocations                : {accountName-eastus}
ReadLocations                 : {accountName-eastus}
FailoverPolicies              : {accountName-eastus}
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : True
Location                      : East US
Tags                          : {}
Id                            : /subscriptions/{subscriptionid}/resourceGroups/resourceGroupName/providers/Microsoft.DocumentDB/databaseAccounts/accountName
Name                          : accountName
Type                          : Microsoft.DocumentDB/databaseAccounts
```

<span data-ttu-id="0c76c-113">DefaultConsistencyLevel을 "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations 및 Enabled VirtualNetwork for CosmosDB Account with name accountName으로 업데이트했습니다.</span><span class="sxs-lookup"><span data-stu-id="0c76c-113">Updated DefaultConsistencyLevel to "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations and Enabled VirtualNetwork for CosmosDB Account with name accountName.</span></span> 

## <span data-ttu-id="0c76c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c76c-114">PARAMETERS</span></span>

### <span data-ttu-id="0c76c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c76c-115">-AsJob</span></span>
<span data-ttu-id="0c76c-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0c76c-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c76c-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c76c-117">-Confirm</span></span>
<span data-ttu-id="0c76c-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0c76c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c76c-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="0c76c-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="0c76c-120">Cosmos DB 데이터베이스 계정의 기본 일관성 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="0c76c-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="0c76c-121">허용되는 값: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span><span class="sxs-lookup"><span data-stu-id="0c76c-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="0c76c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c76c-122">-DefaultProfile</span></span>
<span data-ttu-id="0c76c-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0c76c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c76c-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="0c76c-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="0c76c-125">계정 키를 통해 메타데이터 리소스(데이터베이스, 컨테이너, 데이터)에 대한 쓰기 작업을 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="0c76c-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c76c-126">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="0c76c-126">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="0c76c-127">계정에서 AnalyticalStorage를 사용하도록 설정되어 있는 경우를 나타내는 Bool입니다.</span><span class="sxs-lookup"><span data-stu-id="0c76c-127">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c76c-128">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="0c76c-128">-EnableAutomaticFailover</span></span>
<span data-ttu-id="0c76c-129">중단으로 인해 지역을 사용할 수 없는 드문 경우 쓰기 지역의 자동 장애 조치(failover)를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0c76c-129">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="0c76c-130">자동 장애 조치(failover)를 수행하면 계정에 대한 새 쓰기 지역이 발생하고 계정에 대해 구성된 장애 조치 우선 순위에 따라 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="0c76c-130">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="0c76c-131">허용되는 값: false, true</span><span class="sxs-lookup"><span data-stu-id="0c76c-131">Accepted values: false, true</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c76c-132">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="0c76c-132">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="0c76c-133">여러 쓰기 위치를 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="0c76c-133">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="0c76c-134">허용되는 값: false, true</span><span class="sxs-lookup"><span data-stu-id="0c76c-134">Accepted values: false, true</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c76c-135">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0c76c-135">-EnableVirtualNetwork</span></span>
<span data-ttu-id="0c76c-136">Cosmos DB 데이터베이스 계정에서 가상 네트워크를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="0c76c-136">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="0c76c-137">허용되는 값: false, true</span><span class="sxs-lookup"><span data-stu-id="0c76c-137">Accepted values: false, true</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c76c-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c76c-138">-InputObject</span></span>
<span data-ttu-id="0c76c-139">CosmosDB 계정 개체</span><span class="sxs-lookup"><span data-stu-id="0c76c-139">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c76c-140">-IpRule</span><span class="sxs-lookup"><span data-stu-id="0c76c-140">-IpRule</span></span>
<span data-ttu-id="0c76c-141">방화벽 지원.</span><span class="sxs-lookup"><span data-stu-id="0c76c-141">Firewall support.</span></span> <span data-ttu-id="0c76c-142">특정 데이터베이스 계정에 대해 허용되는 클라이언트 IP 목록으로 포함될 CIDR 양식의 IP 주소 또는 IP 주소 범위 집합을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0c76c-142">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c76c-143">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="0c76c-143">-KeyVaultKeyUri</span></span>
<span data-ttu-id="0c76c-144">KeyVault의 URI</span><span class="sxs-lookup"><span data-stu-id="0c76c-144">URI of the KeyVault</span></span>

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

### <span data-ttu-id="0c76c-145">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="0c76c-145">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="0c76c-146">경계가 있는 부실 일관성과 함께 사용하는 경우 이 값은 용인되는 부실의 시간 양(시간pan)을 나타냈습니다.</span><span class="sxs-lookup"><span data-stu-id="0c76c-146">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="0c76c-147">이 값에 허용되는 범위는 5-86400입니다.</span><span class="sxs-lookup"><span data-stu-id="0c76c-147">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="0c76c-148">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="0c76c-148">-MaxStalenessPrefix</span></span>
<span data-ttu-id="0c76c-149">경계가 있는 부실 일관성과 함께 사용하는 경우 이 값은 용인되는 부실 요청 수를 나타냈습니다.</span><span class="sxs-lookup"><span data-stu-id="0c76c-149">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="0c76c-150">이 값에 허용되는 범위는 1 - 2,147,483,647입니다.</span><span class="sxs-lookup"><span data-stu-id="0c76c-150">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="0c76c-151">-Name</span><span class="sxs-lookup"><span data-stu-id="0c76c-151">-Name</span></span>
<span data-ttu-id="0c76c-152">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0c76c-152">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0c76c-153">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="0c76c-153">-PublicNetworkAccess</span></span>
<span data-ttu-id="0c76c-154">이 서버에 대해 공용 엔드포인트 액세스가 허용되는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="0c76c-154">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="0c76c-155">가능한 값은 'Enabled', 'Disabled'입니다.</span><span class="sxs-lookup"><span data-stu-id="0c76c-155">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="0c76c-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c76c-156">-ResourceGroupName</span></span>
<span data-ttu-id="0c76c-157">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0c76c-157">Name of resource group.</span></span>

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

### <span data-ttu-id="0c76c-158">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c76c-158">-ResourceId</span></span>
<span data-ttu-id="0c76c-159">리소스의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="0c76c-159">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="0c76c-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="0c76c-160">-Tag</span></span>
<span data-ttu-id="0c76c-161">태그를 키-값 쌍으로 해시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0c76c-161">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="0c76c-162">빈 문자열을 사용하여 기존 태그를 지우면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0c76c-162">Use empty string to clear existing tag.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c76c-163">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0c76c-163">-VirtualNetworkRule</span></span>
<span data-ttu-id="0c76c-164">가상 네트워크에 대한 ACL의 문자열 값 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="0c76c-164">Array of string values of ACL's for virtual network.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c76c-165">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="0c76c-165">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="0c76c-166">가상 네트워크에 대한 PSVirtualNetworkRuleObjects의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="0c76c-166">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

```yaml
Type: PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c76c-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c76c-167">-WhatIf</span></span>
<span data-ttu-id="0c76c-168">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0c76c-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c76c-169">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0c76c-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c76c-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c76c-170">CommonParameters</span></span>
<span data-ttu-id="0c76c-171">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0c76c-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c76c-172">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0c76c-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c76c-173">입력</span><span class="sxs-lookup"><span data-stu-id="0c76c-173">INPUTS</span></span>

### <span data-ttu-id="0c76c-174">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span><span class="sxs-lookup"><span data-stu-id="0c76c-174">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="0c76c-175">출력</span><span class="sxs-lookup"><span data-stu-id="0c76c-175">OUTPUTS</span></span>

### <span data-ttu-id="0c76c-176">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="0c76c-176">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="0c76c-177">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0c76c-177">NOTES</span></span>

## <span data-ttu-id="0c76c-178">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0c76c-178">RELATED LINKS</span></span>
