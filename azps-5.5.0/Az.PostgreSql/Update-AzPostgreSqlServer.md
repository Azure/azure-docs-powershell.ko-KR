---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlServer.md
ms.openlocfilehash: 4b0d2f01336de83acbd904e08b0d0cbc62c0aca6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202177"
---
# <span data-ttu-id="d5314-101">Update-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="d5314-101">Update-AzPostgreSqlServer</span></span>

## <span data-ttu-id="d5314-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5314-102">SYNOPSIS</span></span>
<span data-ttu-id="d5314-103">기존 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-103">Updates an existing server.</span></span>
<span data-ttu-id="d5314-104">요청 본문은 일반 서버 정의에 있는 속성 중 하나에서 다수 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="d5314-105">대신 Update-AzPostSqlConfiguration 서버 매개 변수를 업데이트하려는 경우 wait_timeout net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="d5314-105">Use Update-AzPostSqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="d5314-106">구문</span><span class="sxs-lookup"><span data-stu-id="d5314-106">SYNTAX</span></span>

### <span data-ttu-id="d5314-107">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="d5314-107">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>] [-Sku <String>]
 [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d5314-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d5314-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d5314-109">설명</span><span class="sxs-lookup"><span data-stu-id="d5314-109">DESCRIPTION</span></span>
<span data-ttu-id="d5314-110">기존 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-110">Updates an existing server.</span></span>
<span data-ttu-id="d5314-111">요청 본문은 일반 서버 정의에 있는 속성 중 하나에서 다수 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="d5314-112">대신 Update-AzPostSqlConfiguration 서버 매개 변수를 업데이트하려는 경우 wait_timeout net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="d5314-112">Use Update-AzPostSqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="d5314-113">예제</span><span class="sxs-lookup"><span data-stu-id="d5314-113">EXAMPLES</span></span>

### <span data-ttu-id="d5314-114">예제 1: 리소스 그룹 및 서버 이름으로 PostgreSql 서버 업데이트</span><span class="sxs-lookup"><span data-stu-id="d5314-114">Example 1: Update PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SslEnforcement Disabled

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="d5314-115">이 cmdlet은 리소스 그룹 및 서버 이름으로 PostgreSql 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-115">This cmdlet updates PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="d5314-116">예제 2: ID로 PostgreSql 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-116">Example 2: Update PostgreSql server by identity.</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Update-AzPostgreSqlServer -BackupRetentionDay 23

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="d5314-117">이 cmdlet은 ID에 의해 PostgreSql 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-117">This cmdlet updates PostgreSql server by identity.</span></span>

## <span data-ttu-id="d5314-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5314-118">PARAMETERS</span></span>

### <span data-ttu-id="d5314-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="d5314-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="d5314-120">관리자 로그인의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="d5314-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d5314-121">-AsJob</span></span>
<span data-ttu-id="d5314-122">명령을 작업으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="d5314-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="d5314-123">-BackupRetentionDay</span></span>
<span data-ttu-id="d5314-124">서버에 대한 백업 보존 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-124">Backup retention days for the server.</span></span>
<span data-ttu-id="d5314-125">일 수는 7에서 35 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="d5314-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5314-126">-DefaultProfile</span></span>
<span data-ttu-id="d5314-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5314-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5314-128">-InputObject</span></span>
<span data-ttu-id="d5314-129">ID 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-129">Identity Parameter.</span></span>
<span data-ttu-id="d5314-130">생성을 위해 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="d5314-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d5314-131">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="d5314-131">-MinimalTlsVersion</span></span>
<span data-ttu-id="d5314-132">SSL을 사용할 때 서버에 연결하기 위한 최소 TLS 버전을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-132">Set the minimal TLS version for connections to server when SSL is enabled.</span></span>
<span data-ttu-id="d5314-133">기본값은 TLSEnforcementDisabled.accepted 값(TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled)입니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-133">Default is TLSEnforcementDisabled.accepted values: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.MinimalTlsVersionEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5314-134">-Name</span><span class="sxs-lookup"><span data-stu-id="d5314-134">-Name</span></span>
<span data-ttu-id="d5314-135">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-135">The name of the server.</span></span>

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

### <span data-ttu-id="d5314-136">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d5314-136">-NoWait</span></span>
<span data-ttu-id="d5314-137">명령을 비동기적으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-137">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="d5314-138">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="d5314-138">-ReplicationRole</span></span>
<span data-ttu-id="d5314-139">서버의 복제 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-139">The replication role of the server.</span></span>

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

### <span data-ttu-id="d5314-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5314-140">-ResourceGroupName</span></span>
<span data-ttu-id="d5314-141">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-141">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d5314-142">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-142">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d5314-143">-Sku</span><span class="sxs-lookup"><span data-stu-id="d5314-143">-Sku</span></span>
<span data-ttu-id="d5314-144">SKU의 이름(일반적으로 계층 + 패밀리 + 코어)입니다(예: B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="d5314-144">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="d5314-145">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="d5314-145">-SkuCapacity</span></span>
<span data-ttu-id="d5314-146">서버의 컴퓨팅 단위를 나타내는 확장/확장 용량입니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-146">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="d5314-147">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="d5314-147">-SkuFamily</span></span>
<span data-ttu-id="d5314-148">하드웨어의 패밀리입니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-148">The family of hardware.</span></span>

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

### <span data-ttu-id="d5314-149">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="d5314-149">-SkuTier</span></span>
<span data-ttu-id="d5314-150">특정 SKU의 계층(예: 기본)</span><span class="sxs-lookup"><span data-stu-id="d5314-150">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="d5314-151">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="d5314-151">-SslEnforcement</span></span>
<span data-ttu-id="d5314-152">서버에 연결할 때 ssl 적용을 사용하도록 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-152">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="d5314-153">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="d5314-153">-StorageAutogrow</span></span>
<span data-ttu-id="d5314-154">저장소 자동 증가를 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="d5314-154">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="d5314-155">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="d5314-155">-StorageInMb</span></span>
<span data-ttu-id="d5314-156">서버에 허용되는 최대 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-156">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="d5314-157">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d5314-157">-SubscriptionId</span></span>
<span data-ttu-id="d5314-158">Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-158">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="d5314-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="d5314-159">-Tag</span></span>
<span data-ttu-id="d5314-160">키-값 쌍의 형태로 애플리케이션별 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-160">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="d5314-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d5314-161">-Confirm</span></span>
<span data-ttu-id="d5314-162">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5314-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5314-163">-WhatIf</span></span>
<span data-ttu-id="d5314-164">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d5314-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5314-165">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5314-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5314-166">CommonParameters</span></span>
<span data-ttu-id="d5314-167">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5314-168">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d5314-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5314-169">입력</span><span class="sxs-lookup"><span data-stu-id="d5314-169">INPUTS</span></span>

### <span data-ttu-id="d5314-170">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="d5314-170">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="d5314-171">출력</span><span class="sxs-lookup"><span data-stu-id="d5314-171">OUTPUTS</span></span>

### <span data-ttu-id="d5314-172">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="d5314-172">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="d5314-173">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d5314-173">NOTES</span></span>

<span data-ttu-id="d5314-174">별칭</span><span class="sxs-lookup"><span data-stu-id="d5314-174">ALIASES</span></span>

<span data-ttu-id="d5314-175">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="d5314-175">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d5314-176">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-176">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d5314-177">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d5314-177">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d5314-178">INPUTOBJECT: <IPostgreSqlIdentity> ID 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-178">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="d5314-179">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-179">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d5314-180">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-180">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d5314-181">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-181">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d5314-182">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="d5314-182">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d5314-183">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-183">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d5314-184">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-184">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d5314-185">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-185">The name is case insensitive.</span></span>
  - <span data-ttu-id="d5314-186">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-186">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d5314-187">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-187">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d5314-188">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-188">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d5314-189">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5314-189">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d5314-190">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d5314-190">RELATED LINKS</span></span>

