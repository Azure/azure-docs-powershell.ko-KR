---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlServer.md
ms.openlocfilehash: ecb568a356d0f1cf5ed36d966028e2d0ca4f813a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492467"
---
# <span data-ttu-id="d4170-101">Update-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="d4170-101">Update-AzPostgreSqlServer</span></span>

## <span data-ttu-id="d4170-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4170-102">SYNOPSIS</span></span>
<span data-ttu-id="d4170-103">기존 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-103">Updates an existing server.</span></span>
<span data-ttu-id="d4170-104">요청 본문은 일반 서버 정의에 있는 속성 중 하나에서 다수 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="d4170-105">대신 Update-AzPostSqlConfiguration 서버 매개 변수를 업데이트하려는 경우 wait_timeout net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="d4170-105">Use Update-AzPostSqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="d4170-106">구문</span><span class="sxs-lookup"><span data-stu-id="d4170-106">SYNTAX</span></span>

### <span data-ttu-id="d4170-107">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="d4170-107">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d4170-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d4170-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-ReplicationRole <String>] [-Sku <String>] [-SkuCapacity <Int32>]
 [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d4170-109">설명</span><span class="sxs-lookup"><span data-stu-id="d4170-109">DESCRIPTION</span></span>
<span data-ttu-id="d4170-110">기존 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-110">Updates an existing server.</span></span>
<span data-ttu-id="d4170-111">요청 본문은 일반 서버 정의에 있는 속성 중 하나에서 다수 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="d4170-112">대신 Update-AzPostSqlConfiguration 서버 매개 변수를 업데이트하려는 경우 wait_timeout net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="d4170-112">Use Update-AzPostSqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="d4170-113">예제</span><span class="sxs-lookup"><span data-stu-id="d4170-113">EXAMPLES</span></span>

### <span data-ttu-id="d4170-114">예제 1: 리소스 그룹 및 서버 이름으로 PostgreSql 서버 업데이트</span><span class="sxs-lookup"><span data-stu-id="d4170-114">Example 1: Update PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SslEnforcement Disabled

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="d4170-115">이 cmdlet은 리소스 그룹 및 서버 이름으로 PostgreSql 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-115">This cmdlet updates PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="d4170-116">예제 2: ID로 PostgreSql 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-116">Example 2: Update PostgreSql server by identity.</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Update-AzPostgreSqlServer -BackupRetentionDay 23

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="d4170-117">이 cmdlet은 ID에 의해 PostgreSql 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-117">This cmdlet updates PostgreSql server by identity.</span></span>

## <span data-ttu-id="d4170-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4170-118">PARAMETERS</span></span>

### <span data-ttu-id="d4170-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="d4170-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="d4170-120">관리자 로그인의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-120">The password of the administrator login.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4170-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4170-121">-AsJob</span></span>
<span data-ttu-id="d4170-122">명령을 작업으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="d4170-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="d4170-123">-BackupRetentionDay</span></span>
<span data-ttu-id="d4170-124">서버에 대한 백업 보존 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-124">Backup retention days for the server.</span></span>
<span data-ttu-id="d4170-125">일 수는 7에서 35 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-125">Day count is between 7 and 35.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4170-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4170-126">-DefaultProfile</span></span>
<span data-ttu-id="d4170-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4170-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4170-128">-InputObject</span></span>
<span data-ttu-id="d4170-129">ID 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-129">Identity Parameter.</span></span>
<span data-ttu-id="d4170-130">생성을 위해 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="d4170-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4170-131">-Name</span><span class="sxs-lookup"><span data-stu-id="d4170-131">-Name</span></span>
<span data-ttu-id="d4170-132">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-132">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4170-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d4170-133">-NoWait</span></span>
<span data-ttu-id="d4170-134">명령을 비동기적으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-134">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="d4170-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="d4170-135">-ReplicationRole</span></span>
<span data-ttu-id="d4170-136">서버의 복제 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="d4170-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4170-137">-ResourceGroupName</span></span>
<span data-ttu-id="d4170-138">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-138">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d4170-139">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-139">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4170-140">-Sku</span><span class="sxs-lookup"><span data-stu-id="d4170-140">-Sku</span></span>
<span data-ttu-id="d4170-141">SKU의 이름(일반적으로 계층 + 패밀리 + 코어)입니다(예: B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="d4170-141">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="d4170-142">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="d4170-142">-SkuCapacity</span></span>
<span data-ttu-id="d4170-143">서버의 컴퓨팅 단위를 나타내는 확장/확장 용량입니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-143">The scale up/out capacity, representing server's compute units.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4170-144">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="d4170-144">-SkuFamily</span></span>
<span data-ttu-id="d4170-145">하드웨어의 패밀리입니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-145">The family of hardware.</span></span>

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

### <span data-ttu-id="d4170-146">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="d4170-146">-SkuTier</span></span>
<span data-ttu-id="d4170-147">특정 SKU의 계층(예: 기본)</span><span class="sxs-lookup"><span data-stu-id="d4170-147">The tier of the particular SKU, e.g. Basic.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.SkuTier
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4170-148">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="d4170-148">-SslEnforcement</span></span>
<span data-ttu-id="d4170-149">서버에 연결할 때 ssl 적용을 사용하도록 설정하거나 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-149">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4170-150">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="d4170-150">-StorageAutogrow</span></span>
<span data-ttu-id="d4170-151">저장소 자동 증가를 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="d4170-151">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4170-152">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="d4170-152">-StorageInMb</span></span>
<span data-ttu-id="d4170-153">서버에 허용되는 최대 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-153">Max storage allowed for a server.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4170-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d4170-154">-SubscriptionId</span></span>
<span data-ttu-id="d4170-155">Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-155">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4170-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="d4170-156">-Tag</span></span>
<span data-ttu-id="d4170-157">키-값 쌍의 형태로 애플리케이션별 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-157">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="d4170-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4170-158">-Confirm</span></span>
<span data-ttu-id="d4170-159">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4170-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4170-160">-WhatIf</span></span>
<span data-ttu-id="d4170-161">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d4170-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4170-162">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4170-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4170-163">CommonParameters</span></span>
<span data-ttu-id="d4170-164">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4170-165">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d4170-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4170-166">입력</span><span class="sxs-lookup"><span data-stu-id="d4170-166">INPUTS</span></span>

### <span data-ttu-id="d4170-167">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="d4170-167">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="d4170-168">출력</span><span class="sxs-lookup"><span data-stu-id="d4170-168">OUTPUTS</span></span>

### <span data-ttu-id="d4170-169">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="d4170-169">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="d4170-170">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d4170-170">NOTES</span></span>

<span data-ttu-id="d4170-171">별칭</span><span class="sxs-lookup"><span data-stu-id="d4170-171">ALIASES</span></span>

<span data-ttu-id="d4170-172">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="d4170-172">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d4170-173">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-173">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d4170-174">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d4170-174">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d4170-175">INPUTOBJECT: <IPostgreSqlIdentity> ID 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-175">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="d4170-176">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-176">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d4170-177">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-177">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d4170-178">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-178">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d4170-179">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="d4170-179">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d4170-180">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-180">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d4170-181">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-181">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d4170-182">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-182">The name is case insensitive.</span></span>
  - <span data-ttu-id="d4170-183">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-183">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d4170-184">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-184">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d4170-185">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-185">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d4170-186">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d4170-186">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d4170-187">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d4170-187">RELATED LINKS</span></span>

