---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
ms.openlocfilehash: 76df37703882e799eb42542cd08d105f62787419
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042565"
---
# <span data-ttu-id="d06ba-101">New-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="d06ba-101">New-AzCosmosDBAccount</span></span>

## <span data-ttu-id="d06ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d06ba-102">SYNOPSIS</span></span>
<span data-ttu-id="d06ba-103">새 CosmosDB 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d06ba-103">Create a new CosmosDB Account.</span></span>

## <span data-ttu-id="d06ba-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d06ba-104">SYNTAX</span></span>

```
New-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover] [-EnableMultipleWriteLocations] [-EnableVirtualNetwork] [-IpRangeFilter <String[]>]
 [-Location <String[]>] [-LocationObject <PSLocation[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-ApiKind <String>] [-PublicNetworkAccess <String>]
 [-DisableKeyBasedMetadataWriteAccess] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d06ba-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d06ba-105">DESCRIPTION</span></span>
<span data-ttu-id="d06ba-106">지정 된 ResourceGroup에 새 CosmosDB Account를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d06ba-106">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="d06ba-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d06ba-107">EXAMPLES</span></span>

### <span data-ttu-id="d06ba-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d06ba-108">Example 1</span></span>
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

<span data-ttu-id="d06ba-109">이름 databaseAccountName을 사용 하는 새 CosmosDB 계정이 ResourceGroup resourceGroupName에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="d06ba-109">A new CosmosDB Account with name databaseAccountName is created in the ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="d06ba-110">변수</span><span class="sxs-lookup"><span data-stu-id="d06ba-110">PARAMETERS</span></span>

### <span data-ttu-id="d06ba-111">-ApiKind</span><span class="sxs-lookup"><span data-stu-id="d06ba-111">-ApiKind</span></span>
<span data-ttu-id="d06ba-112">만들 Cosmos DB 데이터베이스 계정의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="d06ba-112">The type of Cosmos DB database account to create.</span></span>
<span data-ttu-id="d06ba-113">허용 되는 값: GlobalDocumentDB, MongoDB, Gremlin, Table, Cassandra.</span><span class="sxs-lookup"><span data-stu-id="d06ba-113">Accepted values: GlobalDocumentDB, MongoDB, Gremlin, Table, Cassandra.</span></span>
<span data-ttu-id="d06ba-114">기본값: GlobalDocumentDB</span><span class="sxs-lookup"><span data-stu-id="d06ba-114">Default value: GlobalDocumentDB</span></span>

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

### <span data-ttu-id="d06ba-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d06ba-115">-AsJob</span></span>
<span data-ttu-id="d06ba-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d06ba-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d06ba-117">-확인</span><span class="sxs-lookup"><span data-stu-id="d06ba-117">-Confirm</span></span>
<span data-ttu-id="d06ba-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d06ba-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d06ba-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="d06ba-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="d06ba-120">Cosmos DB 데이터베이스 계정의 기본 일관성 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="d06ba-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="d06ba-121">허용 되는 값: BoundedStaleness, ConsistentPrefix, 궁극적인, Session, Strong</span><span class="sxs-lookup"><span data-stu-id="d06ba-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="d06ba-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d06ba-122">-DefaultProfile</span></span>
<span data-ttu-id="d06ba-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d06ba-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d06ba-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="d06ba-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="d06ba-125">계정 키를 통해 메타 데이터 리소스 (데이터베이스, 컨테이너, 처리량)에 대 한 쓰기 작업을 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="d06ba-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="d06ba-126">-Enable자동 장애 조치</span><span class="sxs-lookup"><span data-stu-id="d06ba-126">-EnableAutomaticFailover</span></span>
<span data-ttu-id="d06ba-127">비활성으로 인해 지역을 사용할 수 없는 드문 이벤트에서 쓰기 영역의 자동 장애 조치를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d06ba-127">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="d06ba-128">자동 장애 조치 (failover)로 인해 계정에 대 한 새 쓰기 영역이 만들어지고 계정에 대해 구성 된 장애 조치 (failover) 우선 순위에 따라 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d06ba-128">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="d06ba-129">허용 된 값: false, true</span><span class="sxs-lookup"><span data-stu-id="d06ba-129">Accepted values: false, true</span></span>

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

### <span data-ttu-id="d06ba-130">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="d06ba-130">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="d06ba-131">여러 쓰기 위치를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d06ba-131">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="d06ba-132">허용 된 값: false, true</span><span class="sxs-lookup"><span data-stu-id="d06ba-132">Accepted values: false, true</span></span>

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

### <span data-ttu-id="d06ba-133">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d06ba-133">-EnableVirtualNetwork</span></span>
<span data-ttu-id="d06ba-134">Cosmos DB 데이터베이스 계정에서 가상 네트워크를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d06ba-134">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="d06ba-135">허용 된 값: false, true</span><span class="sxs-lookup"><span data-stu-id="d06ba-135">Accepted values: false, true</span></span>

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

### <span data-ttu-id="d06ba-136">-IpRangeFilter</span><span class="sxs-lookup"><span data-stu-id="d06ba-136">-IpRangeFilter</span></span>
<span data-ttu-id="d06ba-137">방화벽 지원.</span><span class="sxs-lookup"><span data-stu-id="d06ba-137">Firewall support.</span></span>
<span data-ttu-id="d06ba-138">지정 된 데이터베이스 계정에 대 한 클라이언트 Ip의 허용 목록으로 포함할 IP 주소 또는 IP 주소 범위 집합을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d06ba-138">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account</span></span>

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

### <span data-ttu-id="d06ba-139">-위치</span><span class="sxs-lookup"><span data-stu-id="d06ba-139">-Location</span></span>
<span data-ttu-id="d06ba-140">Cosmos DB 데이터베이스 계정에 위치를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d06ba-140">Add a location to the Cosmos DB database account.</span></span>
<span data-ttu-id="d06ba-141">장애 조치 우선 순위에 따라 정렬 되는 문자열의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="d06ba-141">Array of strings, ordered by failover priority.</span></span>

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

### <span data-ttu-id="d06ba-142">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="d06ba-142">-LocationObject</span></span>
<span data-ttu-id="d06ba-143">Cosmos DB 데이터베이스 계정에 위치를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d06ba-143">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="d06ba-144">PSLocation 개체의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="d06ba-144">Array of PSLocation objects.</span></span>

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

### <span data-ttu-id="d06ba-145">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="d06ba-145">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="d06ba-146">제한 된 부실 일관성에 사용 하는 경우이 값은 부실 (timespan) 허용의 시간을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d06ba-146">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="d06ba-147">이 값에 허용 된 범위는 5-86400입니다.</span><span class="sxs-lookup"><span data-stu-id="d06ba-147">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="d06ba-148">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="d06ba-148">-MaxStalenessPrefix</span></span>
<span data-ttu-id="d06ba-149">제한 된 만료 일관성에 사용 하는 경우이 값은 허용 되는 부실 요청 수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d06ba-149">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="d06ba-150">이 값에 허용 되는 범위는 1-2147483647입니다.</span><span class="sxs-lookup"><span data-stu-id="d06ba-150">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="d06ba-151">-이름</span><span class="sxs-lookup"><span data-stu-id="d06ba-151">-Name</span></span>
<span data-ttu-id="d06ba-152">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d06ba-152">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d06ba-153">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="d06ba-153">-PublicNetworkAccess</span></span>
<span data-ttu-id="d06ba-154">이 서버에 대 한 공개 끝점 액세스가 허용 되는지 여부</span><span class="sxs-lookup"><span data-stu-id="d06ba-154">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="d06ba-155">사용할 수 있는 값은 다음과 같습니다. ' Enabled ', ' Disabled '</span><span class="sxs-lookup"><span data-stu-id="d06ba-155">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="d06ba-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d06ba-156">-ResourceGroupName</span></span>
<span data-ttu-id="d06ba-157">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d06ba-157">Name of resource group.</span></span>

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

### <span data-ttu-id="d06ba-158">태그</span><span class="sxs-lookup"><span data-stu-id="d06ba-158">-Tag</span></span>
<span data-ttu-id="d06ba-159">태그의 해시 테이블 (키-값 쌍)</span><span class="sxs-lookup"><span data-stu-id="d06ba-159">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="d06ba-160">빈 문자열을 사용 하 여 기존 태그 지우기</span><span class="sxs-lookup"><span data-stu-id="d06ba-160">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="d06ba-161">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d06ba-161">-VirtualNetworkRule</span></span>
<span data-ttu-id="d06ba-162">가상 네트워크에 대 한 ACL의 문자열 값 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="d06ba-162">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="d06ba-163">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="d06ba-163">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="d06ba-164">가상 네트워크에 대 한 PSVirtualNetworkRuleObjects의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="d06ba-164">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="d06ba-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d06ba-165">-WhatIf</span></span>
<span data-ttu-id="d06ba-166">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d06ba-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d06ba-167">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d06ba-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d06ba-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d06ba-168">CommonParameters</span></span>
<span data-ttu-id="d06ba-169">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d06ba-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d06ba-170">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d06ba-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d06ba-171">입력</span><span class="sxs-lookup"><span data-stu-id="d06ba-171">INPUTS</span></span>

### <span data-ttu-id="d06ba-172">CosmosDB [] PSCorsRule []</span><span class="sxs-lookup"><span data-stu-id="d06ba-172">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="d06ba-173">출력</span><span class="sxs-lookup"><span data-stu-id="d06ba-173">OUTPUTS</span></span>

### <span data-ttu-id="d06ba-174">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="d06ba-174">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="d06ba-175">상속자</span><span class="sxs-lookup"><span data-stu-id="d06ba-175">NOTES</span></span>

## <span data-ttu-id="d06ba-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d06ba-176">RELATED LINKS</span></span>
