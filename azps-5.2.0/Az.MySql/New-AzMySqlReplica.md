---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlReplica.md
ms.openlocfilehash: 54463e38982a711f98515879f826a3cd2e068384
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372744"
---
# <span data-ttu-id="b3f8a-101">New-AzMySqlReplica</span><span class="sxs-lookup"><span data-stu-id="b3f8a-101">New-AzMySqlReplica</span></span>

## <span data-ttu-id="b3f8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3f8a-102">SYNOPSIS</span></span>
<span data-ttu-id="b3f8a-103">기존 데이터베이스에서 새 복제본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-103">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="b3f8a-104">구문</span><span class="sxs-lookup"><span data-stu-id="b3f8a-104">SYNTAX</span></span>

```
New-AzMySqlReplica -Replica <String> -ResourceGroupName <String> -Master <IServer> [-SubscriptionId <String>]
 [-Location <String>] [-Sku <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="b3f8a-105">설명</span><span class="sxs-lookup"><span data-stu-id="b3f8a-105">DESCRIPTION</span></span>
<span data-ttu-id="b3f8a-106">기존 데이터베이스에서 새 복제본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-106">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="b3f8a-107">예제</span><span class="sxs-lookup"><span data-stu-id="b3f8a-107">EXAMPLES</span></span>

### <span data-ttu-id="b3f8a-108">예제 1: 새 MySql 서버 복제본 만들기</span><span class="sxs-lookup"><span data-stu-id="b3f8a-108">Example 1: Create a new MySql server replica</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | New-AzMySqlReplica -Replica mysql-test-replica -ResourceGroupName PowershellMySqlTest

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="b3f8a-109">이 cmdlet은 새 MySql 서버 복제본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-109">This cmdlet creates a new MySql server replica.</span></span>

### <span data-ttu-id="b3f8a-110">예제 2: 새 MySql 서버 복제본 만들기</span><span class="sxs-lookup"><span data-stu-id="b3f8a-110">Example 2: Create a new MySql server replica</span></span>
```powershell
PS C:\> $mysql = Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test
PS C:\> New-AzMySqlReplica -Master $mysql -Replica mysql-test-replica -ResourceGroupName PowershellMySqlTest

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="b3f8a-111">매개 변수 master(inputobject)가 있는 이 cmdlet은 새 MySql 서버 복제본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-111">This cmdlet with parameter master(inputobject) creates a new MySql server replica.</span></span>

## <span data-ttu-id="b3f8a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3f8a-112">PARAMETERS</span></span>

### <span data-ttu-id="b3f8a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3f8a-113">-AsJob</span></span>
<span data-ttu-id="b3f8a-114">명령을 작업으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="b3f8a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3f8a-115">-DefaultProfile</span></span>
<span data-ttu-id="b3f8a-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3f8a-117">-Location</span><span class="sxs-lookup"><span data-stu-id="b3f8a-117">-Location</span></span>
<span data-ttu-id="b3f8a-118">리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-118">The location the resource resides in.</span></span>

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

### <span data-ttu-id="b3f8a-119">-Master</span><span class="sxs-lookup"><span data-stu-id="b3f8a-119">-Master</span></span>
<span data-ttu-id="b3f8a-120">복제본을 만들 원본 서버 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-120">The source server object to create replica from.</span></span>
<span data-ttu-id="b3f8a-121">생성을 위해 MASTER 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-121">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3f8a-122">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b3f8a-122">-NoWait</span></span>
<span data-ttu-id="b3f8a-123">명령을 비동기적으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="b3f8a-124">-Replica</span><span class="sxs-lookup"><span data-stu-id="b3f8a-124">-Replica</span></span>
<span data-ttu-id="b3f8a-125">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-125">The name of the server.</span></span>

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

### <span data-ttu-id="b3f8a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3f8a-126">-ResourceGroupName</span></span>
<span data-ttu-id="b3f8a-127">리소스가 포함된 리소스 그룹의 이름입니다. Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-127">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b3f8a-128">-Sku</span><span class="sxs-lookup"><span data-stu-id="b3f8a-128">-Sku</span></span>
<span data-ttu-id="b3f8a-129">SKU의 이름(일반적으로 계층 + 패밀리 + 코어)입니다(예: B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-129">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="b3f8a-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b3f8a-130">-SubscriptionId</span></span>
<span data-ttu-id="b3f8a-131">Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="b3f8a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3f8a-132">-Confirm</span></span>
<span data-ttu-id="b3f8a-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3f8a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3f8a-134">-WhatIf</span></span>
<span data-ttu-id="b3f8a-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b3f8a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3f8a-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3f8a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3f8a-137">CommonParameters</span></span>
<span data-ttu-id="b3f8a-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3f8a-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3f8a-140">입력</span><span class="sxs-lookup"><span data-stu-id="b3f8a-140">INPUTS</span></span>

### <span data-ttu-id="b3f8a-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="b3f8a-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="b3f8a-142">출력</span><span class="sxs-lookup"><span data-stu-id="b3f8a-142">OUTPUTS</span></span>

### <span data-ttu-id="b3f8a-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="b3f8a-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="b3f8a-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b3f8a-144">NOTES</span></span>

<span data-ttu-id="b3f8a-145">별칭</span><span class="sxs-lookup"><span data-stu-id="b3f8a-145">ALIASES</span></span>

<span data-ttu-id="b3f8a-146">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="b3f8a-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b3f8a-147">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b3f8a-148">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b3f8a-149">MASTER: <IServer> 복제본을 만들 원본 서버 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-149">MASTER <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="b3f8a-150">`Location <String>`: 리소스가 있는 지리적 위치</span><span class="sxs-lookup"><span data-stu-id="b3f8a-150">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="b3f8a-151">`SkuName <String>`: SKU의 이름(일반적으로 계층 + 패밀리 + 코어)입니다(예: B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-151">`SkuName <String>`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="b3f8a-152">`[Tag <ITrackedResourceTags>]`: 리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-152">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="b3f8a-153">`[(Any) <String>]`: 이 개체에 추가할 수 있는 속성을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-153">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="b3f8a-154">`[AdministratorLogin <String>]`: 서버의 관리자 로그인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-154">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="b3f8a-155">서버를 만들 때만 지정할 수 있습니다(생성에 필요).</span><span class="sxs-lookup"><span data-stu-id="b3f8a-155">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="b3f8a-156">`[EarliestRestoreDate <DateTime?>]`: 가장 빠른 복원 지점 생성 시간(ISO8601 형식)</span><span class="sxs-lookup"><span data-stu-id="b3f8a-156">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="b3f8a-157">`[FullyQualifiedDomainName <String>]`: 서버의 정식 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-157">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="b3f8a-158">`[IdentityType <IdentityType?>]`: ID 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-158">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="b3f8a-159">리소스에 대한 Azure Active Directory 주체를 자동으로 만들고 할당하기 위해 이를 'SystemAssigned'로 설정하세요.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-159">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="b3f8a-160">`[InfrastructureEncryption <InfrastructureEncryption?>]`: 서버가 인프라 암호화를 사용할 수 있는지 여부를 보여주는 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-160">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="b3f8a-161">`[MasterServerId <String>]`: 복제본 서버의 마스터 서버 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-161">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="b3f8a-162">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: 서버에 최소 Tls 버전을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-162">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="b3f8a-163">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: 이 서버에 대해 공용 네트워크 액세스가 허용되는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-163">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="b3f8a-164">값은 선택 사항이지만 전달된 경우 'Enabled' 또는 'Disabled'입니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-164">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="b3f8a-165">`[ReplicaCapacity <Int32?>]`: 마스터 서버가 사용할 수 있는 최대 복제본 수입니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-165">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="b3f8a-166">`[ReplicationRole <String>]`: 서버의 복제 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-166">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="b3f8a-167">`[SkuCapacity <Int32?>]`: 서버의 컴퓨팅 단위를 나타내는 확장/확장 용량입니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-167">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="b3f8a-168">`[SkuFamily <String>]`: 하드웨어의 패밀리입니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-168">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="b3f8a-169">`[SkuSize <String>]`: 리소스에서 적절하게 해석할 크기 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-169">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="b3f8a-170">`[SkuTier <SkuTier?>]`: 특정 SKU의 계층(예: 기본)</span><span class="sxs-lookup"><span data-stu-id="b3f8a-170">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="b3f8a-171">`[SslEnforcement <SslEnforcementEnum?>]`: 서버에 연결할 때 ssl 적용을 사용하도록 설정하거나 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-171">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="b3f8a-172">`[StorageProfileBackupRetentionDay <Int32?>]`: 서버에 대한 백업 보존 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="b3f8a-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: 서버 백업에 지역 중복 사용 또는 사용 안 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="b3f8a-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="b3f8a-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: 저장소 자동 증가를 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="b3f8a-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="b3f8a-175">`[StorageProfileStorageMb <Int32?>]`: 서버에 허용되는 최대 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-175">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="b3f8a-176">`[UserVisibleState <ServerState?>]`: 사용자에게 표시되는 서버의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-176">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="b3f8a-177">`[Version <ServerVersion?>]`: 서버 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="b3f8a-177">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="b3f8a-178">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b3f8a-178">RELATED LINKS</span></span>

