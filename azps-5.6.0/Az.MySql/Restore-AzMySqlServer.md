---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/restore-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
ms.openlocfilehash: 95807621ffb054610a5778872db243eea50a7efa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968912"
---
# <span data-ttu-id="f4c17-101">Restore-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="f4c17-101">Restore-AzMySqlServer</span></span>

## <span data-ttu-id="f4c17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4c17-102">SYNOPSIS</span></span>
<span data-ttu-id="f4c17-103">기존 백업에서 서버 복원</span><span class="sxs-lookup"><span data-stu-id="f4c17-103">Restore a server from an existing backup</span></span>

## <span data-ttu-id="f4c17-104">구문</span><span class="sxs-lookup"><span data-stu-id="f4c17-104">SYNTAX</span></span>

### <span data-ttu-id="f4c17-105">GeoRestore(기본값)</span><span class="sxs-lookup"><span data-stu-id="f4c17-105">GeoRestore (Default)</span></span>
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer> -UseGeoRestore
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f4c17-106">PointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="f4c17-106">PointInTimeRestore</span></span>
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer>
 -RestorePointInTime <DateTime> -UsePointInTimeRestore [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="f4c17-107">설명</span><span class="sxs-lookup"><span data-stu-id="f4c17-107">DESCRIPTION</span></span>
<span data-ttu-id="f4c17-108">기존 백업에서 서버 복원</span><span class="sxs-lookup"><span data-stu-id="f4c17-108">Restore a server from an existing backup</span></span>

## <span data-ttu-id="f4c17-109">예제</span><span class="sxs-lookup"><span data-stu-id="f4c17-109">EXAMPLES</span></span>

### <span data-ttu-id="f4c17-110">예제 1: GeoReplica Restore를 사용하여 MySql 서버 복원</span><span class="sxs-lookup"><span data-stu-id="f4c17-110">Example 1: Restore MySql server using GeoReplica Restore</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test-replica | Restore-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -UseGeoRestore 

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-11 eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="f4c17-111">이 cmdlet은 GeoReplica Restore를 사용하여 MySql 서버를 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-111">This cmdlet restores MySql server using GeoReplica Restore.</span></span>

### <span data-ttu-id="f4c17-112">예제 2: PointInTime 복원을 사용하여 MySql 서버 복원</span><span class="sxs-lookup"><span data-stu-id="f4c17-112">Example 2: Restore MySql server using PointInTime Restore</span></span>
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Restore-AzMySqlServer -Name mysql-test-restore -ResourceGroupName PowershellMySqlTest -RestorePointInTime $restorePointInTime -UsePointInTimeRestore

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-restore eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="f4c17-113">이러한 cmdlet은 PointInTime 복원을 사용하여 MySql 서버를 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-113">These cmdlets restore MySql server using PointInTime Restore.</span></span>

## <span data-ttu-id="f4c17-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f4c17-114">PARAMETERS</span></span>

### <span data-ttu-id="f4c17-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4c17-115">-AsJob</span></span>
<span data-ttu-id="f4c17-116">명령을 작업으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="f4c17-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4c17-117">-DefaultProfile</span></span>
<span data-ttu-id="f4c17-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4c17-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4c17-119">-InputObject</span></span>
<span data-ttu-id="f4c17-120">복원할 원본 서버 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-120">The source server object to restore from.</span></span>
<span data-ttu-id="f4c17-121">생성을 위해 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="f4c17-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4c17-122">-Location</span><span class="sxs-lookup"><span data-stu-id="f4c17-122">-Location</span></span>
<span data-ttu-id="f4c17-123">리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-123">The location the resource resides in.</span></span>

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

### <span data-ttu-id="f4c17-124">-Name</span><span class="sxs-lookup"><span data-stu-id="f4c17-124">-Name</span></span>
<span data-ttu-id="f4c17-125">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-125">The name of the server.</span></span>

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

### <span data-ttu-id="f4c17-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f4c17-126">-NoWait</span></span>
<span data-ttu-id="f4c17-127">명령을 비동기적으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-127">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="f4c17-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4c17-128">-ResourceGroupName</span></span>
<span data-ttu-id="f4c17-129">리소스를 포함하는 리소스 그룹의 이름, Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-129">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="f4c17-130">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="f4c17-130">-RestorePointInTime</span></span>
<span data-ttu-id="f4c17-131">리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-131">The location the resource resides in.</span></span>

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

### <span data-ttu-id="f4c17-132">-Sku</span><span class="sxs-lookup"><span data-stu-id="f4c17-132">-Sku</span></span>
<span data-ttu-id="f4c17-133">sku의 이름은 일반적으로 계층 + 패밀리 + 코어(예: B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="f4c17-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="f4c17-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f4c17-134">-SubscriptionId</span></span>
<span data-ttu-id="f4c17-135">Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-135">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="f4c17-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="f4c17-136">-Tag</span></span>
<span data-ttu-id="f4c17-137">키-값 쌍의 형태로 애플리케이션별 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="f4c17-138">-UseGeoRestore</span><span class="sxs-lookup"><span data-stu-id="f4c17-138">-UseGeoRestore</span></span>
<span data-ttu-id="f4c17-139">지역 모드를 사용하여 복원</span><span class="sxs-lookup"><span data-stu-id="f4c17-139">Use Geo mode to restore</span></span>

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

### <span data-ttu-id="f4c17-140">-UsePointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="f4c17-140">-UsePointInTimeRestore</span></span>
<span data-ttu-id="f4c17-141">PointInTime 모드를 사용하여 복원</span><span class="sxs-lookup"><span data-stu-id="f4c17-141">Use PointInTime mode to restore</span></span>

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

### <span data-ttu-id="f4c17-142">-확인</span><span class="sxs-lookup"><span data-stu-id="f4c17-142">-Confirm</span></span>
<span data-ttu-id="f4c17-143">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4c17-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4c17-144">-WhatIf</span></span>
<span data-ttu-id="f4c17-145">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4c17-146">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4c17-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4c17-147">CommonParameters</span></span>
<span data-ttu-id="f4c17-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4c17-149">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4c17-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4c17-150">입력</span><span class="sxs-lookup"><span data-stu-id="f4c17-150">INPUTS</span></span>

### <span data-ttu-id="f4c17-151">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="f4c17-151">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="f4c17-152">출력</span><span class="sxs-lookup"><span data-stu-id="f4c17-152">OUTPUTS</span></span>

### <span data-ttu-id="f4c17-153">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="f4c17-153">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="f4c17-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f4c17-154">NOTES</span></span>

<span data-ttu-id="f4c17-155">별칭</span><span class="sxs-lookup"><span data-stu-id="f4c17-155">ALIASES</span></span>

<span data-ttu-id="f4c17-156">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="f4c17-156">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f4c17-157">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-157">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f4c17-158">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f4c17-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f4c17-159">INPUTOBJECT : 복원할 원본 <IServer> 서버 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-159">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="f4c17-160">`Location <String>`: 리소스가 있는 지리적 위치</span><span class="sxs-lookup"><span data-stu-id="f4c17-160">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="f4c17-161">`[Tag <ITrackedResourceTags>]`: 리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-161">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="f4c17-162">`[(Any) <String>]`: 이 개체에 속성을 추가할 수 있는 경우를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-162">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="f4c17-163">`[AdministratorLogin <String>]`: 서버의 관리자의 로그인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-163">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="f4c17-164">서버를 만들 때만 지정할 수 있습니다(및 생성에 필요합니다).</span><span class="sxs-lookup"><span data-stu-id="f4c17-164">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="f4c17-165">`[EarliestRestoreDate <DateTime?>]`: 초기 복원 지점 만들기 시간(ISO8601 형식)</span><span class="sxs-lookup"><span data-stu-id="f4c17-165">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="f4c17-166">`[FullyQualifiedDomainName <String>]`: 서버의 완전히 자격을 갖춘 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-166">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="f4c17-167">`[IdentityType <IdentityType?>]`: ID 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-167">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="f4c17-168">리소스에 대해 Azure Active Directory 주체를 자동으로 만들고 할당하기 위해 이를 'SystemAssigned'로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-168">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="f4c17-169">`[InfrastructureEncryption <InfrastructureEncryption?>]`: 서버가 인프라 암호화를 사용하도록 설정하는지 여부를 보여주는 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-169">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="f4c17-170">`[MasterServerId <String>]`: 복제본 서버의 마스터 서버 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-170">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="f4c17-171">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: 서버에 최소 Tls 버전을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-171">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="f4c17-172">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: 이 서버에 대해 공용 네트워크 액세스가 허용되는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-172">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="f4c17-173">값은 선택 사항이지만 전달된 경우 '사용' 또는 '사용 안 되어야 합니다'</span><span class="sxs-lookup"><span data-stu-id="f4c17-173">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="f4c17-174">`[ReplicaCapacity <Int32?>]`: 마스터 서버가 사용할 수 있는 복제본의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-174">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="f4c17-175">`[ReplicationRole <String>]`: 서버의 복제 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-175">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="f4c17-176">`[SkuCapacity <Int32?>]`: 서버의 계산 단위를 나타내는 확장/확장 용량입니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-176">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="f4c17-177">`[SkuFamily <String>]`: 하드웨어의 패밀리입니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-177">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="f4c17-178">`[SkuName <String>]`: sku의 이름, 일반적으로 계층 + 패밀리 + 코어(예: B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="f4c17-178">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="f4c17-179">`[SkuSize <String>]`: 리소스로 적절하게 해석할 크기 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-179">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="f4c17-180">`[SkuTier <SkuTier?>]`: 특정 SKU의 계층(예: Basic)</span><span class="sxs-lookup"><span data-stu-id="f4c17-180">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="f4c17-181">`[SslEnforcement <SslEnforcementEnum?>]`: 서버에 연결할 때 ssl 적용을 사용하도록 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-181">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="f4c17-182">`[StorageProfileBackupRetentionDay <Int32?>]`: 서버에 대한 백업 보존일입니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="f4c17-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: 서버 백업에 대해 지역 중복을 사용하도록 설정하거나 사용 안 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="f4c17-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: 저장소 자동 증가를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="f4c17-185">`[StorageProfileStorageMb <Int32?>]`: 서버에 대해 허용되는 최대 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-185">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="f4c17-186">`[UserVisibleState <ServerState?>]`: 사용자에게 표시되는 서버의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-186">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="f4c17-187">`[Version <ServerVersion?>]`: 서버 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="f4c17-187">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="f4c17-188">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f4c17-188">RELATED LINKS</span></span>

