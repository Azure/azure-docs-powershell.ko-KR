---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/restore-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlServer.md
ms.openlocfilehash: 7eb1105985202bd8cd05a1b2f2e546e4dd834e50
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179081"
---
# <span data-ttu-id="025f9-101">Restore-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="025f9-101">Restore-AzPostgreSqlServer</span></span>

## <span data-ttu-id="025f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="025f9-102">SYNOPSIS</span></span>
<span data-ttu-id="025f9-103">기존 백업에서 서버 복원</span><span class="sxs-lookup"><span data-stu-id="025f9-103">Restore a server from an existing backup</span></span>

## <span data-ttu-id="025f9-104">구문</span><span class="sxs-lookup"><span data-stu-id="025f9-104">SYNTAX</span></span>

### <span data-ttu-id="025f9-105">GeoRestore(기본값)</span><span class="sxs-lookup"><span data-stu-id="025f9-105">GeoRestore (Default)</span></span>
```
Restore-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer> -UseGeoRestore
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="025f9-106">PointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="025f9-106">PointInTimeRestore</span></span>
```
Restore-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer>
 -RestorePointInTime <DateTime> -UsePointInTimeRestore [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="025f9-107">설명</span><span class="sxs-lookup"><span data-stu-id="025f9-107">DESCRIPTION</span></span>
<span data-ttu-id="025f9-108">기존 백업에서 서버 복원</span><span class="sxs-lookup"><span data-stu-id="025f9-108">Restore a server from an existing backup</span></span>

## <span data-ttu-id="025f9-109">예제</span><span class="sxs-lookup"><span data-stu-id="025f9-109">EXAMPLES</span></span>

### <span data-ttu-id="025f9-110">예제 1: GeoReplica 복원을 사용하여 PostgreSql 서버 복원</span><span class="sxs-lookup"><span data-stu-id="025f9-110">Example 1: Restore PostgreSql server using GeoReplica Restore</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName postgresqltestserverreplica | Restore-AzPostgreSqlServer -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG -UseGeoRestore

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="025f9-111">이 cmdlet은 GeoReplica Restore를 사용하여 PostgreSql 서버를 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-111">This cmdlet restores PostgreSql server using GeoReplica Restore.</span></span>

### <span data-ttu-id="025f9-112">예제 2: PointInTime 복원을 사용하여 PostgreSql 서버 복원</span><span class="sxs-lookup"><span data-stu-id="025f9-112">Example 2: Restore PostgreSql server using PointInTime Restore</span></span>
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Restore-AzPostgreSqlServer -Name PostgreSqlTestServerGEO -ResourceGroupName PostgreSqlTestRG -RestorePointInTime $restorePointInTime -UsePointInTimeRestore

Name                    Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                    -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestservergeo eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="025f9-113">이러한 cmdlet은 PointInTime 복원을 사용하여 PostgreSql 서버를 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-113">These cmdlets restore PostgreSql server using PointInTime Restore.</span></span>

## <span data-ttu-id="025f9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="025f9-114">PARAMETERS</span></span>

### <span data-ttu-id="025f9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="025f9-115">-AsJob</span></span>
<span data-ttu-id="025f9-116">명령을 작업으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-116">Run the command as a job.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="025f9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="025f9-117">-DefaultProfile</span></span>
<span data-ttu-id="025f9-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="025f9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="025f9-119">-InputObject</span></span>
<span data-ttu-id="025f9-120">복원할 원본 서버 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-120">The source server object to restore from.</span></span>
<span data-ttu-id="025f9-121">생성을 위해 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="025f9-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="025f9-122">-Location</span><span class="sxs-lookup"><span data-stu-id="025f9-122">-Location</span></span>
<span data-ttu-id="025f9-123">리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-123">The location the resource resides in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="025f9-124">-Name</span><span class="sxs-lookup"><span data-stu-id="025f9-124">-Name</span></span>
<span data-ttu-id="025f9-125">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-125">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="025f9-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="025f9-126">-NoWait</span></span>
<span data-ttu-id="025f9-127">명령을 비동기적으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-127">Run the command asynchronously.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="025f9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="025f9-128">-ResourceGroupName</span></span>
<span data-ttu-id="025f9-129">리소스가 포함된 리소스 그룹의 이름입니다. Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-129">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="025f9-130">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="025f9-130">-RestorePointInTime</span></span>
<span data-ttu-id="025f9-131">리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-131">The location the resource resides in.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="025f9-132">-Sku</span><span class="sxs-lookup"><span data-stu-id="025f9-132">-Sku</span></span>
<span data-ttu-id="025f9-133">SKU의 이름(일반적으로 계층 + 패밀리 + 코어)입니다(예: B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="025f9-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="025f9-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="025f9-134">-SubscriptionId</span></span>
<span data-ttu-id="025f9-135">Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-135">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="025f9-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="025f9-136">-Tag</span></span>
<span data-ttu-id="025f9-137">키-값 쌍의 형태로 애플리케이션별 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-137">Application-specific metadata in the form of key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="025f9-138">-UseGeoRestore</span><span class="sxs-lookup"><span data-stu-id="025f9-138">-UseGeoRestore</span></span>
<span data-ttu-id="025f9-139">지역 모드를 사용하여 복원</span><span class="sxs-lookup"><span data-stu-id="025f9-139">Use Geo mode to restore</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeoRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="025f9-140">-UsePointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="025f9-140">-UsePointInTimeRestore</span></span>
<span data-ttu-id="025f9-141">PointInTime 모드를 사용하여 복원</span><span class="sxs-lookup"><span data-stu-id="025f9-141">Use PointInTime mode to restore</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PointInTimeRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="025f9-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="025f9-142">-Confirm</span></span>
<span data-ttu-id="025f9-143">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="025f9-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="025f9-144">-WhatIf</span></span>
<span data-ttu-id="025f9-145">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="025f9-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="025f9-146">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="025f9-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="025f9-147">CommonParameters</span></span>
<span data-ttu-id="025f9-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="025f9-149">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="025f9-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="025f9-150">입력</span><span class="sxs-lookup"><span data-stu-id="025f9-150">INPUTS</span></span>

### <span data-ttu-id="025f9-151">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="025f9-151">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="025f9-152">출력</span><span class="sxs-lookup"><span data-stu-id="025f9-152">OUTPUTS</span></span>

### <span data-ttu-id="025f9-153">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="025f9-153">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="025f9-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="025f9-154">NOTES</span></span>

<span data-ttu-id="025f9-155">별칭</span><span class="sxs-lookup"><span data-stu-id="025f9-155">ALIASES</span></span>

<span data-ttu-id="025f9-156">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="025f9-156">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="025f9-157">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-157">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="025f9-158">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="025f9-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="025f9-159">INPUTOBJECT: 복원할 원본 <IServer> 서버 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-159">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="025f9-160">`Location <String>`: 리소스가 있는 지리적 위치</span><span class="sxs-lookup"><span data-stu-id="025f9-160">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="025f9-161">`[Tag <ITrackedResourceTags>]`: 리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-161">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="025f9-162">`[(Any) <String>]`: 이 개체에 추가할 수 있는 속성을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-162">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="025f9-163">`[AdministratorLogin <String>]`: 서버의 관리자 로그인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-163">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="025f9-164">서버를 만들 때만 지정할 수 있습니다(생성에 필요).</span><span class="sxs-lookup"><span data-stu-id="025f9-164">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="025f9-165">`[EarliestRestoreDate <DateTime?>]`: 가장 빠른 복원 지점 생성 시간(ISO8601 형식)</span><span class="sxs-lookup"><span data-stu-id="025f9-165">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="025f9-166">`[FullyQualifiedDomainName <String>]`: 서버의 정식 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-166">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="025f9-167">`[IdentityType <IdentityType?>]`: ID 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-167">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="025f9-168">리소스에 대한 Azure Active Directory 주체를 자동으로 만들고 할당하기 위해 이를 'SystemAssigned'로 설정하세요.</span><span class="sxs-lookup"><span data-stu-id="025f9-168">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="025f9-169">`[InfrastructureEncryption <InfrastructureEncryption?>]`: 서버가 인프라 암호화를 사용할 수 있는지 여부를 보여주는 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-169">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="025f9-170">`[MasterServerId <String>]`: 복제본 서버의 마스터 서버 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-170">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="025f9-171">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: 서버에 최소 Tls 버전을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-171">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="025f9-172">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: 이 서버에 대해 공용 네트워크 액세스가 허용되는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-172">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="025f9-173">값은 선택 사항이지만 전달된 경우 'Enabled' 또는 'Disabled'입니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-173">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="025f9-174">`[ReplicaCapacity <Int32?>]`: 마스터 서버가 사용할 수 있는 최대 복제본 수입니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-174">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="025f9-175">`[ReplicationRole <String>]`: 서버의 복제 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-175">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="025f9-176">`[SkuCapacity <Int32?>]`: 서버의 컴퓨팅 단위를 나타내는 확장/확장 용량입니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-176">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="025f9-177">`[SkuFamily <String>]`: 하드웨어의 패밀리입니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-177">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="025f9-178">`[SkuName <String>]`: SKU의 이름(일반적으로 계층 + 패밀리 + 코어)입니다(예: B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="025f9-178">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="025f9-179">`[SkuSize <String>]`: 리소스에서 적절하게 해석할 크기 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-179">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="025f9-180">`[SkuTier <SkuTier?>]`: 특정 SKU의 계층(예: 기본)</span><span class="sxs-lookup"><span data-stu-id="025f9-180">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="025f9-181">`[SslEnforcement <SslEnforcementEnum?>]`: 서버에 연결할 때 ssl 적용을 사용하도록 설정하거나 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-181">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="025f9-182">`[StorageProfileBackupRetentionDay <Int32?>]`: 서버에 대한 백업 보존 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="025f9-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: 서버 백업에 지역 중복 사용 또는 사용 안 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="025f9-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="025f9-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: 저장소 자동 증가를 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="025f9-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="025f9-185">`[StorageProfileStorageMb <Int32?>]`: 서버에 허용되는 최대 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-185">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="025f9-186">`[UserVisibleState <ServerState?>]`: 사용자에게 표시되는 서버의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-186">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="025f9-187">`[Version <ServerVersion?>]`: 서버 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="025f9-187">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="025f9-188">관련 링크</span><span class="sxs-lookup"><span data-stu-id="025f9-188">RELATED LINKS</span></span>

