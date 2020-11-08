---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlReplica.md
ms.openlocfilehash: e3c0d7e8d3b3d9fe42bc97c40ad54424b7bfd0da
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217567"
---
# <span data-ttu-id="e2b1e-101">New-AzPostgreSqlReplica</span><span class="sxs-lookup"><span data-stu-id="e2b1e-101">New-AzPostgreSqlReplica</span></span>

## <span data-ttu-id="e2b1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2b1e-102">SYNOPSIS</span></span>
<span data-ttu-id="e2b1e-103">기존 데이터베이스에서 새 복제본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-103">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="e2b1e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e2b1e-104">SYNTAX</span></span>

```
New-AzPostgreSqlReplica -ReplicaName <String> -ResourceGroupName <String> -Master <IServer>
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e2b1e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e2b1e-105">DESCRIPTION</span></span>
<span data-ttu-id="e2b1e-106">기존 데이터베이스에서 새 복제본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-106">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="e2b1e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e2b1e-107">EXAMPLES</span></span>

### <span data-ttu-id="e2b1e-108">예제 1: 새 PostgreSql server 복제본 만들기</span><span class="sxs-lookup"><span data-stu-id="e2b1e-108">Example 1: Create a new PostgreSql server replica</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | New-AzPostgreSqlReplica -ReplicaName PostgreSqlTestServerReplica -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="e2b1e-109">이 cmdlet은 새 PostgreSql server 복제본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-109">This cmdlet creates a new PostgreSql server replica.</span></span>

### <span data-ttu-id="e2b1e-110">예제 2: 새 PostgreSql server 복제본 만들기</span><span class="sxs-lookup"><span data-stu-id="e2b1e-110">Example 2: Create a new PostgreSql server replica</span></span>
```powershell
PS C:\> $pgDb = Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer 
PS C:\> New-AzPostgreSqlReplica -Master $pgDb -ReplicaName PostgreSqlTestServerReplica -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="e2b1e-111">이 cmdlet은 새 PostgreSql server 복제본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-111">This cmdlet creates a new PostgreSql server replica.</span></span>

## <span data-ttu-id="e2b1e-112">변수</span><span class="sxs-lookup"><span data-stu-id="e2b1e-112">PARAMETERS</span></span>

### <span data-ttu-id="e2b1e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2b1e-113">-AsJob</span></span>
<span data-ttu-id="e2b1e-114">명령을 작업으로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="e2b1e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2b1e-115">-DefaultProfile</span></span>
<span data-ttu-id="e2b1e-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2b1e-117">-위치</span><span class="sxs-lookup"><span data-stu-id="e2b1e-117">-Location</span></span>
<span data-ttu-id="e2b1e-118">리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-118">The location the resource resides in.</span></span>

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

### <span data-ttu-id="e2b1e-119">-마스터</span><span class="sxs-lookup"><span data-stu-id="e2b1e-119">-Master</span></span>
<span data-ttu-id="e2b1e-120">복제를 만들 원본 서버 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-120">The source server object to create replica from.</span></span>
<span data-ttu-id="e2b1e-121">생성 하려면 마스터 속성에 대 한 메모 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-121">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2b1e-122">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e2b1e-122">-NoWait</span></span>
<span data-ttu-id="e2b1e-123">비동기적으로 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="e2b1e-124">-ReplicaName</span><span class="sxs-lookup"><span data-stu-id="e2b1e-124">-ReplicaName</span></span>
<span data-ttu-id="e2b1e-125">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-125">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicaServerName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2b1e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2b1e-126">-ResourceGroupName</span></span>
<span data-ttu-id="e2b1e-127">리소스가 포함 된 리소스 그룹의 이름입니다. Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-127">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e2b1e-128">-Sku</span><span class="sxs-lookup"><span data-stu-id="e2b1e-128">-Sku</span></span>
<span data-ttu-id="e2b1e-129">Sku (일반적으로 계층 + 패밀리 + 코어)의 이름 (예: B_Gen4_1 GP_Gen5_8)입니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-129">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="e2b1e-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e2b1e-130">-SubscriptionId</span></span>
<span data-ttu-id="e2b1e-131">Azure 구독을 식별 하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="e2b1e-132">-확인</span><span class="sxs-lookup"><span data-stu-id="e2b1e-132">-Confirm</span></span>
<span data-ttu-id="e2b1e-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2b1e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2b1e-134">-WhatIf</span></span>
<span data-ttu-id="e2b1e-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2b1e-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2b1e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2b1e-137">CommonParameters</span></span>
<span data-ttu-id="e2b1e-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2b1e-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2b1e-140">입력</span><span class="sxs-lookup"><span data-stu-id="e2b1e-140">INPUTS</span></span>

### <span data-ttu-id="e2b1e-141">PostgreSql. Api20171201. i m m.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="e2b1e-142">출력</span><span class="sxs-lookup"><span data-stu-id="e2b1e-142">OUTPUTS</span></span>

### <span data-ttu-id="e2b1e-143">PostgreSql. Api20171201. i m m.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="e2b1e-144">상속자</span><span class="sxs-lookup"><span data-stu-id="e2b1e-144">NOTES</span></span>

<span data-ttu-id="e2b1e-145">별칭과</span><span class="sxs-lookup"><span data-stu-id="e2b1e-145">ALIASES</span></span>

<span data-ttu-id="e2b1e-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="e2b1e-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e2b1e-147">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e2b1e-148">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e2b1e-149">MASTER <IServer> : 복제본을 만들 원본 서버 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-149">MASTER <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="e2b1e-150">`Location <String>`: 리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-150">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="e2b1e-151">`[Tag <ITrackedResourceTags>]`: 키-값 쌍의 형식으로 된 응용 프로그램 관련 메타 데이터</span><span class="sxs-lookup"><span data-stu-id="e2b1e-151">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="e2b1e-152">`[(Any) <String>]`:이 개체에 모든 속성이 추가 될 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-152">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="e2b1e-153">`[AdministratorLogin <String>]`: 서버의 관리자 로그인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-153">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="e2b1e-154">서버를 만드는 경우에만 지정할 수 있습니다 (만들기에 필요 함).</span><span class="sxs-lookup"><span data-stu-id="e2b1e-154">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="e2b1e-155">`[EarliestRestoreDate <DateTime?>]`: 초기 복원 시점 생성 시간 (ISO8601 형식)</span><span class="sxs-lookup"><span data-stu-id="e2b1e-155">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="e2b1e-156">`[FullyQualifiedDomainName <String>]`: 서버의 정규화 된 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-156">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="e2b1e-157">`[IdentityType <IdentityType?>]`: Id 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-157">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="e2b1e-158">해당 리소스에 대 한 Azure Active Directory 보안 주체를 자동으로 만들고 할당 하려면이를 ' SystemAssigned '로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-158">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="e2b1e-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`: 서버에서 인프라 암호화를 사용 하는지 여부를 나타내는 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="e2b1e-160">`[MasterServerId <String>]`: 복제본 서버의 마스터 서버 id입니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-160">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="e2b1e-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: 서버에 대해 최소 Tls 버전을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="e2b1e-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`:이 서버에 공용 네트워크 액세스가 허용 되는지 여부</span><span class="sxs-lookup"><span data-stu-id="e2b1e-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="e2b1e-163">값은 선택 사항 이지만, 전달 되는 경우에는 ' Enabled ' 또는 ' Disabled ' 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-163">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="e2b1e-164">`[ReplicaCapacity <Int32?>]`: 마스터 서버에 포함할 수 있는 최대 복제 데이터베이스 수입니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-164">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="e2b1e-165">`[ReplicationRole <String>]`: 서버의 복제 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-165">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="e2b1e-166">`[SkuCapacity <Int32?>]`: 서버의 계산 단위를 나타내는 스케일 업/out 용량입니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-166">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="e2b1e-167">`[SkuFamily <String>]`: 하드웨어의 패밀리입니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-167">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="e2b1e-168">`[SkuName <String>]`: Sku의 이름 (일반적으로 계층 + 패밀리 + 코어) (예: B_Gen4_1 GP_Gen5_8)입니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-168">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="e2b1e-169">`[SkuSize <String>]`: 리소스에 따라 적절 하 게 해석 되는 크기 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-169">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="e2b1e-170">`[SkuTier <SkuTier?>]`: 특정 SKU (예: 기본)의 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-170">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="e2b1e-171">`[SslEnforcement <SslEnforcementEnum?>]`: 서버에 연결할 때 ssl 적용 여부를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-171">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="e2b1e-172">`[StorageProfileBackupRetentionDay <Int32?>]`: 서버에 대 한 백업 보존 일입니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="e2b1e-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: 서버 백업에 대해 지리적 중복을 사용 하거나 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="e2b1e-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: 저장소 자동 증가를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="e2b1e-175">`[StorageProfileStorageMb <Int32?>]`: 서버에 허용 된 최대 저장소.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-175">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="e2b1e-176">`[UserVisibleState <ServerState?>]`: 사용자에 게 표시 되는 서버의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-176">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="e2b1e-177">`[Version <ServerVersion?>]`: 서버 버전.</span><span class="sxs-lookup"><span data-stu-id="e2b1e-177">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="e2b1e-178">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2b1e-178">RELATED LINKS</span></span>

