---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/restore-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
ms.openlocfilehash: 95988d83cbb4c3dcf0b5da890bf38f8c40eb4dfa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207176"
---
# <span data-ttu-id="dc56f-101">Restore-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="dc56f-101">Restore-AzMariaDbServer</span></span>

## <span data-ttu-id="dc56f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc56f-102">SYNOPSIS</span></span>
<span data-ttu-id="dc56f-103">기존 MariaDB에서 MariaDB를 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-103">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="dc56f-104">구문</span><span class="sxs-lookup"><span data-stu-id="dc56f-104">SYNTAX</span></span>

```
Restore-AzMariaDbServer -Name <String> -RestorePointInTime <DateTime> [-InputObject <IServer>]
 [-ResourceGroupName <String>] [-ServerName <String>] [-SubscriptionId <String>] [-Location <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dc56f-105">설명</span><span class="sxs-lookup"><span data-stu-id="dc56f-105">DESCRIPTION</span></span>
<span data-ttu-id="dc56f-106">기존 MariaDB에서 MariaDB를 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-106">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="dc56f-107">예제</span><span class="sxs-lookup"><span data-stu-id="dc56f-107">EXAMPLES</span></span>

### <span data-ttu-id="dc56f-108">예제 1: 서버 이름으로 PointInTime MariaDB 복원</span><span class="sxs-lookup"><span data-stu-id="dc56f-108">Example 1: Restore a PointInTime MariaDB by server name.</span></span>
```powershell
PS C:\> Restore-AzMariaDbServer -Name restore-db01 -ServerName mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db01 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="dc56f-109">이 명령은 서버 이름으로 PointInTime MariaDB를 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-109">This command restore a PointInTime MariaDB by server name.</span></span>

### <span data-ttu-id="dc56f-110">예제 2: 서버 개체로 PointInTime MariaDB 복원</span><span class="sxs-lookup"><span data-stu-id="dc56f-110">Example 2: Restore a PointInTime MariaDB by server object</span></span>
```powershell
PS C:\> $db = Get-AzMariaDbServer -Name mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z
PS C:\>Restore-AzMariaDbServer -Name restore-db02 -InputObject $db -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db02 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="dc56f-111">이 명령은 서버 개체에 의해 PointInTime MariaDB를 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-111">This command restore a PointInTime MariaDB by server object.</span></span>

## <span data-ttu-id="dc56f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc56f-112">PARAMETERS</span></span>

### <span data-ttu-id="dc56f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dc56f-113">-AsJob</span></span>
<span data-ttu-id="dc56f-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="dc56f-114">Run the command as a job</span></span>

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

### <span data-ttu-id="dc56f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc56f-115">-DefaultProfile</span></span>
<span data-ttu-id="dc56f-116">region DefaultParameters Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-116">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc56f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc56f-117">-InputObject</span></span>
<span data-ttu-id="dc56f-118">복원할 원본 서버 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-118">The source server object to restore from.</span></span>
<span data-ttu-id="dc56f-119">생성을 위해 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="dc56f-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc56f-120">-Location</span><span class="sxs-lookup"><span data-stu-id="dc56f-120">-Location</span></span>
<span data-ttu-id="dc56f-121">리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-121">The location the resource resides in.</span></span>

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

### <span data-ttu-id="dc56f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="dc56f-122">-Name</span></span>
<span data-ttu-id="dc56f-123">복원할 서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-123">The dest server name to restore from.</span></span>

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

### <span data-ttu-id="dc56f-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="dc56f-124">-NoWait</span></span>
<span data-ttu-id="dc56f-125">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="dc56f-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dc56f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc56f-126">-ResourceGroupName</span></span>
<span data-ttu-id="dc56f-127">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="dc56f-128">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="dc56f-129">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="dc56f-129">-RestorePointInTime</span></span>
<span data-ttu-id="dc56f-130">region PointInTimeRestore 리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-130">region PointInTimeRestore The location the resource resides in.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc56f-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="dc56f-131">-ServerName</span></span>
<span data-ttu-id="dc56f-132">복원할 원본 서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-132">The source server name to restore from.</span></span>

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

### <span data-ttu-id="dc56f-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dc56f-133">-SubscriptionId</span></span>
<span data-ttu-id="dc56f-134">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-134">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="dc56f-135">구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-135">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="dc56f-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="dc56f-136">-Tag</span></span>
<span data-ttu-id="dc56f-137">키-값 쌍의 형태로 애플리케이션별 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="dc56f-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc56f-138">-Confirm</span></span>
<span data-ttu-id="dc56f-139">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc56f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc56f-140">-WhatIf</span></span>
<span data-ttu-id="dc56f-141">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="dc56f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc56f-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc56f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc56f-143">CommonParameters</span></span>
<span data-ttu-id="dc56f-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc56f-145">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dc56f-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc56f-146">입력</span><span class="sxs-lookup"><span data-stu-id="dc56f-146">INPUTS</span></span>

### <span data-ttu-id="dc56f-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="dc56f-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="dc56f-148">출력</span><span class="sxs-lookup"><span data-stu-id="dc56f-148">OUTPUTS</span></span>

### <span data-ttu-id="dc56f-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="dc56f-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="dc56f-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dc56f-150">NOTES</span></span>

<span data-ttu-id="dc56f-151">별칭</span><span class="sxs-lookup"><span data-stu-id="dc56f-151">ALIASES</span></span>

<span data-ttu-id="dc56f-152">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="dc56f-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dc56f-153">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dc56f-154">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dc56f-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dc56f-155">INPUTOBJECT: 복원할 원본 <IServer> 서버 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-155">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="dc56f-156">`Location <String>`: 리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-156">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="dc56f-157">`[Tag <ITrackedResourceTags>]`: 키-값 쌍의 형태로 애플리케이션별 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-157">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="dc56f-158">`[(Any) <String>]`: 이 개체에 추가할 수 있는 속성을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-158">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="dc56f-159">`[AdministratorLogin <String>]`: 서버의 관리자 로그인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-159">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="dc56f-160">서버를 만들 때만 지정할 수 있습니다(생성에 필요).</span><span class="sxs-lookup"><span data-stu-id="dc56f-160">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="dc56f-161">`[EarliestRestoreDate <DateTime?>]`: 가장 빠른 복원 지점 생성 시간(ISO8601 형식)</span><span class="sxs-lookup"><span data-stu-id="dc56f-161">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="dc56f-162">`[FullyQualifiedDomainName <String>]`: 서버의 정식 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-162">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="dc56f-163">`[IdentityType <IdentityType?>]`: ID 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-163">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="dc56f-164">리소스에 대한 Azure Active Directory 주체를 자동으로 만들고 할당하기 위해 이를 'SystemAssigned'로 설정하세요.</span><span class="sxs-lookup"><span data-stu-id="dc56f-164">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="dc56f-165">`[MasterServerId <String>]`: 복제본 서버의 마스터 서버 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-165">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="dc56f-166">`[ReplicaCapacity <Int32?>]`: 마스터 서버가 사용할 수 있는 최대 복제본 수입니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-166">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="dc56f-167">`[ReplicationRole <String>]`: 서버의 복제 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-167">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="dc56f-168">`[SkuCapacity <Int32?>]`: 서버의 컴퓨팅 단위를 나타내는 확장/확장 용량입니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-168">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="dc56f-169">`[SkuFamily <String>]`: 하드웨어의 패밀리입니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-169">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="dc56f-170">`[SkuName <String>]`: SKU의 이름(일반적으로 계층 + 패밀리 + 코어)입니다(예: B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="dc56f-170">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="dc56f-171">`[SkuSize <String>]`: 리소스에서 적절하게 해석할 크기 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-171">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="dc56f-172">`[SkuTier <SkuTier?>]`: 특정 SKU의 계층(예: 기본)</span><span class="sxs-lookup"><span data-stu-id="dc56f-172">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="dc56f-173">`[SslEnforcement <SslEnforcementEnum?>]`: 서버에 연결할 때 ssl 적용을 사용하도록 설정하거나 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-173">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="dc56f-174">`[StorageProfileBackupRetentionDay <Int32?>]`: 서버에 대한 백업 보존 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-174">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="dc56f-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: 서버 백업에 지역 중복 사용 또는 사용 안 하도록 설정</span><span class="sxs-lookup"><span data-stu-id="dc56f-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="dc56f-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: 저장소 자동 증가를 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="dc56f-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="dc56f-177">`[StorageProfileStorageMb <Int32?>]`: 서버에 허용되는 최대 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-177">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="dc56f-178">`[UserVisibleState <ServerState?>]`: 사용자에게 표시되는 서버의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-178">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="dc56f-179">`[Version <ServerVersion?>]`: 서버 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="dc56f-179">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="dc56f-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dc56f-180">RELATED LINKS</span></span>

