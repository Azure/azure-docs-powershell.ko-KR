---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/update-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: 65004c35ffa9c4cb227845787c91219a319789fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974667"
---
# <span data-ttu-id="c0cc3-101">Update-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="c0cc3-101">Update-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="c0cc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0cc3-102">SYNOPSIS</span></span>
<span data-ttu-id="c0cc3-103">기존 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-103">Updates an existing server.</span></span>
<span data-ttu-id="c0cc3-104">요청 본문에는 일반 서버 정의에 있는 속성 중 하나에서 많은 속성이 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="c0cc3-105">서버 Update-AzPostSqlFlexibleServerConfiguration 서버 매개 변수를 업데이트하려는 경우 대신 wait_timeout net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-105">Use Update-AzPostSqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="c0cc3-106">구문</span><span class="sxs-lookup"><span data-stu-id="c0cc3-106">SYNTAX</span></span>

### <span data-ttu-id="c0cc3-107">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="c0cc3-107">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-MaintenanceWindow <String>] [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c0cc3-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c0cc3-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity>
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-MaintenanceWindow <String>] [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c0cc3-109">설명</span><span class="sxs-lookup"><span data-stu-id="c0cc3-109">DESCRIPTION</span></span>
<span data-ttu-id="c0cc3-110">기존 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-110">Updates an existing server.</span></span>
<span data-ttu-id="c0cc3-111">요청 본문에는 일반 서버 정의에 있는 속성 중 하나에서 많은 속성이 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="c0cc3-112">서버 Update-AzPostgreSqlFlexibleServerConfiguration 서버 매개 변수를 업데이트하려는 경우 대신 wait_timeout net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-112">Use Update-AzPostgreSqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="c0cc3-113">예제</span><span class="sxs-lookup"><span data-stu-id="c0cc3-113">EXAMPLES</span></span>

### <span data-ttu-id="c0cc3-114">예제 1: 리소스 그룹 및 서버 이름으로 PostgreSql 서버 업데이트</span><span class="sxs-lookup"><span data-stu-id="c0cc3-114">Example 1: Update PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test -Sku Standard_D4s_v3

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus postgresql_test     12     131072                  Standard_D4s_v3 GeneralPurpose
```

<span data-ttu-id="c0cc3-115">이 cmdlet은 리소스 그룹 및 서버 이름으로 PostgreSql 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-115">This cmdlet updates PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="c0cc3-116">예제 2: ID로 PostgreSql 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-116">Example 2: Update PostgreSql server by identity.</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test | Update-AzPostgreSqlFlexibleServer -BackupRetentionDay 23 -StorageMb 10240

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----            -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus   postgresql_test     12     131072                  Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="c0cc3-117">이 cmdlet은 ID로 PostgreSql 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-117">This cmdlet updates PostgreSql server by identity.</span></span>

## <span data-ttu-id="c0cc3-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c0cc3-118">PARAMETERS</span></span>

### <span data-ttu-id="c0cc3-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="c0cc3-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="c0cc3-120">관리자 로그인의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="c0cc3-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0cc3-121">-AsJob</span></span>
<span data-ttu-id="c0cc3-122">명령을 작업으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="c0cc3-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="c0cc3-123">-BackupRetentionDay</span></span>
<span data-ttu-id="c0cc3-124">서버에 대한 백업 보존 일입니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-124">Backup retention days for the server.</span></span>
<span data-ttu-id="c0cc3-125">일 수는 7에서 35 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="c0cc3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0cc3-126">-DefaultProfile</span></span>
<span data-ttu-id="c0cc3-127">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0cc3-128">-HaEnabled</span><span class="sxs-lookup"><span data-stu-id="c0cc3-128">-HaEnabled</span></span>
<span data-ttu-id="c0cc3-129">고가용성 기능을 사용하도록 설정하거나 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-129">Enable or disable high availability feature.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.HaEnabledEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0cc3-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0cc3-130">-InputObject</span></span>
<span data-ttu-id="c0cc3-131">ID 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-131">Identity Parameter.</span></span>
<span data-ttu-id="c0cc3-132">생성을 위해 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-132">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c0cc3-133">-MaintenanceWindow</span><span class="sxs-lookup"><span data-stu-id="c0cc3-133">-MaintenanceWindow</span></span>
<span data-ttu-id="c0cc3-134">유지 관리에 지정된 기간(UTC)입니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-134">Period of time (UTC) designated for maintenance.</span></span>
<span data-ttu-id="c0cc3-135">예: 일요일 11:30pm UTC에 예약하는 "Sun:23:30"입니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-135">Examples: "Sun:23:30" to schedule on Sunday, 11:30pm UTC.</span></span>
<span data-ttu-id="c0cc3-136">"사용 안 하여"에서 기본 패스로 다시 설정</span><span class="sxs-lookup"><span data-stu-id="c0cc3-136">To set back to default pass in "Disabled"</span></span>

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

### <span data-ttu-id="c0cc3-137">-Name</span><span class="sxs-lookup"><span data-stu-id="c0cc3-137">-Name</span></span>
<span data-ttu-id="c0cc3-138">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-138">The name of the server.</span></span>

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

### <span data-ttu-id="c0cc3-139">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c0cc3-139">-NoWait</span></span>
<span data-ttu-id="c0cc3-140">명령을 비동기적으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-140">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="c0cc3-141">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="c0cc3-141">-ReplicationRole</span></span>
<span data-ttu-id="c0cc3-142">서버의 복제 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-142">The replication role of the server.</span></span>

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

### <span data-ttu-id="c0cc3-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0cc3-143">-ResourceGroupName</span></span>
<span data-ttu-id="c0cc3-144">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-144">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c0cc3-145">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-145">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c0cc3-146">-Sku</span><span class="sxs-lookup"><span data-stu-id="c0cc3-146">-Sku</span></span>
<span data-ttu-id="c0cc3-147">sku의 이름(예: Burstable_B1ms Standard_D2ds_v4</span><span class="sxs-lookup"><span data-stu-id="c0cc3-147">The name of the sku, e.g. Burstable_B1ms, Standard_D2ds_v4</span></span>

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

### <span data-ttu-id="c0cc3-148">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="c0cc3-148">-SkuTier</span></span>
<span data-ttu-id="c0cc3-149">특정 SKU의 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-149">The tier of the particular SKU.</span></span>
<span data-ttu-id="c0cc3-150">수락된 값: Burstable, GeneralPurpose, 메모리 최적화.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-150">Accepted values: Burstable, GeneralPurpose, Memory Optimized.</span></span>
<span data-ttu-id="c0cc3-151">기본값: Burstable입니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-151">Default: Burstable.</span></span>

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

### <span data-ttu-id="c0cc3-152">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="c0cc3-152">-SslEnforcement</span></span>
<span data-ttu-id="c0cc3-153">서버에 연결할 때 ssl 적용을 사용하도록 설정하거나 활성화하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-153">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="c0cc3-154">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="c0cc3-154">-StorageAutogrow</span></span>
<span data-ttu-id="c0cc3-155">저장소 자동 증가를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-155">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="c0cc3-156">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="c0cc3-156">-StorageInMb</span></span>
<span data-ttu-id="c0cc3-157">서버에 대해 허용되는 최대 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-157">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="c0cc3-158">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c0cc3-158">-SubscriptionId</span></span>
<span data-ttu-id="c0cc3-159">Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-159">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="c0cc3-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="c0cc3-160">-Tag</span></span>
<span data-ttu-id="c0cc3-161">키-값 쌍의 형태로 애플리케이션별 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-161">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="c0cc3-162">-확인</span><span class="sxs-lookup"><span data-stu-id="c0cc3-162">-Confirm</span></span>
<span data-ttu-id="c0cc3-163">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0cc3-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0cc3-164">-WhatIf</span></span>
<span data-ttu-id="c0cc3-165">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0cc3-166">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0cc3-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0cc3-167">CommonParameters</span></span>
<span data-ttu-id="c0cc3-168">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0cc3-169">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0cc3-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0cc3-170">입력</span><span class="sxs-lookup"><span data-stu-id="c0cc3-170">INPUTS</span></span>

### <span data-ttu-id="c0cc3-171">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="c0cc3-171">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="c0cc3-172">출력</span><span class="sxs-lookup"><span data-stu-id="c0cc3-172">OUTPUTS</span></span>

### <span data-ttu-id="c0cc3-173">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="c0cc3-173">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="c0cc3-174">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c0cc3-174">NOTES</span></span>

<span data-ttu-id="c0cc3-175">별칭</span><span class="sxs-lookup"><span data-stu-id="c0cc3-175">ALIASES</span></span>

<span data-ttu-id="c0cc3-176">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="c0cc3-176">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c0cc3-177">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-177">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c0cc3-178">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-178">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c0cc3-179">INPUTOBJECT <IPostgreSqlIdentity> : ID 매개 변수.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-179">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="c0cc3-180">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-180">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="c0cc3-181">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-181">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="c0cc3-182">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-182">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="c0cc3-183">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="c0cc3-183">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c0cc3-184">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-184">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="c0cc3-185">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-185">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c0cc3-186">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-186">The name is case insensitive.</span></span>
  - <span data-ttu-id="c0cc3-187">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-187">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="c0cc3-188">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-188">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="c0cc3-189">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-189">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c0cc3-190">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0cc3-190">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="c0cc3-191">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c0cc3-191">RELATED LINKS</span></span>

