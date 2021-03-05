---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/restore-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
ms.openlocfilehash: 092e109de5fd38fcad924886f55d918a91e12aed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003899"
---
# <span data-ttu-id="4ad84-101">Restore-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="4ad84-101">Restore-AzMariaDbServer</span></span>

## <span data-ttu-id="4ad84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ad84-102">SYNOPSIS</span></span>
<span data-ttu-id="4ad84-103">기존 MariaDB에서 MariaDB를 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-103">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="4ad84-104">구문</span><span class="sxs-lookup"><span data-stu-id="4ad84-104">SYNTAX</span></span>

```
Restore-AzMariaDbServer -Name <String> -RestorePointInTime <DateTime> [-InputObject <IServer>]
 [-ResourceGroupName <String>] [-ServerName <String>] [-SubscriptionId <String>] [-Location <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4ad84-105">설명</span><span class="sxs-lookup"><span data-stu-id="4ad84-105">DESCRIPTION</span></span>
<span data-ttu-id="4ad84-106">기존 MariaDB에서 MariaDB를 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-106">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="4ad84-107">예제</span><span class="sxs-lookup"><span data-stu-id="4ad84-107">EXAMPLES</span></span>

### <span data-ttu-id="4ad84-108">예제 1: 서버 이름으로 PointInTime MariaDB를 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-108">Example 1: Restore a PointInTime MariaDB by server name.</span></span>
```powershell
PS C:\> Restore-AzMariaDbServer -Name restore-db01 -ServerName mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db01 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="4ad84-109">이 명령은 서버 이름으로 PointInTime MariaDB를 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-109">This command restore a PointInTime MariaDB by server name.</span></span>

### <span data-ttu-id="4ad84-110">예제 2: 서버 개체에 따라 PointInTime MariaDB 복원</span><span class="sxs-lookup"><span data-stu-id="4ad84-110">Example 2: Restore a PointInTime MariaDB by server object</span></span>
```powershell
PS C:\> $db = Get-AzMariaDbServer -Name mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z
PS C:\>Restore-AzMariaDbServer -Name restore-db02 -InputObject $db -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db02 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="4ad84-111">이 명령은 서버 개체에 의해 PointInTime MariaDB를 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-111">This command restore a PointInTime MariaDB by server object.</span></span>

## <span data-ttu-id="4ad84-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4ad84-112">PARAMETERS</span></span>

### <span data-ttu-id="4ad84-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ad84-113">-AsJob</span></span>
<span data-ttu-id="4ad84-114">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-114">Run the command as a job</span></span>

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

### <span data-ttu-id="4ad84-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ad84-115">-DefaultProfile</span></span>
<span data-ttu-id="4ad84-116">region DefaultParameters Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-116">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ad84-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ad84-117">-InputObject</span></span>
<span data-ttu-id="4ad84-118">복원할 원본 서버 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-118">The source server object to restore from.</span></span>
<span data-ttu-id="4ad84-119">생성을 위해 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="4ad84-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4ad84-120">-Location</span><span class="sxs-lookup"><span data-stu-id="4ad84-120">-Location</span></span>
<span data-ttu-id="4ad84-121">리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-121">The location the resource resides in.</span></span>

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

### <span data-ttu-id="4ad84-122">-Name</span><span class="sxs-lookup"><span data-stu-id="4ad84-122">-Name</span></span>
<span data-ttu-id="4ad84-123">복원할 서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-123">The dest server name to restore from.</span></span>

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

### <span data-ttu-id="4ad84-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4ad84-124">-NoWait</span></span>
<span data-ttu-id="4ad84-125">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="4ad84-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4ad84-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ad84-126">-ResourceGroupName</span></span>
<span data-ttu-id="4ad84-127">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="4ad84-128">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="4ad84-129">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="4ad84-129">-RestorePointInTime</span></span>
<span data-ttu-id="4ad84-130">region PointInTimeRestore 리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-130">region PointInTimeRestore The location the resource resides in.</span></span>

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

### <span data-ttu-id="4ad84-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4ad84-131">-ServerName</span></span>
<span data-ttu-id="4ad84-132">복원할 원본 서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-132">The source server name to restore from.</span></span>

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

### <span data-ttu-id="4ad84-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4ad84-133">-SubscriptionId</span></span>
<span data-ttu-id="4ad84-134">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-134">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="4ad84-135">구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-135">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4ad84-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="4ad84-136">-Tag</span></span>
<span data-ttu-id="4ad84-137">키-값 쌍의 형태로 애플리케이션별 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="4ad84-138">-확인</span><span class="sxs-lookup"><span data-stu-id="4ad84-138">-Confirm</span></span>
<span data-ttu-id="4ad84-139">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ad84-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ad84-140">-WhatIf</span></span>
<span data-ttu-id="4ad84-141">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ad84-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ad84-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ad84-143">CommonParameters</span></span>
<span data-ttu-id="4ad84-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ad84-145">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ad84-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ad84-146">입력</span><span class="sxs-lookup"><span data-stu-id="4ad84-146">INPUTS</span></span>

### <span data-ttu-id="4ad84-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="4ad84-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="4ad84-148">출력</span><span class="sxs-lookup"><span data-stu-id="4ad84-148">OUTPUTS</span></span>

### <span data-ttu-id="4ad84-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="4ad84-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="4ad84-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4ad84-150">NOTES</span></span>

<span data-ttu-id="4ad84-151">별칭</span><span class="sxs-lookup"><span data-stu-id="4ad84-151">ALIASES</span></span>

<span data-ttu-id="4ad84-152">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="4ad84-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4ad84-153">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4ad84-154">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4ad84-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4ad84-155">INPUTOBJECT : 복원할 원본 <IServer> 서버 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-155">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="4ad84-156">`Location <String>`: 리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-156">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="4ad84-157">`[Tag <ITrackedResourceTags>]`: 키-값 쌍의 형태로 애플리케이션별 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-157">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="4ad84-158">`[(Any) <String>]`: 이 개체에 속성을 추가할 수 있는 경우를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-158">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="4ad84-159">`[AdministratorLogin <String>]`: 서버의 관리자의 로그인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-159">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="4ad84-160">서버를 만들 때만 지정할 수 있습니다(및 생성에 필요합니다).</span><span class="sxs-lookup"><span data-stu-id="4ad84-160">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="4ad84-161">`[EarliestRestoreDate <DateTime?>]`: 초기 복원 지점 만들기 시간(ISO8601 형식)</span><span class="sxs-lookup"><span data-stu-id="4ad84-161">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="4ad84-162">`[FullyQualifiedDomainName <String>]`: 서버의 완전히 자격을 갖춘 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-162">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="4ad84-163">`[IdentityType <IdentityType?>]`: ID 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-163">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="4ad84-164">리소스에 대해 Azure Active Directory 주체를 자동으로 만들고 할당하기 위해 이를 'SystemAssigned'로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-164">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="4ad84-165">`[MasterServerId <String>]`: 복제본 서버의 마스터 서버 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-165">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="4ad84-166">`[ReplicaCapacity <Int32?>]`: 마스터 서버가 사용할 수 있는 복제본의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-166">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="4ad84-167">`[ReplicationRole <String>]`: 서버의 복제 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-167">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="4ad84-168">`[SkuCapacity <Int32?>]`: 서버의 계산 단위를 나타내는 확장/확장 용량입니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-168">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="4ad84-169">`[SkuFamily <String>]`: 하드웨어의 패밀리입니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-169">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="4ad84-170">`[SkuName <String>]`: sku의 이름, 일반적으로 계층 + 패밀리 + 코어(예: B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="4ad84-170">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="4ad84-171">`[SkuSize <String>]`: 리소스로 적절하게 해석할 크기 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-171">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="4ad84-172">`[SkuTier <SkuTier?>]`: 특정 SKU의 계층(예: Basic)</span><span class="sxs-lookup"><span data-stu-id="4ad84-172">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="4ad84-173">`[SslEnforcement <SslEnforcementEnum?>]`: 서버에 연결할 때 ssl 적용을 사용하도록 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-173">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="4ad84-174">`[StorageProfileBackupRetentionDay <Int32?>]`: 서버에 대한 백업 보존일입니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-174">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="4ad84-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: 서버 백업에 대해 지역 중복을 사용하도록 설정하거나 사용 안 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="4ad84-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: 저장소 자동 증가를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="4ad84-177">`[StorageProfileStorageMb <Int32?>]`: 서버에 대해 허용되는 최대 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-177">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="4ad84-178">`[UserVisibleState <ServerState?>]`: 사용자에게 표시되는 서버의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-178">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="4ad84-179">`[Version <ServerVersion?>]`: 서버 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="4ad84-179">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="4ad84-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4ad84-180">RELATED LINKS</span></span>

