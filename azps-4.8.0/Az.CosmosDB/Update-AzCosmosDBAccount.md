---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
ms.openlocfilehash: e88deadc0a46aa5d89bd513a4aba1b93e22fbb5a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212375"
---
# <span data-ttu-id="97fd1-101">Update-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="97fd1-101">Update-AzCosmosDBAccount</span></span>

## <span data-ttu-id="97fd1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97fd1-102">SYNOPSIS</span></span>
<span data-ttu-id="97fd1-103">CosmosDB account 특성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="97fd1-103">Update a CosmosDB account attributes.</span></span>

## <span data-ttu-id="97fd1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="97fd1-104">SYNTAX</span></span>

### <span data-ttu-id="97fd1-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="97fd1-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccount [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-DisableKeyBasedMetadataWriteAccess <Boolean>] -ResourceGroupName <String>
 -Name <String> [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97fd1-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="97fd1-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccount -ResourceId <String> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97fd1-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="97fd1-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97fd1-108">설명은</span><span class="sxs-lookup"><span data-stu-id="97fd1-108">DESCRIPTION</span></span>
<span data-ttu-id="97fd1-109">CosmosDB 계정의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="97fd1-109">Update the properties of a CosmosDB account.</span></span> <span data-ttu-id="97fd1-110">다른 속성과 함께 simulataneously 계정 지역을 업데이트할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="97fd1-110">Cannot update Account Regions simulataneously with other properties.</span></span>

## <span data-ttu-id="97fd1-111">예제의</span><span class="sxs-lookup"><span data-stu-id="97fd1-111">EXAMPLES</span></span>

### <span data-ttu-id="97fd1-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="97fd1-112">Example 1</span></span>
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

<span data-ttu-id="97fd1-113">이름이 accountName 인 CosmosDB 계정에 대해 DefaultConsistencyLevel를 "강력한", 사용 하도록 설정 된 자동 장애 조치, 사용 MultipleWriteLocations 및 사용 VirtualNetwork이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="97fd1-113">Updated DefaultConsistencyLevel to "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations and Enabled VirtualNetwork for CosmosDB Account with name accountName.</span></span> 

## <span data-ttu-id="97fd1-114">변수</span><span class="sxs-lookup"><span data-stu-id="97fd1-114">PARAMETERS</span></span>

### <span data-ttu-id="97fd1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97fd1-115">-AsJob</span></span>
<span data-ttu-id="97fd1-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="97fd1-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="97fd1-117">-확인</span><span class="sxs-lookup"><span data-stu-id="97fd1-117">-Confirm</span></span>
<span data-ttu-id="97fd1-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="97fd1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97fd1-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="97fd1-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="97fd1-120">Cosmos DB 데이터베이스 계정의 기본 일관성 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="97fd1-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="97fd1-121">허용 되는 값: BoundedStaleness, ConsistentPrefix, 궁극적인, Session, Strong</span><span class="sxs-lookup"><span data-stu-id="97fd1-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="97fd1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97fd1-122">-DefaultProfile</span></span>
<span data-ttu-id="97fd1-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="97fd1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97fd1-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="97fd1-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="97fd1-125">계정 키를 통해 메타 데이터 리소스 (데이터베이스, 컨테이너, 처리량)에 대 한 쓰기 작업을 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="97fd1-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="97fd1-126">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="97fd1-126">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="97fd1-127">계정에서 AnalyticalStorage을 사용할 수 있는지 여부를 나타내는 부울입니다.</span><span class="sxs-lookup"><span data-stu-id="97fd1-127">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="97fd1-128">-Enable자동 장애 조치</span><span class="sxs-lookup"><span data-stu-id="97fd1-128">-EnableAutomaticFailover</span></span>
<span data-ttu-id="97fd1-129">비활성으로 인해 지역을 사용할 수 없는 드문 이벤트에서 쓰기 영역의 자동 장애 조치를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97fd1-129">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="97fd1-130">자동 장애 조치 (failover)로 인해 계정에 대 한 새 쓰기 영역이 만들어지고 계정에 대해 구성 된 장애 조치 (failover) 우선 순위에 따라 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="97fd1-130">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="97fd1-131">허용 된 값: false, true</span><span class="sxs-lookup"><span data-stu-id="97fd1-131">Accepted values: false, true</span></span>

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

### <span data-ttu-id="97fd1-132">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="97fd1-132">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="97fd1-133">여러 쓰기 위치를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97fd1-133">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="97fd1-134">허용 된 값: false, true</span><span class="sxs-lookup"><span data-stu-id="97fd1-134">Accepted values: false, true</span></span>

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

### <span data-ttu-id="97fd1-135">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="97fd1-135">-EnableVirtualNetwork</span></span>
<span data-ttu-id="97fd1-136">Cosmos DB 데이터베이스 계정에서 가상 네트워크를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97fd1-136">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="97fd1-137">허용 된 값: false, true</span><span class="sxs-lookup"><span data-stu-id="97fd1-137">Accepted values: false, true</span></span>

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

### <span data-ttu-id="97fd1-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97fd1-138">-InputObject</span></span>
<span data-ttu-id="97fd1-139">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="97fd1-139">CosmosDB Account object</span></span>

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

### <span data-ttu-id="97fd1-140">-IpRule</span><span class="sxs-lookup"><span data-stu-id="97fd1-140">-IpRule</span></span>
<span data-ttu-id="97fd1-141">방화벽 지원.</span><span class="sxs-lookup"><span data-stu-id="97fd1-141">Firewall support.</span></span> <span data-ttu-id="97fd1-142">지정 된 데이터베이스 계정에 대 한 클라이언트 Ip의 허용 목록으로 포함할 IP 주소 또는 IP 주소 범위 집합을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="97fd1-142">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="97fd1-143">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="97fd1-143">-KeyVaultKeyUri</span></span>
<span data-ttu-id="97fd1-144">KeyVault의 URI</span><span class="sxs-lookup"><span data-stu-id="97fd1-144">URI of the KeyVault</span></span>

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

### <span data-ttu-id="97fd1-145">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="97fd1-145">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="97fd1-146">제한 된 부실 일관성에 사용 하는 경우이 값은 부실 (timespan) 허용의 시간을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="97fd1-146">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="97fd1-147">이 값에 허용 된 범위는 5-86400입니다.</span><span class="sxs-lookup"><span data-stu-id="97fd1-147">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="97fd1-148">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="97fd1-148">-MaxStalenessPrefix</span></span>
<span data-ttu-id="97fd1-149">제한 된 만료 일관성에 사용 하는 경우이 값은 허용 되는 부실 요청 수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="97fd1-149">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="97fd1-150">이 값에 허용 되는 범위는 1-2147483647입니다.</span><span class="sxs-lookup"><span data-stu-id="97fd1-150">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="97fd1-151">-이름</span><span class="sxs-lookup"><span data-stu-id="97fd1-151">-Name</span></span>
<span data-ttu-id="97fd1-152">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="97fd1-152">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="97fd1-153">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="97fd1-153">-PublicNetworkAccess</span></span>
<span data-ttu-id="97fd1-154">이 서버에 대 한 공개 끝점 액세스가 허용 되는지 여부</span><span class="sxs-lookup"><span data-stu-id="97fd1-154">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="97fd1-155">사용할 수 있는 값은 다음과 같습니다. ' Enabled ', ' Disabled '</span><span class="sxs-lookup"><span data-stu-id="97fd1-155">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="97fd1-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97fd1-156">-ResourceGroupName</span></span>
<span data-ttu-id="97fd1-157">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="97fd1-157">Name of resource group.</span></span>

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

### <span data-ttu-id="97fd1-158">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97fd1-158">-ResourceId</span></span>
<span data-ttu-id="97fd1-159">리소스의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="97fd1-159">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="97fd1-160">태그</span><span class="sxs-lookup"><span data-stu-id="97fd1-160">-Tag</span></span>
<span data-ttu-id="97fd1-161">태그의 해시 테이블 (키-값 쌍)</span><span class="sxs-lookup"><span data-stu-id="97fd1-161">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="97fd1-162">빈 문자열을 사용 하 여 기존 태그 지우기</span><span class="sxs-lookup"><span data-stu-id="97fd1-162">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="97fd1-163">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="97fd1-163">-VirtualNetworkRule</span></span>
<span data-ttu-id="97fd1-164">가상 네트워크에 대 한 ACL의 문자열 값 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="97fd1-164">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="97fd1-165">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="97fd1-165">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="97fd1-166">가상 네트워크에 대 한 PSVirtualNetworkRuleObjects의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="97fd1-166">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="97fd1-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97fd1-167">-WhatIf</span></span>
<span data-ttu-id="97fd1-168">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="97fd1-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97fd1-169">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="97fd1-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97fd1-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97fd1-170">CommonParameters</span></span>
<span data-ttu-id="97fd1-171">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="97fd1-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97fd1-172">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="97fd1-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97fd1-173">입력</span><span class="sxs-lookup"><span data-stu-id="97fd1-173">INPUTS</span></span>

### <span data-ttu-id="97fd1-174">CosmosDB [] PSCorsRule []</span><span class="sxs-lookup"><span data-stu-id="97fd1-174">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="97fd1-175">출력</span><span class="sxs-lookup"><span data-stu-id="97fd1-175">OUTPUTS</span></span>

### <span data-ttu-id="97fd1-176">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="97fd1-176">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="97fd1-177">상속자</span><span class="sxs-lookup"><span data-stu-id="97fd1-177">NOTES</span></span>

## <span data-ttu-id="97fd1-178">관련 링크</span><span class="sxs-lookup"><span data-stu-id="97fd1-178">RELATED LINKS</span></span>
