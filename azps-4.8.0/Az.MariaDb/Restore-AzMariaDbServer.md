---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/restore-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
ms.openlocfilehash: 95988d83cbb4c3dcf0b5da890bf38f8c40eb4dfa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056270"
---
# <span data-ttu-id="57451-101">Restore-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="57451-101">Restore-AzMariaDbServer</span></span>

## <span data-ttu-id="57451-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57451-102">SYNOPSIS</span></span>
<span data-ttu-id="57451-103">기존에 있는 a 2 Iadb를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="57451-103">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="57451-104">구문과</span><span class="sxs-lookup"><span data-stu-id="57451-104">SYNTAX</span></span>

```
Restore-AzMariaDbServer -Name <String> -RestorePointInTime <DateTime> [-InputObject <IServer>]
 [-ResourceGroupName <String>] [-ServerName <String>] [-SubscriptionId <String>] [-Location <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="57451-105">설명은</span><span class="sxs-lookup"><span data-stu-id="57451-105">DESCRIPTION</span></span>
<span data-ttu-id="57451-106">기존에 있는 a 2 Iadb를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="57451-106">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="57451-107">예제의</span><span class="sxs-lookup"><span data-stu-id="57451-107">EXAMPLES</span></span>

### <span data-ttu-id="57451-108">예제 1: 서버 이름에 따라 PointInTime a e b를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="57451-108">Example 1: Restore a PointInTime MariaDB by server name.</span></span>
```powershell
PS C:\> Restore-AzMariaDbServer -Name restore-db01 -ServerName mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db01 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="57451-109">이 명령은 PointInTime a 서버 이름을 기준으로 하 여 e b를 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="57451-109">This command restore a PointInTime MariaDB by server name.</span></span>

### <span data-ttu-id="57451-110">예제 2: 서버 개체를 기준으로 PointInTime을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="57451-110">Example 2: Restore a PointInTime MariaDB by server object</span></span>
```powershell
PS C:\> $db = Get-AzMariaDbServer -Name mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z
PS C:\>Restore-AzMariaDbServer -Name restore-db02 -InputObject $db -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db02 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="57451-111">이 명령을 실행할 때 서버 개체 별로 PointInTime을 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="57451-111">This command restore a PointInTime MariaDB by server object.</span></span>

## <span data-ttu-id="57451-112">변수</span><span class="sxs-lookup"><span data-stu-id="57451-112">PARAMETERS</span></span>

### <span data-ttu-id="57451-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57451-113">-AsJob</span></span>
<span data-ttu-id="57451-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="57451-114">Run the command as a job</span></span>

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

### <span data-ttu-id="57451-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57451-115">-DefaultProfile</span></span>
<span data-ttu-id="57451-116">region DefaultParameters Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="57451-116">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57451-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57451-117">-InputObject</span></span>
<span data-ttu-id="57451-118">복원할 원본 서버 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="57451-118">The source server object to restore from.</span></span>
<span data-ttu-id="57451-119">생성 하려면 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="57451-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="57451-120">-위치</span><span class="sxs-lookup"><span data-stu-id="57451-120">-Location</span></span>
<span data-ttu-id="57451-121">리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="57451-121">The location the resource resides in.</span></span>

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

### <span data-ttu-id="57451-122">-이름</span><span class="sxs-lookup"><span data-stu-id="57451-122">-Name</span></span>
<span data-ttu-id="57451-123">복원할 대상 서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57451-123">The dest server name to restore from.</span></span>

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

### <span data-ttu-id="57451-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="57451-124">-NoWait</span></span>
<span data-ttu-id="57451-125">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="57451-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="57451-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57451-126">-ResourceGroupName</span></span>
<span data-ttu-id="57451-127">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57451-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="57451-128">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57451-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="57451-129">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="57451-129">-RestorePointInTime</span></span>
<span data-ttu-id="57451-130">리소스가 있는 위치를 PointInTimeRestore 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="57451-130">region PointInTimeRestore The location the resource resides in.</span></span>

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

### <span data-ttu-id="57451-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="57451-131">-ServerName</span></span>
<span data-ttu-id="57451-132">복원할 원본 서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57451-132">The source server name to restore from.</span></span>

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

### <span data-ttu-id="57451-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="57451-133">-SubscriptionId</span></span>
<span data-ttu-id="57451-134">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 Id를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="57451-134">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="57451-135">구독 ID는 모든 서비스 호출에 대 한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="57451-135">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="57451-136">태그</span><span class="sxs-lookup"><span data-stu-id="57451-136">-Tag</span></span>
<span data-ttu-id="57451-137">키-값 쌍의 형식으로 된 응용 프로그램 관련 메타 데이터</span><span class="sxs-lookup"><span data-stu-id="57451-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="57451-138">-확인</span><span class="sxs-lookup"><span data-stu-id="57451-138">-Confirm</span></span>
<span data-ttu-id="57451-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="57451-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57451-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57451-140">-WhatIf</span></span>
<span data-ttu-id="57451-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="57451-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57451-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="57451-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57451-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57451-143">CommonParameters</span></span>
<span data-ttu-id="57451-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="57451-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57451-145">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="57451-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57451-146">입력</span><span class="sxs-lookup"><span data-stu-id="57451-146">INPUTS</span></span>

### <span data-ttu-id="57451-147">Api20180601Preview Iadb. i r i. IServer</span><span class="sxs-lookup"><span data-stu-id="57451-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="57451-148">출력</span><span class="sxs-lookup"><span data-stu-id="57451-148">OUTPUTS</span></span>

### <span data-ttu-id="57451-149">Api20180601Preview Iadb. i r i. IServer</span><span class="sxs-lookup"><span data-stu-id="57451-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="57451-150">상속자</span><span class="sxs-lookup"><span data-stu-id="57451-150">NOTES</span></span>

<span data-ttu-id="57451-151">별칭과</span><span class="sxs-lookup"><span data-stu-id="57451-151">ALIASES</span></span>

<span data-ttu-id="57451-152">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="57451-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="57451-153">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="57451-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="57451-154">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="57451-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="57451-155">INPUTOBJECT <IServer> : 복원할 원본 서버 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="57451-155">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="57451-156">`Location <String>`: 리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="57451-156">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="57451-157">`[Tag <ITrackedResourceTags>]`: 키-값 쌍의 형식으로 된 응용 프로그램 관련 메타 데이터</span><span class="sxs-lookup"><span data-stu-id="57451-157">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="57451-158">`[(Any) <String>]`:이 개체에 모든 속성이 추가 될 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="57451-158">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="57451-159">`[AdministratorLogin <String>]`: 서버의 관리자 로그인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57451-159">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="57451-160">서버를 만드는 경우에만 지정할 수 있습니다 (만들기에 필요 함).</span><span class="sxs-lookup"><span data-stu-id="57451-160">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="57451-161">`[EarliestRestoreDate <DateTime?>]`: 초기 복원 시점 생성 시간 (ISO8601 형식)</span><span class="sxs-lookup"><span data-stu-id="57451-161">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="57451-162">`[FullyQualifiedDomainName <String>]`: 서버의 정규화 된 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57451-162">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="57451-163">`[IdentityType <IdentityType?>]`: Id 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="57451-163">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="57451-164">해당 리소스에 대 한 Azure Active Directory 보안 주체를 자동으로 만들고 할당 하려면이를 ' SystemAssigned '로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57451-164">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="57451-165">`[MasterServerId <String>]`: 복제본 서버의 마스터 서버 id입니다.</span><span class="sxs-lookup"><span data-stu-id="57451-165">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="57451-166">`[ReplicaCapacity <Int32?>]`: 마스터 서버에 포함할 수 있는 최대 복제 데이터베이스 수입니다.</span><span class="sxs-lookup"><span data-stu-id="57451-166">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="57451-167">`[ReplicationRole <String>]`: 서버의 복제 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="57451-167">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="57451-168">`[SkuCapacity <Int32?>]`: 서버의 계산 단위를 나타내는 스케일 업/out 용량입니다.</span><span class="sxs-lookup"><span data-stu-id="57451-168">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="57451-169">`[SkuFamily <String>]`: 하드웨어의 패밀리입니다.</span><span class="sxs-lookup"><span data-stu-id="57451-169">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="57451-170">`[SkuName <String>]`: Sku의 이름 (일반적으로 계층 + 패밀리 + 코어) (예: B_Gen4_1 GP_Gen5_8)입니다.</span><span class="sxs-lookup"><span data-stu-id="57451-170">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="57451-171">`[SkuSize <String>]`: 리소스에 따라 적절 하 게 해석 되는 크기 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="57451-171">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="57451-172">`[SkuTier <SkuTier?>]`: 특정 SKU (예: 기본)의 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="57451-172">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="57451-173">`[SslEnforcement <SslEnforcementEnum?>]`: 서버에 연결할 때 ssl 적용 여부를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="57451-173">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="57451-174">`[StorageProfileBackupRetentionDay <Int32?>]`: 서버에 대 한 백업 보존 일입니다.</span><span class="sxs-lookup"><span data-stu-id="57451-174">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="57451-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: 서버 백업에 대해 지리적 중복을 사용 하거나 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="57451-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="57451-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: 저장소 자동 증가를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="57451-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="57451-177">`[StorageProfileStorageMb <Int32?>]`: 서버에 허용 된 최대 저장소.</span><span class="sxs-lookup"><span data-stu-id="57451-177">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="57451-178">`[UserVisibleState <ServerState?>]`: 사용자에 게 표시 되는 서버의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="57451-178">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="57451-179">`[Version <ServerVersion?>]`: 서버 버전.</span><span class="sxs-lookup"><span data-stu-id="57451-179">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="57451-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57451-180">RELATED LINKS</span></span>

