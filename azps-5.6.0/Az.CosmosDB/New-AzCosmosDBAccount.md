---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
ms.openlocfilehash: 75085bed9c1f9b0cd0c0328b9a166c6dc08a60b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992824"
---
# <span data-ttu-id="9fa67-101">New-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="9fa67-101">New-AzCosmosDBAccount</span></span>

## <span data-ttu-id="9fa67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fa67-102">SYNOPSIS</span></span>
<span data-ttu-id="9fa67-103">새 CosmosDB 계정을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-103">Create a new CosmosDB Account.</span></span>

## <span data-ttu-id="9fa67-104">구문</span><span class="sxs-lookup"><span data-stu-id="9fa67-104">SYNTAX</span></span>

```
New-AzCosmosDBAccount [-EnableAutomaticFailover] [-EnableMultipleWriteLocations] [-EnableVirtualNetwork]
 [-ApiKind <String>] [-DisableKeyBasedMetadataWriteAccess] [-EnableFreeTier <Boolean>] [-Location <String[]>]
 [-LocationObject <PSLocation[]>] -ResourceGroupName <String> -Name <String>
 [-DefaultConsistencyLevel <String>] [-IpRule <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-PublicNetworkAccess <String>]
 [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob] [-NetworkAclBypass <String>]
 [-NetworkAclBypassResourceId <String[]>] [-ServerVersion <String>] [-BackupIntervalInMinutes <Int32>]
 [-BackupRetentionIntervalInHours <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9fa67-105">설명</span><span class="sxs-lookup"><span data-stu-id="9fa67-105">DESCRIPTION</span></span>
<span data-ttu-id="9fa67-106">주어진 ResourceGroup에서 새 CosmosDB 계정을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-106">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="9fa67-107">예제</span><span class="sxs-lookup"><span data-stu-id="9fa67-107">EXAMPLES</span></span>

### <span data-ttu-id="9fa67-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="9fa67-108">Example 1</span></span>
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
NetworkAclBypass              : None
NetworkAclBypassResourceIds   : {}
```

<span data-ttu-id="9fa67-109">Name databaseAccountName이 있는 새 CosmosDB 계정이 ResourceGroup resourceGroupName에 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-109">A new CosmosDB Account with name databaseAccountName is created in the ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="9fa67-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9fa67-110">PARAMETERS</span></span>

### <span data-ttu-id="9fa67-111">-ApiKind</span><span class="sxs-lookup"><span data-stu-id="9fa67-111">-ApiKind</span></span>
<span data-ttu-id="9fa67-112">만들 Cosmos DB 데이터베이스 계정의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-112">The type of Cosmos DB database account to create.</span></span>
<span data-ttu-id="9fa67-113">수락된 값: Sql, MongoDB, Gremlin, Table, Cassandra.</span><span class="sxs-lookup"><span data-stu-id="9fa67-113">Accepted values: Sql, MongoDB, Gremlin, Table, Cassandra.</span></span>
<span data-ttu-id="9fa67-114">기본값: Sql</span><span class="sxs-lookup"><span data-stu-id="9fa67-114">Default value: Sql</span></span>

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

### <span data-ttu-id="9fa67-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9fa67-115">-AsJob</span></span>
<span data-ttu-id="9fa67-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9fa67-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9fa67-117">-BackupIntervalInMinutes</span><span class="sxs-lookup"><span data-stu-id="9fa67-117">-BackupIntervalInMinutes</span></span>
<span data-ttu-id="9fa67-118">백업이 수행되는 간격(분)(주기적 모드 백업이 있는 계정에만 해당)</span><span class="sxs-lookup"><span data-stu-id="9fa67-118">The interval(in minutes) with which backup are taken (only for accounts with periodic mode backups)</span></span>

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

### <span data-ttu-id="9fa67-119">-BackupRetentionIntervalInHours</span><span class="sxs-lookup"><span data-stu-id="9fa67-119">-BackupRetentionIntervalInHours</span></span>
<span data-ttu-id="9fa67-120">각 백업이 유지되는 시간(시간)(주기적 모드 백업이 있는 계정에만 해당)</span><span class="sxs-lookup"><span data-stu-id="9fa67-120">The time(in hours) for which each backup is retained (only for accounts with periodic mode backups)</span></span>

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

### <span data-ttu-id="9fa67-121">-확인</span><span class="sxs-lookup"><span data-stu-id="9fa67-121">-Confirm</span></span>
<span data-ttu-id="9fa67-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fa67-123">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="9fa67-123">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="9fa67-124">Cosmos DB 데이터베이스 계정의 기본 일관성 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-124">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="9fa67-125">수락된 값: BoundedStaleness, ConsistentPrefix, 최종, 세션, 강력한</span><span class="sxs-lookup"><span data-stu-id="9fa67-125">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="9fa67-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fa67-126">-DefaultProfile</span></span>
<span data-ttu-id="9fa67-127">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fa67-128">-DisableKeyBasedMetadataWriteAccesss</span><span class="sxs-lookup"><span data-stu-id="9fa67-128">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="9fa67-129">계정 키를 통해 메타데이터 리소스(데이터베이스, 컨테이너, 전송 데이터)에 대한 쓰기 작업을 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="9fa67-129">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="9fa67-130">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="9fa67-130">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="9fa67-131">Bool을 통해 계정에서 분석Storage를 사용하도록 설정되어 있는 경우를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-131">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="9fa67-132">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="9fa67-132">-EnableAutomaticFailover</span></span>
<span data-ttu-id="9fa67-133">중단으로 인해 지역을 사용할 수 없는 드문 경우 쓰기 영역의 자동 장애 조치(failover)를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-133">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="9fa67-134">자동 장애 조치(failover)는 계정에 대한 새 쓰기 지역을 발생하며 계정에 대해 구성된 장애 조치(failover) 우선 순위에 따라 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-134">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="9fa67-135">수락된 값: false, true</span><span class="sxs-lookup"><span data-stu-id="9fa67-135">Accepted values: false, true</span></span>

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

### <span data-ttu-id="9fa67-136">-EnableFreeTier</span><span class="sxs-lookup"><span data-stu-id="9fa67-136">-EnableFreeTier</span></span>
<span data-ttu-id="9fa67-137">계정에서 FreeTier를 사용하도록 설정되어 있는 경우를 나타내는 Bool입니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-137">Bool to indicate if FreeTier is enabled on the account.</span></span>

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

### <span data-ttu-id="9fa67-138">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="9fa67-138">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="9fa67-139">여러 쓰기 위치를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-139">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="9fa67-140">수락된 값: false, true</span><span class="sxs-lookup"><span data-stu-id="9fa67-140">Accepted values: false, true</span></span>

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

### <span data-ttu-id="9fa67-141">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9fa67-141">-EnableVirtualNetwork</span></span>
<span data-ttu-id="9fa67-142">Cosmos DB 데이터베이스 계정에서 가상 네트워크를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-142">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="9fa67-143">수락된 값: false, true</span><span class="sxs-lookup"><span data-stu-id="9fa67-143">Accepted values: false, true</span></span>

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

### <span data-ttu-id="9fa67-144">-IpRule</span><span class="sxs-lookup"><span data-stu-id="9fa67-144">-IpRule</span></span>
<span data-ttu-id="9fa67-145">방화벽 지원.</span><span class="sxs-lookup"><span data-stu-id="9fa67-145">Firewall support.</span></span> <span data-ttu-id="9fa67-146">특정 데이터베이스 계정에 대해 허용되는 클라이언트 IP 목록으로 포함될 CIDR 형식의 IP 주소 또는 IP 주소 범위 집합을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-146">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="9fa67-147">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="9fa67-147">-KeyVaultKeyUri</span></span>
<span data-ttu-id="9fa67-148">KeyVault의 URI</span><span class="sxs-lookup"><span data-stu-id="9fa67-148">URI of the KeyVault</span></span>

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

### <span data-ttu-id="9fa67-149">-Location</span><span class="sxs-lookup"><span data-stu-id="9fa67-149">-Location</span></span>
<span data-ttu-id="9fa67-150">Cosmos DB 데이터베이스 계정에 위치를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-150">Add a location to the Cosmos DB database account.</span></span>
<span data-ttu-id="9fa67-151">장애 조치(failover) 우선 순위로 순서가 지정된 문자열 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-151">Array of strings, ordered by failover priority.</span></span>

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

### <span data-ttu-id="9fa67-152">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="9fa67-152">-LocationObject</span></span>
<span data-ttu-id="9fa67-153">Cosmos DB 데이터베이스 계정에 위치를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-153">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="9fa67-154">PSLocation 개체의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-154">Array of PSLocation objects.</span></span>

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

### <span data-ttu-id="9fa67-155">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="9fa67-155">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="9fa67-156">경계 부실 일관성과 함께 사용하는 경우 이 값은 부실(시간)을 용인하는 시간 양을 나타냈습니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-156">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="9fa67-157">이 값에 대해 허용되는 범위는 5-86400입니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-157">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="9fa67-158">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="9fa67-158">-MaxStalenessPrefix</span></span>
<span data-ttu-id="9fa67-159">바인딩된 부실 일관성과 함께 사용하는 경우 이 값은 부실 요청의 수를 나타냈습니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-159">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="9fa67-160">이 값에 대해 허용되는 범위는 1 - 2,147,483,647입니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-160">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="9fa67-161">-Name</span><span class="sxs-lookup"><span data-stu-id="9fa67-161">-Name</span></span>
<span data-ttu-id="9fa67-162">Cosmos DB 데이터베이스 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-162">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9fa67-163">-NetworkAclBypass</span><span class="sxs-lookup"><span data-stu-id="9fa67-163">-NetworkAclBypass</span></span>
<span data-ttu-id="9fa67-164">Synapse Link에 대해 이 계정에 대해 네트워크 Acl Bypass를 사용하도록 설정되어 있는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-164">Whether or not Network Acl Bypass is enabled for this account for Synapse Link.</span></span> <span data-ttu-id="9fa67-165">가능한 값은 'None', 'AzureServices'를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-165">Possible values include: 'None', 'AzureServices'.</span></span>

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

### <span data-ttu-id="9fa67-166">-NetworkAclBypassResourceId</span><span class="sxs-lookup"><span data-stu-id="9fa67-166">-NetworkAclBypassResourceId</span></span>
<span data-ttu-id="9fa67-167">Synapse Link에 대한 네트워크 Acl 우회를 허용하는 리소스 ID 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-167">List of Resource Ids to allow Network Acl Bypass for Synapse Link.</span></span>

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

### <span data-ttu-id="9fa67-168">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="9fa67-168">-PublicNetworkAccess</span></span>
<span data-ttu-id="9fa67-169">이 서버에 대해 공용 엔드포인트 액세스가 허용되는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-169">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="9fa67-170">가능한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-170">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="9fa67-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fa67-171">-ResourceGroupName</span></span>
<span data-ttu-id="9fa67-172">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-172">Name of resource group.</span></span>

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

### <span data-ttu-id="9fa67-173">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="9fa67-173">-ServerVersion</span></span>
<span data-ttu-id="9fa67-174">ServerVersion, MongoDB 계정의 경우만 유효합니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-174">ServerVersion, valid only in case of MongoDB Accounts.</span></span>

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

### <span data-ttu-id="9fa67-175">-Tag</span><span class="sxs-lookup"><span data-stu-id="9fa67-175">-Tag</span></span>
<span data-ttu-id="9fa67-176">키 값 쌍으로 태그의 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-176">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="9fa67-177">빈 문자열을 사용하여 기존 태그를 지우면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-177">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="9fa67-178">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9fa67-178">-VirtualNetworkRule</span></span>
<span data-ttu-id="9fa67-179">가상 네트워크에 대한 ACL의 문자열 값의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-179">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="9fa67-180">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="9fa67-180">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="9fa67-181">가상 네트워크에 대한 PSVirtualNetworkRuleObjects의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-181">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="9fa67-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fa67-182">-WhatIf</span></span>
<span data-ttu-id="9fa67-183">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fa67-184">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fa67-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fa67-185">CommonParameters</span></span>
<span data-ttu-id="9fa67-186">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9fa67-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fa67-187">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9fa67-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fa67-188">입력</span><span class="sxs-lookup"><span data-stu-id="9fa67-188">INPUTS</span></span>

### <span data-ttu-id="9fa67-189">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span><span class="sxs-lookup"><span data-stu-id="9fa67-189">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="9fa67-190">출력</span><span class="sxs-lookup"><span data-stu-id="9fa67-190">OUTPUTS</span></span>

### <span data-ttu-id="9fa67-191">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="9fa67-191">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="9fa67-192">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9fa67-192">NOTES</span></span>

## <span data-ttu-id="9fa67-193">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9fa67-193">RELATED LINKS</span></span>
