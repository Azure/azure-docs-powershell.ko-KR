---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
ms.openlocfilehash: 4e31ae75f6fcea77c179757312988a0abbbb58f1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347157"
---
# <span data-ttu-id="29186-101">New-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="29186-101">New-AzCosmosDBAccount</span></span>

## <span data-ttu-id="29186-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29186-102">SYNOPSIS</span></span>
<span data-ttu-id="29186-103">새 CosmosDB 계정을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="29186-103">Create a new CosmosDB Account.</span></span>

## <span data-ttu-id="29186-104">구문</span><span class="sxs-lookup"><span data-stu-id="29186-104">SYNTAX</span></span>

```
New-AzCosmosDBAccount [-EnableAutomaticFailover] [-EnableMultipleWriteLocations] [-EnableVirtualNetwork]
 [-ApiKind <String>] [-DisableKeyBasedMetadataWriteAccess] [-EnableFreeTier <Boolean>]
 [-ServerVersion <String>] [-Location <String[]>] [-LocationObject <PSLocation[]>] -ResourceGroupName <String>
 -Name <String> [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29186-105">설명</span><span class="sxs-lookup"><span data-stu-id="29186-105">DESCRIPTION</span></span>
<span data-ttu-id="29186-106">주어진 ResourceGroup에서 새 CosmosDB 계정을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="29186-106">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="29186-107">예제</span><span class="sxs-lookup"><span data-stu-id="29186-107">EXAMPLES</span></span>

### <span data-ttu-id="29186-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="29186-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBAccount -ResourceGroupName resourceGroupName -Name databaseAccountName  -Location "East US"

Kind                          : GlobalDocumentDB
ProvisioningState             : Initializing
DocumentEndpoint              :
DatabaseAccountOfferType      : Standard
IpRangeFilter                 :
IsVirtualNetworkFilterEnabled : False
EnableAutomaticFailover       : False
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Models.ConsistencyPolicy
Capabilities                  : {}
WriteLocations                : {databaseAccountName-eastus}
ReadLocations                 : {databaseAccountName-eastus}
FailoverPolicies              : {databaseAccountName-eastus}
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : False
Location                      : East US
Tags                          : {}
Id                            : /subscriptions/{subscriptionid}/resourceGroups/resourceGroupName/providers/Microsoft.DocumentDB/databaseAccounts/databaseAccountName
Name                          : databaseAccountName
Type                          : Microsoft.DocumentDB/databaseAccounts
```

<span data-ttu-id="29186-109">ResourceGroup resourceGroupName에 이름이 databaseAccountName인 새 CosmosDB 계정이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="29186-109">A new CosmosDB Account with name databaseAccountName is created in the ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="29186-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29186-110">PARAMETERS</span></span>

### <span data-ttu-id="29186-111">-ApiKind</span><span class="sxs-lookup"><span data-stu-id="29186-111">-ApiKind</span></span>
<span data-ttu-id="29186-112">만들 Cosmos DB 데이터베이스 계정의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="29186-112">The type of Cosmos DB database account to create.</span></span>
<span data-ttu-id="29186-113">허용되는 값: Sql, MongoDB, Gremlin, Table, Cassandra.</span><span class="sxs-lookup"><span data-stu-id="29186-113">Accepted values: Sql, MongoDB, Gremlin, Table, Cassandra.</span></span>
<span data-ttu-id="29186-114">기본값: Sql</span><span class="sxs-lookup"><span data-stu-id="29186-114">Default value: Sql</span></span>

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

### <span data-ttu-id="29186-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29186-115">-AsJob</span></span>
<span data-ttu-id="29186-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="29186-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="29186-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="29186-117">-Confirm</span></span>
<span data-ttu-id="29186-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="29186-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29186-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="29186-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="29186-120">Cosmos DB 데이터베이스 계정의 기본 일관성 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="29186-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="29186-121">허용되는 값: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span><span class="sxs-lookup"><span data-stu-id="29186-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="29186-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29186-122">-DefaultProfile</span></span>
<span data-ttu-id="29186-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="29186-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29186-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="29186-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="29186-125">계정 키를 통해 메타데이터 리소스(데이터베이스, 컨테이너, 데이터)에 대한 쓰기 작업을 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="29186-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="29186-126">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="29186-126">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="29186-127">계정에서 AnalyticalStorage를 사용하도록 설정되어 있는 경우를 나타내는 Bool입니다.</span><span class="sxs-lookup"><span data-stu-id="29186-127">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="29186-128">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="29186-128">-EnableAutomaticFailover</span></span>
<span data-ttu-id="29186-129">중단으로 인해 지역을 사용할 수 없는 드문 경우 쓰기 지역의 자동 장애 조치(failover)를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="29186-129">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="29186-130">자동 장애 조치(failover)를 수행하면 계정에 대한 새 쓰기 지역이 발생하고 계정에 대해 구성된 장애 조치 우선 순위에 따라 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="29186-130">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="29186-131">허용되는 값: false, true</span><span class="sxs-lookup"><span data-stu-id="29186-131">Accepted values: false, true</span></span>

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

### <span data-ttu-id="29186-132">-EnableFreeTier</span><span class="sxs-lookup"><span data-stu-id="29186-132">-EnableFreeTier</span></span>
<span data-ttu-id="29186-133">계정에서 FreeTier를 사용하도록 설정되어 있는 경우를 나타내는 Bool입니다.</span><span class="sxs-lookup"><span data-stu-id="29186-133">Bool to indicate if FreeTier is enabled on the account.</span></span>

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

### <span data-ttu-id="29186-134">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="29186-134">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="29186-135">여러 쓰기 위치를 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="29186-135">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="29186-136">허용되는 값: false, true</span><span class="sxs-lookup"><span data-stu-id="29186-136">Accepted values: false, true</span></span>

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

### <span data-ttu-id="29186-137">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="29186-137">-EnableVirtualNetwork</span></span>
<span data-ttu-id="29186-138">Cosmos DB 데이터베이스 계정에서 가상 네트워크를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="29186-138">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="29186-139">허용되는 값: false, true</span><span class="sxs-lookup"><span data-stu-id="29186-139">Accepted values: false, true</span></span>

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

### <span data-ttu-id="29186-140">-IpRule</span><span class="sxs-lookup"><span data-stu-id="29186-140">-IpRule</span></span>
<span data-ttu-id="29186-141">방화벽 지원.</span><span class="sxs-lookup"><span data-stu-id="29186-141">Firewall support.</span></span> <span data-ttu-id="29186-142">특정 데이터베이스 계정에 대해 허용되는 클라이언트 IP 목록으로 포함될 CIDR 양식의 IP 주소 또는 IP 주소 범위 집합을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="29186-142">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="29186-143">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="29186-143">-KeyVaultKeyUri</span></span>
<span data-ttu-id="29186-144">KeyVault의 URI</span><span class="sxs-lookup"><span data-stu-id="29186-144">URI of the KeyVault</span></span>

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

### <span data-ttu-id="29186-145">-Location</span><span class="sxs-lookup"><span data-stu-id="29186-145">-Location</span></span>
<span data-ttu-id="29186-146">Cosmos DB 데이터베이스 계정에 위치를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="29186-146">Add a location to the Cosmos DB database account.</span></span>
<span data-ttu-id="29186-147">장애 조치 우선 순위에 따라 순서가 지정되는 문자열 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="29186-147">Array of strings, ordered by failover priority.</span></span>

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

### <span data-ttu-id="29186-148">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="29186-148">-LocationObject</span></span>
<span data-ttu-id="29186-149">Cosmos DB 데이터베이스 계정에 위치를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="29186-149">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="29186-150">PSLocation 개체의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="29186-150">Array of PSLocation objects.</span></span>

```yaml
Type: PSLocation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29186-151">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="29186-151">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="29186-152">경계가 있는 부실 일관성과 함께 사용하는 경우 이 값은 용인되는 부실의 시간 양(시간pan)을 나타냈습니다.</span><span class="sxs-lookup"><span data-stu-id="29186-152">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="29186-153">이 값에 허용되는 범위는 5-86400입니다.</span><span class="sxs-lookup"><span data-stu-id="29186-153">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="29186-154">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="29186-154">-MaxStalenessPrefix</span></span>
<span data-ttu-id="29186-155">경계가 있는 부실 일관성과 함께 사용하는 경우 이 값은 용인되는 부실 요청 수를 나타냈습니다.</span><span class="sxs-lookup"><span data-stu-id="29186-155">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="29186-156">이 값에 허용되는 범위는 1 - 2,147,483,647입니다.</span><span class="sxs-lookup"><span data-stu-id="29186-156">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="29186-157">-Name</span><span class="sxs-lookup"><span data-stu-id="29186-157">-Name</span></span>
<span data-ttu-id="29186-158">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29186-158">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="29186-159">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="29186-159">-PublicNetworkAccess</span></span>
<span data-ttu-id="29186-160">이 서버에 대해 공용 엔드포인트 액세스가 허용되는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="29186-160">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="29186-161">가능한 값은 'Enabled', 'Disabled'입니다.</span><span class="sxs-lookup"><span data-stu-id="29186-161">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="29186-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29186-162">-ResourceGroupName</span></span>
<span data-ttu-id="29186-163">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29186-163">Name of resource group.</span></span>

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

### <span data-ttu-id="29186-164">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="29186-164">-ServerVersion</span></span>
<span data-ttu-id="29186-165">ServerVersion( MongoDB 계정의 경우만 유효)</span><span class="sxs-lookup"><span data-stu-id="29186-165">ServerVersion, valid only in case of MongoDB Accounts.</span></span>

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

### <span data-ttu-id="29186-166">-Tag</span><span class="sxs-lookup"><span data-stu-id="29186-166">-Tag</span></span>
<span data-ttu-id="29186-167">태그를 키-값 쌍으로 해시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="29186-167">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="29186-168">빈 문자열을 사용하여 기존 태그를 지우면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="29186-168">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="29186-169">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="29186-169">-VirtualNetworkRule</span></span>
<span data-ttu-id="29186-170">가상 네트워크에 대한 ACL의 문자열 값 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="29186-170">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="29186-171">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="29186-171">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="29186-172">가상 네트워크에 대한 PSVirtualNetworkRuleObjects의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="29186-172">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="29186-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29186-173">-WhatIf</span></span>
<span data-ttu-id="29186-174">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="29186-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29186-175">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="29186-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29186-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29186-176">CommonParameters</span></span>
<span data-ttu-id="29186-177">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="29186-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29186-178">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="29186-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29186-179">입력</span><span class="sxs-lookup"><span data-stu-id="29186-179">INPUTS</span></span>

### <span data-ttu-id="29186-180">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span><span class="sxs-lookup"><span data-stu-id="29186-180">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="29186-181">출력</span><span class="sxs-lookup"><span data-stu-id="29186-181">OUTPUTS</span></span>

### <span data-ttu-id="29186-182">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="29186-182">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="29186-183">참고 사항</span><span class="sxs-lookup"><span data-stu-id="29186-183">NOTES</span></span>

## <span data-ttu-id="29186-184">관련 링크</span><span class="sxs-lookup"><span data-stu-id="29186-184">RELATED LINKS</span></span>
 
