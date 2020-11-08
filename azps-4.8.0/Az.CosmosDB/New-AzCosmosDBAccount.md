---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
ms.openlocfilehash: f082f9390dd5a00fa5984aa2e0df26e8c3b63636
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056475"
---
# <span data-ttu-id="ece66-101">New-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="ece66-101">New-AzCosmosDBAccount</span></span>

## <span data-ttu-id="ece66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ece66-102">SYNOPSIS</span></span>
<span data-ttu-id="ece66-103">새 CosmosDB 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ece66-103">Create a new CosmosDB Account.</span></span>

## <span data-ttu-id="ece66-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ece66-104">SYNTAX</span></span>

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

## <span data-ttu-id="ece66-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ece66-105">DESCRIPTION</span></span>
<span data-ttu-id="ece66-106">지정 된 ResourceGroup에 새 CosmosDB Account를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ece66-106">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="ece66-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ece66-107">EXAMPLES</span></span>

### <span data-ttu-id="ece66-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ece66-108">Example 1</span></span>
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

<span data-ttu-id="ece66-109">이름 databaseAccountName을 사용 하는 새 CosmosDB 계정이 ResourceGroup resourceGroupName에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="ece66-109">A new CosmosDB Account with name databaseAccountName is created in the ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="ece66-110">변수</span><span class="sxs-lookup"><span data-stu-id="ece66-110">PARAMETERS</span></span>

### <span data-ttu-id="ece66-111">-ApiKind</span><span class="sxs-lookup"><span data-stu-id="ece66-111">-ApiKind</span></span>
<span data-ttu-id="ece66-112">만들 Cosmos DB 데이터베이스 계정의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="ece66-112">The type of Cosmos DB database account to create.</span></span>
<span data-ttu-id="ece66-113">허용 되는 값: GlobalDocumentDB, MongoDB, Gremlin, Table, Cassandra.</span><span class="sxs-lookup"><span data-stu-id="ece66-113">Accepted values: GlobalDocumentDB, MongoDB, Gremlin, Table, Cassandra.</span></span>
<span data-ttu-id="ece66-114">기본값: GlobalDocumentDB</span><span class="sxs-lookup"><span data-stu-id="ece66-114">Default value: GlobalDocumentDB</span></span>

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

### <span data-ttu-id="ece66-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ece66-115">-AsJob</span></span>
<span data-ttu-id="ece66-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ece66-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ece66-117">-확인</span><span class="sxs-lookup"><span data-stu-id="ece66-117">-Confirm</span></span>
<span data-ttu-id="ece66-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece66-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ece66-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="ece66-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="ece66-120">Cosmos DB 데이터베이스 계정의 기본 일관성 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="ece66-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="ece66-121">허용 되는 값: BoundedStaleness, ConsistentPrefix, 궁극적인, Session, Strong</span><span class="sxs-lookup"><span data-stu-id="ece66-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="ece66-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ece66-122">-DefaultProfile</span></span>
<span data-ttu-id="ece66-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ece66-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ece66-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="ece66-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="ece66-125">계정 키를 통해 메타 데이터 리소스 (데이터베이스, 컨테이너, 처리량)에 대 한 쓰기 작업을 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="ece66-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="ece66-126">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="ece66-126">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="ece66-127">계정에서 AnalyticalStorage을 사용할 수 있는지 여부를 나타내는 부울입니다.</span><span class="sxs-lookup"><span data-stu-id="ece66-127">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="ece66-128">-Enable자동 장애 조치</span><span class="sxs-lookup"><span data-stu-id="ece66-128">-EnableAutomaticFailover</span></span>
<span data-ttu-id="ece66-129">비활성으로 인해 지역을 사용할 수 없는 드문 이벤트에서 쓰기 영역의 자동 장애 조치를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece66-129">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="ece66-130">자동 장애 조치 (failover)로 인해 계정에 대 한 새 쓰기 영역이 만들어지고 계정에 대해 구성 된 장애 조치 (failover) 우선 순위에 따라 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ece66-130">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="ece66-131">허용 된 값: false, true</span><span class="sxs-lookup"><span data-stu-id="ece66-131">Accepted values: false, true</span></span>

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

### <span data-ttu-id="ece66-132">-EnableFreeTier</span><span class="sxs-lookup"><span data-stu-id="ece66-132">-EnableFreeTier</span></span>
<span data-ttu-id="ece66-133">계정에서 FreeTier 사용 되는지 여부를 나타내는 부울입니다.</span><span class="sxs-lookup"><span data-stu-id="ece66-133">Bool to indicate if FreeTier is enabled on the account.</span></span>

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

### <span data-ttu-id="ece66-134">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="ece66-134">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="ece66-135">여러 쓰기 위치를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece66-135">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="ece66-136">허용 된 값: false, true</span><span class="sxs-lookup"><span data-stu-id="ece66-136">Accepted values: false, true</span></span>

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

### <span data-ttu-id="ece66-137">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ece66-137">-EnableVirtualNetwork</span></span>
<span data-ttu-id="ece66-138">Cosmos DB 데이터베이스 계정에서 가상 네트워크를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece66-138">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="ece66-139">허용 된 값: false, true</span><span class="sxs-lookup"><span data-stu-id="ece66-139">Accepted values: false, true</span></span>

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

### <span data-ttu-id="ece66-140">-IpRule</span><span class="sxs-lookup"><span data-stu-id="ece66-140">-IpRule</span></span>
<span data-ttu-id="ece66-141">방화벽 지원.</span><span class="sxs-lookup"><span data-stu-id="ece66-141">Firewall support.</span></span> <span data-ttu-id="ece66-142">지정 된 데이터베이스 계정에 대 한 클라이언트 Ip의 허용 목록으로 포함할 IP 주소 또는 IP 주소 범위 집합을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece66-142">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="ece66-143">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="ece66-143">-KeyVaultKeyUri</span></span>
<span data-ttu-id="ece66-144">KeyVault의 URI</span><span class="sxs-lookup"><span data-stu-id="ece66-144">URI of the KeyVault</span></span>

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

### <span data-ttu-id="ece66-145">-위치</span><span class="sxs-lookup"><span data-stu-id="ece66-145">-Location</span></span>
<span data-ttu-id="ece66-146">Cosmos DB 데이터베이스 계정에 위치를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece66-146">Add a location to the Cosmos DB database account.</span></span>
<span data-ttu-id="ece66-147">장애 조치 우선 순위에 따라 정렬 되는 문자열의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="ece66-147">Array of strings, ordered by failover priority.</span></span>

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

### <span data-ttu-id="ece66-148">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="ece66-148">-LocationObject</span></span>
<span data-ttu-id="ece66-149">Cosmos DB 데이터베이스 계정에 위치를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece66-149">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="ece66-150">PSLocation 개체의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="ece66-150">Array of PSLocation objects.</span></span>

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

### <span data-ttu-id="ece66-151">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="ece66-151">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="ece66-152">제한 된 부실 일관성에 사용 하는 경우이 값은 부실 (timespan) 허용의 시간을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ece66-152">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="ece66-153">이 값에 허용 된 범위는 5-86400입니다.</span><span class="sxs-lookup"><span data-stu-id="ece66-153">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="ece66-154">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="ece66-154">-MaxStalenessPrefix</span></span>
<span data-ttu-id="ece66-155">제한 된 만료 일관성에 사용 하는 경우이 값은 허용 되는 부실 요청 수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ece66-155">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="ece66-156">이 값에 허용 되는 범위는 1-2147483647입니다.</span><span class="sxs-lookup"><span data-stu-id="ece66-156">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="ece66-157">-이름</span><span class="sxs-lookup"><span data-stu-id="ece66-157">-Name</span></span>
<span data-ttu-id="ece66-158">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ece66-158">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ece66-159">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="ece66-159">-PublicNetworkAccess</span></span>
<span data-ttu-id="ece66-160">이 서버에 대 한 공개 끝점 액세스가 허용 되는지 여부</span><span class="sxs-lookup"><span data-stu-id="ece66-160">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="ece66-161">사용할 수 있는 값은 다음과 같습니다. ' Enabled ', ' Disabled '</span><span class="sxs-lookup"><span data-stu-id="ece66-161">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="ece66-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ece66-162">-ResourceGroupName</span></span>
<span data-ttu-id="ece66-163">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ece66-163">Name of resource group.</span></span>

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

### <span data-ttu-id="ece66-164">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="ece66-164">-ServerVersion</span></span>
<span data-ttu-id="ece66-165">ServerVersion, MongoDB 계정의 경우에만 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece66-165">ServerVersion, valid only in case of MongoDB Accounts.</span></span>

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

### <span data-ttu-id="ece66-166">태그</span><span class="sxs-lookup"><span data-stu-id="ece66-166">-Tag</span></span>
<span data-ttu-id="ece66-167">태그의 해시 테이블 (키-값 쌍)</span><span class="sxs-lookup"><span data-stu-id="ece66-167">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="ece66-168">빈 문자열을 사용 하 여 기존 태그 지우기</span><span class="sxs-lookup"><span data-stu-id="ece66-168">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="ece66-169">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ece66-169">-VirtualNetworkRule</span></span>
<span data-ttu-id="ece66-170">가상 네트워크에 대 한 ACL의 문자열 값 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="ece66-170">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="ece66-171">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="ece66-171">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="ece66-172">가상 네트워크에 대 한 PSVirtualNetworkRuleObjects의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="ece66-172">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="ece66-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ece66-173">-WhatIf</span></span>
<span data-ttu-id="ece66-174">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ece66-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ece66-175">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ece66-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ece66-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ece66-176">CommonParameters</span></span>
<span data-ttu-id="ece66-177">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece66-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ece66-178">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ece66-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ece66-179">입력</span><span class="sxs-lookup"><span data-stu-id="ece66-179">INPUTS</span></span>

### <span data-ttu-id="ece66-180">CosmosDB [] PSCorsRule []</span><span class="sxs-lookup"><span data-stu-id="ece66-180">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="ece66-181">출력</span><span class="sxs-lookup"><span data-stu-id="ece66-181">OUTPUTS</span></span>

### <span data-ttu-id="ece66-182">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="ece66-182">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="ece66-183">상속자</span><span class="sxs-lookup"><span data-stu-id="ece66-183">NOTES</span></span>

## <span data-ttu-id="ece66-184">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ece66-184">RELATED LINKS</span></span>
