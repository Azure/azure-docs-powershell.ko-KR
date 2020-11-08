---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
ms.openlocfilehash: a31df71a1242f4f4e9eb01a37d31eb54ec874a99
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034014"
---
# <span data-ttu-id="302c4-101">Update-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="302c4-101">Update-AzCosmosDBAccount</span></span>

## <span data-ttu-id="302c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="302c4-102">SYNOPSIS</span></span>
<span data-ttu-id="302c4-103">CosmosDB account 특성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="302c4-103">Update a CosmosDB account attributes.</span></span>

## <span data-ttu-id="302c4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="302c4-104">SYNTAX</span></span>

### <span data-ttu-id="302c4-105">ByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="302c4-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-IpRangeFilter <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-DisableKeyBasedMetadataWriteAccess <Boolean>]
 [-PublicNetworkAccess <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="302c4-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="302c4-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccount -ResourceId <String> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-IpRangeFilter <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-DisableKeyBasedMetadataWriteAccess <Boolean>]
 [-PublicNetworkAccess <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="302c4-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="302c4-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccount -InputObject <PSDatabaseAccount> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-IpRangeFilter <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-DisableKeyBasedMetadataWriteAccess <Boolean>]
 [-PublicNetworkAccess <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="302c4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="302c4-108">DESCRIPTION</span></span>
<span data-ttu-id="302c4-109">CosmosDB 계정의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="302c4-109">Update the properties of a CosmosDB account.</span></span> <span data-ttu-id="302c4-110">다른 속성과 함께 simulataneously 계정 지역을 업데이트할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="302c4-110">Cannot update Account Regions simulataneously with other properties.</span></span>

## <span data-ttu-id="302c4-111">예제의</span><span class="sxs-lookup"><span data-stu-id="302c4-111">EXAMPLES</span></span>

### <span data-ttu-id="302c4-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="302c4-112">Example 1</span></span>
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

<span data-ttu-id="302c4-113">이름이 accountName 인 CosmosDB 계정에 대해 DefaultConsistencyLevel를 "강력한", 사용 하도록 설정 된 자동 장애 조치, 사용 MultipleWriteLocations 및 사용 VirtualNetwork이 업데이트 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="302c4-113">Updated DefaultConsistencyLevel to "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations and Enabled VirtualNetwork for CosmosDB Account with name accountName.</span></span> 

## <span data-ttu-id="302c4-114">변수</span><span class="sxs-lookup"><span data-stu-id="302c4-114">PARAMETERS</span></span>

### <span data-ttu-id="302c4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="302c4-115">-AsJob</span></span>
<span data-ttu-id="302c4-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="302c4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="302c4-117">-확인</span><span class="sxs-lookup"><span data-stu-id="302c4-117">-Confirm</span></span>
<span data-ttu-id="302c4-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="302c4-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="302c4-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="302c4-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="302c4-120">Cosmos DB 데이터베이스 계정의 기본 일관성 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="302c4-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="302c4-121">허용 되는 값: BoundedStaleness, ConsistentPrefix, 궁극적인, Session, Strong</span><span class="sxs-lookup"><span data-stu-id="302c4-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="302c4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="302c4-122">-DefaultProfile</span></span>
<span data-ttu-id="302c4-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="302c4-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="302c4-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="302c4-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="302c4-125">계정 키를 통해 메타 데이터 리소스 (데이터베이스, 컨테이너, 처리량)에 대 한 쓰기 작업을 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="302c4-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="302c4-126">-Enable자동 장애 조치</span><span class="sxs-lookup"><span data-stu-id="302c4-126">-EnableAutomaticFailover</span></span>
<span data-ttu-id="302c4-127">비활성으로 인해 지역을 사용할 수 없는 드문 이벤트에서 쓰기 영역의 자동 장애 조치를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="302c4-127">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="302c4-128">자동 장애 조치 (failover)로 인해 계정에 대 한 새 쓰기 영역이 만들어지고 계정에 대해 구성 된 장애 조치 (failover) 우선 순위에 따라 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="302c4-128">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="302c4-129">허용 된 값: false, true</span><span class="sxs-lookup"><span data-stu-id="302c4-129">Accepted values: false, true</span></span>

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

### <span data-ttu-id="302c4-130">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="302c4-130">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="302c4-131">여러 쓰기 위치를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="302c4-131">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="302c4-132">허용 된 값: false, true</span><span class="sxs-lookup"><span data-stu-id="302c4-132">Accepted values: false, true</span></span>

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

### <span data-ttu-id="302c4-133">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="302c4-133">-EnableVirtualNetwork</span></span>
<span data-ttu-id="302c4-134">Cosmos DB 데이터베이스 계정에서 가상 네트워크를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="302c4-134">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="302c4-135">허용 된 값: false, true</span><span class="sxs-lookup"><span data-stu-id="302c4-135">Accepted values: false, true</span></span>

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

### <span data-ttu-id="302c4-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="302c4-136">-InputObject</span></span>
<span data-ttu-id="302c4-137">CosmosDB Account 개체</span><span class="sxs-lookup"><span data-stu-id="302c4-137">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="302c4-138">-IpRangeFilter</span><span class="sxs-lookup"><span data-stu-id="302c4-138">-IpRangeFilter</span></span>
<span data-ttu-id="302c4-139">방화벽 지원.</span><span class="sxs-lookup"><span data-stu-id="302c4-139">Firewall support.</span></span>
<span data-ttu-id="302c4-140">지정 된 데이터베이스 계정에 대 한 클라이언트 Ip의 허용 목록으로 포함할 IP 주소 또는 IP 주소 범위 집합을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="302c4-140">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account</span></span>

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

### <span data-ttu-id="302c4-141">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="302c4-141">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="302c4-142">제한 된 부실 일관성에 사용 하는 경우이 값은 부실 (timespan) 허용의 시간을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="302c4-142">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="302c4-143">이 값에 허용 된 범위는 5-86400입니다.</span><span class="sxs-lookup"><span data-stu-id="302c4-143">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="302c4-144">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="302c4-144">-MaxStalenessPrefix</span></span>
<span data-ttu-id="302c4-145">제한 된 만료 일관성에 사용 하는 경우이 값은 허용 되는 부실 요청 수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="302c4-145">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="302c4-146">이 값에 허용 되는 범위는 1-2147483647입니다.</span><span class="sxs-lookup"><span data-stu-id="302c4-146">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="302c4-147">-이름</span><span class="sxs-lookup"><span data-stu-id="302c4-147">-Name</span></span>
<span data-ttu-id="302c4-148">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="302c4-148">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="302c4-149">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="302c4-149">-PublicNetworkAccess</span></span>
<span data-ttu-id="302c4-150">이 서버에 대 한 공개 끝점 액세스가 허용 되는지 여부</span><span class="sxs-lookup"><span data-stu-id="302c4-150">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="302c4-151">사용할 수 있는 값은 다음과 같습니다. ' Enabled ', ' Disabled '</span><span class="sxs-lookup"><span data-stu-id="302c4-151">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="302c4-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="302c4-152">-ResourceGroupName</span></span>
<span data-ttu-id="302c4-153">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="302c4-153">Name of resource group.</span></span>

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

### <span data-ttu-id="302c4-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="302c4-154">-ResourceId</span></span>
<span data-ttu-id="302c4-155">리소스의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="302c4-155">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="302c4-156">태그</span><span class="sxs-lookup"><span data-stu-id="302c4-156">-Tag</span></span>
<span data-ttu-id="302c4-157">태그의 해시 테이블 (키-값 쌍)</span><span class="sxs-lookup"><span data-stu-id="302c4-157">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="302c4-158">빈 문자열을 사용 하 여 기존 태그 지우기</span><span class="sxs-lookup"><span data-stu-id="302c4-158">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="302c4-159">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="302c4-159">-VirtualNetworkRule</span></span>
<span data-ttu-id="302c4-160">가상 네트워크에 대 한 ACL의 문자열 값 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="302c4-160">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="302c4-161">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="302c4-161">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="302c4-162">가상 네트워크에 대 한 PSVirtualNetworkRuleObjects의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="302c4-162">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

```yaml
Type: PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="302c4-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="302c4-163">-WhatIf</span></span>
<span data-ttu-id="302c4-164">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="302c4-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="302c4-165">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="302c4-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="302c4-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="302c4-166">CommonParameters</span></span>
<span data-ttu-id="302c4-167">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="302c4-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="302c4-168">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="302c4-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="302c4-169">입력</span><span class="sxs-lookup"><span data-stu-id="302c4-169">INPUTS</span></span>

### <span data-ttu-id="302c4-170">CosmosDB [] PSCorsRule []</span><span class="sxs-lookup"><span data-stu-id="302c4-170">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="302c4-171">출력</span><span class="sxs-lookup"><span data-stu-id="302c4-171">OUTPUTS</span></span>

### <span data-ttu-id="302c4-172">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="302c4-172">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="302c4-173">상속자</span><span class="sxs-lookup"><span data-stu-id="302c4-173">NOTES</span></span>

## <span data-ttu-id="302c4-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="302c4-174">RELATED LINKS</span></span>
