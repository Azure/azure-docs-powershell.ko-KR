---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/new-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
ms.openlocfilehash: 3e3e63bee89eb9ae89cb647b81ea7d0da792ae3e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970592"
---
# <span data-ttu-id="2607b-101">New-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="2607b-101">New-AzMariaDbReplica</span></span>

## <span data-ttu-id="2607b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2607b-102">SYNOPSIS</span></span>
<span data-ttu-id="2607b-103">MariaDB 서버의 복제본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-103">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="2607b-104">구문</span><span class="sxs-lookup"><span data-stu-id="2607b-104">SYNTAX</span></span>

### <span data-ttu-id="2607b-105">ServerName(기본값)</span><span class="sxs-lookup"><span data-stu-id="2607b-105">ServerName (Default)</span></span>
```
New-AzMariaDbReplica -MasterName <String> -ReplicaName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2607b-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="2607b-106">ServerObject</span></span>
```
New-AzMariaDbReplica -Master <IServer> -ReplicaName <String> [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="2607b-107">설명</span><span class="sxs-lookup"><span data-stu-id="2607b-107">DESCRIPTION</span></span>
<span data-ttu-id="2607b-108">MariaDB 서버의 복제본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-108">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="2607b-109">예제</span><span class="sxs-lookup"><span data-stu-id="2607b-109">EXAMPLES</span></span>

### <span data-ttu-id="2607b-110">예제 1: MariaDB에 대한 복제본 DB 만들기</span><span class="sxs-lookup"><span data-stu-id="2607b-110">Example 1: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbReplica -MasterName mariadb-test-9pebvn -ReplicaName mariadb-test-9pebvn-rep01 -ResourceGroupName mariadb-test-qu5ov0

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep01 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="2607b-111">이 명령은 MariaDB에 대한 복제본 DB를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-111">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="2607b-112">예제 2: MariaDB에 대한 복제본 DB 만들기</span><span class="sxs-lookup"><span data-stu-id="2607b-112">Example 2: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | New-AzMariaDbReplica -ReplicaName mariadb-test-9pebvn-rep02

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep02 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="2607b-113">이 명령은 MariaDB에 대한 복제본 DB를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-113">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="2607b-114">예제 3: MariaDB에 대한 복제본 DB 만들기</span><span class="sxs-lookup"><span data-stu-id="2607b-114">Example 3: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> $mariaDb = Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 
PS C:\> New-AzMariaDbReplica -Master $mariaDb -ReplicaName mariadb-test-9pebvn-rep03

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep03 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="2607b-115">매개 변수 inputobject가 있는 이 명령은 MariaDB에 대한 매개 변수 입력이 있는 복제본 DB를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-115">This command with parameter inputobject creates a replica db with parameter inputobject for a MariaDB.</span></span>

## <span data-ttu-id="2607b-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2607b-116">PARAMETERS</span></span>

### <span data-ttu-id="2607b-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2607b-117">-AsJob</span></span>
<span data-ttu-id="2607b-118">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-118">Run the command as a job</span></span>

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

### <span data-ttu-id="2607b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2607b-119">-DefaultProfile</span></span>
<span data-ttu-id="2607b-120">region DefaultParameters Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2607b-121">-Location</span><span class="sxs-lookup"><span data-stu-id="2607b-121">-Location</span></span>
<span data-ttu-id="2607b-122">리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-122">The location the resource resides in.</span></span>

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

### <span data-ttu-id="2607b-123">-Master</span><span class="sxs-lookup"><span data-stu-id="2607b-123">-Master</span></span>
<span data-ttu-id="2607b-124">복원할 원본 서버 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-124">The source server object to restore from.</span></span>
<span data-ttu-id="2607b-125">생성을 위해 MASTER 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="2607b-125">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: ServerObject
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2607b-126">-MasterName</span><span class="sxs-lookup"><span data-stu-id="2607b-126">-MasterName</span></span>
<span data-ttu-id="2607b-127">MariaDB 서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-127">MariaDB server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2607b-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2607b-128">-NoWait</span></span>
<span data-ttu-id="2607b-129">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="2607b-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2607b-130">-ReplicaName</span><span class="sxs-lookup"><span data-stu-id="2607b-130">-ReplicaName</span></span>
<span data-ttu-id="2607b-131">복제본 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-131">Replica name.</span></span>

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

### <span data-ttu-id="2607b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2607b-132">-ResourceGroupName</span></span>
<span data-ttu-id="2607b-133">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-133">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2607b-134">-Sku</span><span class="sxs-lookup"><span data-stu-id="2607b-134">-Sku</span></span>
<span data-ttu-id="2607b-135">sku의 이름은 일반적으로 계층 + 패밀리 + 코어(예: B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="2607b-135">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="2607b-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2607b-136">-SubscriptionId</span></span>
<span data-ttu-id="2607b-137">구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-137">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2607b-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="2607b-138">-Tag</span></span>
<span data-ttu-id="2607b-139">키-값 쌍의 형태로 애플리케이션별 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-139">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="2607b-140">-확인</span><span class="sxs-lookup"><span data-stu-id="2607b-140">-Confirm</span></span>
<span data-ttu-id="2607b-141">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2607b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2607b-142">-WhatIf</span></span>
<span data-ttu-id="2607b-143">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2607b-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2607b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2607b-145">CommonParameters</span></span>
<span data-ttu-id="2607b-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2607b-147">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2607b-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2607b-148">입력</span><span class="sxs-lookup"><span data-stu-id="2607b-148">INPUTS</span></span>

### <span data-ttu-id="2607b-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="2607b-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="2607b-150">출력</span><span class="sxs-lookup"><span data-stu-id="2607b-150">OUTPUTS</span></span>

### <span data-ttu-id="2607b-151">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="2607b-151">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="2607b-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2607b-152">NOTES</span></span>

<span data-ttu-id="2607b-153">별칭</span><span class="sxs-lookup"><span data-stu-id="2607b-153">ALIASES</span></span>

<span data-ttu-id="2607b-154">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="2607b-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2607b-155">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2607b-156">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2607b-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2607b-157">MASTER : 복원할 원본 <IServer> 서버 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-157">MASTER <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="2607b-158">`Location <String>`: 리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-158">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="2607b-159">`[Tag <ITrackedResourceTags>]`: 키-값 쌍의 형태로 애플리케이션별 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-159">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="2607b-160">`[(Any) <String>]`: 이 개체에 속성을 추가할 수 있는 경우를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="2607b-161">`[AdministratorLogin <String>]`: 서버의 관리자의 로그인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-161">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="2607b-162">서버를 만들 때만 지정할 수 있습니다(및 생성에 필요합니다).</span><span class="sxs-lookup"><span data-stu-id="2607b-162">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="2607b-163">`[EarliestRestoreDate <DateTime?>]`: 초기 복원 지점 만들기 시간(ISO8601 형식)</span><span class="sxs-lookup"><span data-stu-id="2607b-163">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="2607b-164">`[FullyQualifiedDomainName <String>]`: 서버의 완전히 자격을 갖춘 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-164">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="2607b-165">`[IdentityType <IdentityType?>]`: ID 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-165">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="2607b-166">리소스에 대해 Azure Active Directory 주체를 자동으로 만들고 할당하기 위해 이를 'SystemAssigned'로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-166">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="2607b-167">`[MasterServerId <String>]`: 복제본 서버의 마스터 서버 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-167">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="2607b-168">`[ReplicaCapacity <Int32?>]`: 마스터 서버가 사용할 수 있는 복제본의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-168">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="2607b-169">`[ReplicationRole <String>]`: 서버의 복제 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-169">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="2607b-170">`[SkuCapacity <Int32?>]`: 서버의 계산 단위를 나타내는 확장/확장 용량입니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-170">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="2607b-171">`[SkuFamily <String>]`: 하드웨어의 패밀리입니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-171">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="2607b-172">`[SkuName <String>]`: sku의 이름, 일반적으로 계층 + 패밀리 + 코어(예: B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="2607b-172">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="2607b-173">`[SkuSize <String>]`: 리소스로 적절하게 해석할 크기 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-173">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="2607b-174">`[SkuTier <SkuTier?>]`: 특정 SKU의 계층(예: Basic)</span><span class="sxs-lookup"><span data-stu-id="2607b-174">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="2607b-175">`[SslEnforcement <SslEnforcementEnum?>]`: 서버에 연결할 때 ssl 적용을 사용하도록 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-175">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="2607b-176">`[StorageProfileBackupRetentionDay <Int32?>]`: 서버에 대한 백업 보존일입니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-176">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="2607b-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: 서버 백업에 대해 지역 중복을 사용하도록 설정하거나 사용 안 합니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="2607b-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: 저장소 자동 증가를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="2607b-179">`[StorageProfileStorageMb <Int32?>]`: 서버에 대해 허용되는 최대 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-179">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="2607b-180">`[UserVisibleState <ServerState?>]`: 사용자에게 표시되는 서버의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-180">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="2607b-181">`[Version <ServerVersion?>]`: 서버 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="2607b-181">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="2607b-182">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2607b-182">RELATED LINKS</span></span>

