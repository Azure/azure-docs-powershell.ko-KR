---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
ms.openlocfilehash: 0ce25af607d2460abf2ec4585dacc124a1f2e65c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218648"
---
# <span data-ttu-id="3e89a-101">New-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="3e89a-101">New-AzMariaDbReplica</span></span>

## <span data-ttu-id="3e89a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e89a-102">SYNOPSIS</span></span>
<span data-ttu-id="3e89a-103">이 (가) a 2 i의 복제를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-103">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="3e89a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3e89a-104">SYNTAX</span></span>

### <span data-ttu-id="3e89a-105">ServerName (기본값)</span><span class="sxs-lookup"><span data-stu-id="3e89a-105">ServerName (Default)</span></span>
```
New-AzMariaDbReplica -MasterName <String> -ReplicaName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3e89a-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="3e89a-106">ServerObject</span></span>
```
New-AzMariaDbReplica -Master <IServer> -ReplicaName <String> [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="3e89a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3e89a-107">DESCRIPTION</span></span>
<span data-ttu-id="3e89a-108">이 (가) a 2 i의 복제를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-108">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="3e89a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="3e89a-109">EXAMPLES</span></span>

### <span data-ttu-id="3e89a-110">예제 1: a 2에 대 한 복제 db 만들기 Iadb</span><span class="sxs-lookup"><span data-stu-id="3e89a-110">Example 1: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbReplica -MasterName mariadb-test-9pebvn -ReplicaName mariadb-test-9pebvn-rep01 -ResourceGroupName mariadb-test-qu5ov0

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep01 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="3e89a-111">이 명령은 a 2 i에 대 한 복제 db를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-111">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="3e89a-112">예제 2: a 2에 대 한 복제 db 만들기 Iadb</span><span class="sxs-lookup"><span data-stu-id="3e89a-112">Example 2: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | New-AzMariaDbReplica -ReplicaName mariadb-test-9pebvn-rep02

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep02 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="3e89a-113">이 명령은 a 2 i에 대 한 복제 db를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-113">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="3e89a-114">예제 3: a 4에 대 한 복제 db 만들기 (Adb)</span><span class="sxs-lookup"><span data-stu-id="3e89a-114">Example 3: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> $mariaDb = Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 
PS C:\> New-AzMariaDbReplica -Master $mariaDb -ReplicaName mariadb-test-9pebvn-rep03

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep03 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="3e89a-115">매개 변수 inputobject를 사용 하는이 명령은 e 2 Iadb에 대 한 매개 변수 inputobject를 사용 하 여 복제본 db를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-115">This command with parameter inputobject creates a replica db with parameter inputobject for a MariaDB.</span></span>

## <span data-ttu-id="3e89a-116">변수</span><span class="sxs-lookup"><span data-stu-id="3e89a-116">PARAMETERS</span></span>

### <span data-ttu-id="3e89a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e89a-117">-AsJob</span></span>
<span data-ttu-id="3e89a-118">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="3e89a-118">Run the command as a job</span></span>

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

### <span data-ttu-id="3e89a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e89a-119">-DefaultProfile</span></span>
<span data-ttu-id="3e89a-120">region DefaultParameters Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e89a-121">-위치</span><span class="sxs-lookup"><span data-stu-id="3e89a-121">-Location</span></span>
<span data-ttu-id="3e89a-122">리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-122">The location the resource resides in.</span></span>

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

### <span data-ttu-id="3e89a-123">-마스터</span><span class="sxs-lookup"><span data-stu-id="3e89a-123">-Master</span></span>
<span data-ttu-id="3e89a-124">복원할 원본 서버 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-124">The source server object to restore from.</span></span>
<span data-ttu-id="3e89a-125">생성 하려면 마스터 속성에 대 한 메모 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-125">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

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

### <span data-ttu-id="3e89a-126">-MasterName</span><span class="sxs-lookup"><span data-stu-id="3e89a-126">-MasterName</span></span>
<span data-ttu-id="3e89a-127">E 2 Iadb 서버 이름.</span><span class="sxs-lookup"><span data-stu-id="3e89a-127">MariaDB server name.</span></span>

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

### <span data-ttu-id="3e89a-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3e89a-128">-NoWait</span></span>
<span data-ttu-id="3e89a-129">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="3e89a-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3e89a-130">-ReplicaName</span><span class="sxs-lookup"><span data-stu-id="3e89a-130">-ReplicaName</span></span>
<span data-ttu-id="3e89a-131">복제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-131">Replica name.</span></span>

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

### <span data-ttu-id="3e89a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e89a-132">-ResourceGroupName</span></span>
<span data-ttu-id="3e89a-133">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-133">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="3e89a-134">-Sku</span><span class="sxs-lookup"><span data-stu-id="3e89a-134">-Sku</span></span>
<span data-ttu-id="3e89a-135">Sku (일반적으로 계층 + 패밀리 + 코어)의 이름 (예: B_Gen4_1 GP_Gen5_8)입니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-135">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="3e89a-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3e89a-136">-SubscriptionId</span></span>
<span data-ttu-id="3e89a-137">구독 ID는 모든 서비스 호출에 대 한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-137">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3e89a-138">태그</span><span class="sxs-lookup"><span data-stu-id="3e89a-138">-Tag</span></span>
<span data-ttu-id="3e89a-139">키-값 쌍의 형식으로 된 응용 프로그램 관련 메타 데이터</span><span class="sxs-lookup"><span data-stu-id="3e89a-139">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="3e89a-140">-확인</span><span class="sxs-lookup"><span data-stu-id="3e89a-140">-Confirm</span></span>
<span data-ttu-id="3e89a-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e89a-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e89a-142">-WhatIf</span></span>
<span data-ttu-id="3e89a-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e89a-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e89a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e89a-145">CommonParameters</span></span>
<span data-ttu-id="3e89a-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e89a-147">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3e89a-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e89a-148">입력</span><span class="sxs-lookup"><span data-stu-id="3e89a-148">INPUTS</span></span>

### <span data-ttu-id="3e89a-149">Api20180601Preview Iadb. i r i. IServer</span><span class="sxs-lookup"><span data-stu-id="3e89a-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="3e89a-150">출력</span><span class="sxs-lookup"><span data-stu-id="3e89a-150">OUTPUTS</span></span>

### <span data-ttu-id="3e89a-151">Api20180601Preview Iadb. i r i. IServer</span><span class="sxs-lookup"><span data-stu-id="3e89a-151">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="3e89a-152">상속자</span><span class="sxs-lookup"><span data-stu-id="3e89a-152">NOTES</span></span>

<span data-ttu-id="3e89a-153">별칭과</span><span class="sxs-lookup"><span data-stu-id="3e89a-153">ALIASES</span></span>

<span data-ttu-id="3e89a-154">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="3e89a-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3e89a-155">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3e89a-156">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="3e89a-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3e89a-157">MASTER <IServer> : 복원할 원본 서버 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-157">MASTER <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="3e89a-158">`Location <String>`: 리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-158">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="3e89a-159">`[Tag <ITrackedResourceTags>]`: 키-값 쌍의 형식으로 된 응용 프로그램 관련 메타 데이터</span><span class="sxs-lookup"><span data-stu-id="3e89a-159">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="3e89a-160">`[(Any) <String>]`:이 개체에 모든 속성이 추가 될 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="3e89a-161">`[AdministratorLogin <String>]`: 서버의 관리자 로그인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-161">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="3e89a-162">서버를 만드는 경우에만 지정할 수 있습니다 (만들기에 필요 함).</span><span class="sxs-lookup"><span data-stu-id="3e89a-162">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="3e89a-163">`[EarliestRestoreDate <DateTime?>]`: 초기 복원 시점 생성 시간 (ISO8601 형식)</span><span class="sxs-lookup"><span data-stu-id="3e89a-163">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="3e89a-164">`[FullyQualifiedDomainName <String>]`: 서버의 정규화 된 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-164">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="3e89a-165">`[IdentityType <IdentityType?>]`: Id 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-165">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="3e89a-166">해당 리소스에 대 한 Azure Active Directory 보안 주체를 자동으로 만들고 할당 하려면이를 ' SystemAssigned '로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-166">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="3e89a-167">`[MasterServerId <String>]`: 복제본 서버의 마스터 서버 id입니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-167">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="3e89a-168">`[ReplicaCapacity <Int32?>]`: 마스터 서버에 포함할 수 있는 최대 복제 데이터베이스 수입니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-168">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="3e89a-169">`[ReplicationRole <String>]`: 서버의 복제 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-169">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="3e89a-170">`[SkuCapacity <Int32?>]`: 서버의 계산 단위를 나타내는 스케일 업/out 용량입니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-170">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="3e89a-171">`[SkuFamily <String>]`: 하드웨어의 패밀리입니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-171">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="3e89a-172">`[SkuName <String>]`: Sku의 이름 (일반적으로 계층 + 패밀리 + 코어) (예: B_Gen4_1 GP_Gen5_8)입니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-172">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="3e89a-173">`[SkuSize <String>]`: 리소스에 따라 적절 하 게 해석 되는 크기 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-173">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="3e89a-174">`[SkuTier <SkuTier?>]`: 특정 SKU (예: 기본)의 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-174">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="3e89a-175">`[SslEnforcement <SslEnforcementEnum?>]`: 서버에 연결할 때 ssl 적용 여부를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-175">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="3e89a-176">`[StorageProfileBackupRetentionDay <Int32?>]`: 서버에 대 한 백업 보존 일입니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-176">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="3e89a-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: 서버 백업에 대해 지리적 중복을 사용 하거나 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="3e89a-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: 저장소 자동 증가를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="3e89a-179">`[StorageProfileStorageMb <Int32?>]`: 서버에 허용 된 최대 저장소.</span><span class="sxs-lookup"><span data-stu-id="3e89a-179">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="3e89a-180">`[UserVisibleState <ServerState?>]`: 사용자에 게 표시 되는 서버의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="3e89a-180">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="3e89a-181">`[Version <ServerVersion?>]`: 서버 버전.</span><span class="sxs-lookup"><span data-stu-id="3e89a-181">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="3e89a-182">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3e89a-182">RELATED LINKS</span></span>

