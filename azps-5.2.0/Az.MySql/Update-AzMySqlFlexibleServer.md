---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServer.md
ms.openlocfilehash: 3e1f79f431e5f0ff5c39c03a7f3c41a20c2543e4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360228"
---
# <span data-ttu-id="e3686-101">Update-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="e3686-101">Update-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="e3686-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3686-102">SYNOPSIS</span></span>
<span data-ttu-id="e3686-103">기존 MySQL 유연한 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-103">Updates an existing MySQL flexible server.</span></span>
<span data-ttu-id="e3686-104">요청 본문은 일반 서버 정의에 있는 속성 중 하나에서 다수 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="e3686-105">대신 Update-AzMySqlFlexibleServerConfiguration 서버 매개 변수를 업데이트하려는 경우 wait_timeout net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="e3686-105">Use Update-AzMySqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="e3686-106">구문</span><span class="sxs-lookup"><span data-stu-id="e3686-106">SYNTAX</span></span>

### <span data-ttu-id="e3686-107">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="e3686-107">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e3686-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e3686-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>] [-ReplicationRole <String>] [-Sku <String>]
 [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>]
 [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e3686-109">설명</span><span class="sxs-lookup"><span data-stu-id="e3686-109">DESCRIPTION</span></span>
<span data-ttu-id="e3686-110">기존 MySQL 유연한 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-110">Updates an existing MySQL flexible server.</span></span>
<span data-ttu-id="e3686-111">요청 본문은 일반 서버 정의에 있는 속성 중 하나에서 다수 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="e3686-112">대신 Update-AzMySqlFlexibleServerConfiguration 서버 매개 변수를 업데이트하려는 경우 wait_timeout net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="e3686-112">Use Update-AzMySqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="e3686-113">예제</span><span class="sxs-lookup"><span data-stu-id="e3686-113">EXAMPLES</span></span>

### <span data-ttu-id="e3686-114">예제 1: 리소스 그룹 및 서버 이름으로 MySql 서버 업데이트</span><span class="sxs-lookup"><span data-stu-id="e3686-114">Example 1: Update MySql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test -Sku Standard_D4ds_v4

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D4ds_v4 GeneralPurpose
```

<span data-ttu-id="e3686-115">이 cmdlet은 리소스 그룹 및 서버 이름으로 MySql 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-115">This cmdlet updates MySql server by resource group and server name.</span></span>

### <span data-ttu-id="e3686-116">예제 2: ID로 MySql 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-116">Example 2: Update MySql server by identity.</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Update-AzMySqlFlexibleServer -BackupRetentionDay 23 -StorageInMb 10240

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="e3686-117">이 cmdlet은 ID로 MySql 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-117">This cmdlet updates MySql server by identity.</span></span>

## <span data-ttu-id="e3686-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3686-118">PARAMETERS</span></span>

### <span data-ttu-id="e3686-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="e3686-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="e3686-120">관리자 로그인의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="e3686-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3686-121">-AsJob</span></span>
<span data-ttu-id="e3686-122">명령을 작업으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="e3686-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="e3686-123">-BackupRetentionDay</span></span>
<span data-ttu-id="e3686-124">서버에 대한 백업 보존 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-124">Backup retention days for the server.</span></span>
<span data-ttu-id="e3686-125">일 수는 7에서 35 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="e3686-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3686-126">-DefaultProfile</span></span>
<span data-ttu-id="e3686-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3686-128">-HaEnabled</span><span class="sxs-lookup"><span data-stu-id="e3686-128">-HaEnabled</span></span>
<span data-ttu-id="e3686-129">고가용성 기능을 사용 또는 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="e3686-129">Enable or disable high availability feature.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.HaEnabledEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3686-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3686-130">-InputObject</span></span>
<span data-ttu-id="e3686-131">ID 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-131">Identity Parameter.</span></span>
<span data-ttu-id="e3686-132">생성을 위해 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="e3686-132">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3686-133">-Name</span><span class="sxs-lookup"><span data-stu-id="e3686-133">-Name</span></span>
<span data-ttu-id="e3686-134">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-134">The name of the server.</span></span>

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

### <span data-ttu-id="e3686-135">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e3686-135">-NoWait</span></span>
<span data-ttu-id="e3686-136">명령을 비동기적으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-136">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="e3686-137">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="e3686-137">-ReplicationRole</span></span>
<span data-ttu-id="e3686-138">서버의 복제 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-138">The replication role of the server.</span></span>

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

### <span data-ttu-id="e3686-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3686-139">-ResourceGroupName</span></span>
<span data-ttu-id="e3686-140">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-140">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e3686-141">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-141">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e3686-142">-Sku</span><span class="sxs-lookup"><span data-stu-id="e3686-142">-Sku</span></span>
<span data-ttu-id="e3686-143">SKU의 이름(일반적으로 계층 + 패밀리 + 코어)입니다(예: B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="e3686-143">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="e3686-144">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="e3686-144">-SkuTier</span></span>
<span data-ttu-id="e3686-145">특정 SKU의 계층(예: 기본)</span><span class="sxs-lookup"><span data-stu-id="e3686-145">The tier of the particular SKU, e.g. Basic.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.SkuTier
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3686-146">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="e3686-146">-SslEnforcement</span></span>
<span data-ttu-id="e3686-147">서버에 연결할 때 ssl 적용을 사용하도록 설정하거나 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-147">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3686-148">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="e3686-148">-StorageAutogrow</span></span>
<span data-ttu-id="e3686-149">저장소 자동 증가를 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="e3686-149">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3686-150">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="e3686-150">-StorageInMb</span></span>
<span data-ttu-id="e3686-151">서버에 허용되는 최대 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-151">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="e3686-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e3686-152">-SubscriptionId</span></span>
<span data-ttu-id="e3686-153">Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-153">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="e3686-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="e3686-154">-Tag</span></span>
<span data-ttu-id="e3686-155">키-값 쌍의 형태로 애플리케이션별 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-155">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="e3686-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3686-156">-Confirm</span></span>
<span data-ttu-id="e3686-157">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3686-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3686-158">-WhatIf</span></span>
<span data-ttu-id="e3686-159">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e3686-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3686-160">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3686-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3686-161">CommonParameters</span></span>
<span data-ttu-id="e3686-162">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3686-163">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e3686-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3686-164">입력</span><span class="sxs-lookup"><span data-stu-id="e3686-164">INPUTS</span></span>

### <span data-ttu-id="e3686-165">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="e3686-165">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="e3686-166">출력</span><span class="sxs-lookup"><span data-stu-id="e3686-166">OUTPUTS</span></span>

### <span data-ttu-id="e3686-167">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="e3686-167">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="e3686-168">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e3686-168">NOTES</span></span>

<span data-ttu-id="e3686-169">별칭</span><span class="sxs-lookup"><span data-stu-id="e3686-169">ALIASES</span></span>

<span data-ttu-id="e3686-170">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="e3686-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e3686-171">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e3686-172">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e3686-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e3686-173">INPUTOBJECT: <IMySqlIdentity> ID 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-173">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="e3686-174">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-174">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="e3686-175">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-175">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="e3686-176">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-176">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="e3686-177">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="e3686-177">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e3686-178">`[KeyName <String>]`: 서버 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-178">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="e3686-179">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-179">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="e3686-180">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-180">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e3686-181">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-181">The name is case insensitive.</span></span>
  - <span data-ttu-id="e3686-182">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-182">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="e3686-183">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-183">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="e3686-184">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-184">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e3686-185">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3686-185">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="e3686-186">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e3686-186">RELATED LINKS</span></span>

