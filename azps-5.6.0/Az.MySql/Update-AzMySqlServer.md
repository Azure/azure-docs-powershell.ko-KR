---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
ms.openlocfilehash: 46408fc5cd6f718f26c4f55eb7f8bab56891d8b5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968752"
---
# <span data-ttu-id="1057f-101">Update-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="1057f-101">Update-AzMySqlServer</span></span>

## <span data-ttu-id="1057f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1057f-102">SYNOPSIS</span></span>
<span data-ttu-id="1057f-103">기존 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-103">Updates an existing server.</span></span>
<span data-ttu-id="1057f-104">요청 본문에는 일반 서버 정의에 있는 속성 중 하나에서 많은 속성이 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="1057f-105">서버 Update-AzMySqlConfiguration 서버 매개 변수를 업데이트하려는 경우 대신 wait_timeout net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="1057f-105">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="1057f-106">구문</span><span class="sxs-lookup"><span data-stu-id="1057f-106">SYNTAX</span></span>

### <span data-ttu-id="1057f-107">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="1057f-107">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>] [-Sku <String>]
 [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1057f-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1057f-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlServer -InputObject <IMySqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1057f-109">설명</span><span class="sxs-lookup"><span data-stu-id="1057f-109">DESCRIPTION</span></span>
<span data-ttu-id="1057f-110">기존 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-110">Updates an existing server.</span></span>
<span data-ttu-id="1057f-111">요청 본문에는 일반 서버 정의에 있는 속성 중 하나에서 많은 속성이 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="1057f-112">서버 Update-AzMySqlConfiguration 서버 매개 변수를 업데이트하려는 경우 대신 wait_timeout net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="1057f-112">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="1057f-113">예제</span><span class="sxs-lookup"><span data-stu-id="1057f-113">EXAMPLES</span></span>

### <span data-ttu-id="1057f-114">예제 1: 리소스 그룹 및 서버 이름으로 MySql 서버 업데이트</span><span class="sxs-lookup"><span data-stu-id="1057f-114">Example 1: Update MySql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -SslEnforcement Disabled

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="1057f-115">이 cmdlet은 리소스 그룹 및 서버 이름으로 MySql 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-115">This cmdlet updates MySql server by resource group and server name.</span></span>

### <span data-ttu-id="1057f-116">예제 2: ID로 MySql 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-116">Example 2: Update MySql server by identity.</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Update-AzMySqlServer -BackupRetentionDay 23 -StorageMb 10240

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="1057f-117">이 cmdlet은 ID로 MySql 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-117">This cmdlet updates MySql server by identity.</span></span>

## <span data-ttu-id="1057f-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1057f-118">PARAMETERS</span></span>

### <span data-ttu-id="1057f-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="1057f-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="1057f-120">관리자 로그인의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="1057f-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1057f-121">-AsJob</span></span>
<span data-ttu-id="1057f-122">명령을 작업으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="1057f-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="1057f-123">-BackupRetentionDay</span></span>
<span data-ttu-id="1057f-124">서버에 대한 백업 보존 일입니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-124">Backup retention days for the server.</span></span>
<span data-ttu-id="1057f-125">일 수는 7에서 35 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="1057f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1057f-126">-DefaultProfile</span></span>
<span data-ttu-id="1057f-127">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1057f-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1057f-128">-InputObject</span></span>
<span data-ttu-id="1057f-129">ID 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-129">Identity Parameter.</span></span>
<span data-ttu-id="1057f-130">생성을 위해 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="1057f-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1057f-131">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="1057f-131">-MinimalTlsVersion</span></span>
<span data-ttu-id="1057f-132">SSL을 사용하도록 설정하면 서버에 대한 연결에 대한 최소 TLS 버전을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-132">Set the minimal TLS version for connections to server when SSL is enabled.</span></span>
<span data-ttu-id="1057f-133">기본값은 TLSEnforcementDisabled.accepted 값입니다. TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled입니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-133">Default is TLSEnforcementDisabled.accepted values: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.MinimalTlsVersionEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1057f-134">-Name</span><span class="sxs-lookup"><span data-stu-id="1057f-134">-Name</span></span>
<span data-ttu-id="1057f-135">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-135">The name of the server.</span></span>

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

### <span data-ttu-id="1057f-136">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1057f-136">-NoWait</span></span>
<span data-ttu-id="1057f-137">명령을 비동기적으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-137">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="1057f-138">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="1057f-138">-ReplicationRole</span></span>
<span data-ttu-id="1057f-139">서버의 복제 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-139">The replication role of the server.</span></span>

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

### <span data-ttu-id="1057f-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1057f-140">-ResourceGroupName</span></span>
<span data-ttu-id="1057f-141">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-141">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="1057f-142">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-142">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="1057f-143">-Sku</span><span class="sxs-lookup"><span data-stu-id="1057f-143">-Sku</span></span>
<span data-ttu-id="1057f-144">sku의 이름은 일반적으로 계층 + 패밀리 + 코어(예: B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="1057f-144">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="1057f-145">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="1057f-145">-SkuCapacity</span></span>
<span data-ttu-id="1057f-146">서버의 계산 단위를 나타내는 확장/확장 용량입니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-146">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="1057f-147">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="1057f-147">-SkuFamily</span></span>
<span data-ttu-id="1057f-148">하드웨어의 패밀리입니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-148">The family of hardware.</span></span>

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

### <span data-ttu-id="1057f-149">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="1057f-149">-SkuTier</span></span>
<span data-ttu-id="1057f-150">특정 SKU의 계층(예: Basic)입니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-150">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="1057f-151">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="1057f-151">-SslEnforcement</span></span>
<span data-ttu-id="1057f-152">서버에 연결할 때 ssl 적용을 사용하도록 설정하거나 활성화하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-152">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="1057f-153">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="1057f-153">-StorageAutogrow</span></span>
<span data-ttu-id="1057f-154">저장소 자동 증가를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-154">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="1057f-155">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="1057f-155">-StorageInMb</span></span>
<span data-ttu-id="1057f-156">서버에 대해 허용되는 최대 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-156">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="1057f-157">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1057f-157">-SubscriptionId</span></span>
<span data-ttu-id="1057f-158">Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-158">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="1057f-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="1057f-159">-Tag</span></span>
<span data-ttu-id="1057f-160">키-값 쌍의 형태로 애플리케이션별 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-160">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="1057f-161">-확인</span><span class="sxs-lookup"><span data-stu-id="1057f-161">-Confirm</span></span>
<span data-ttu-id="1057f-162">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1057f-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1057f-163">-WhatIf</span></span>
<span data-ttu-id="1057f-164">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1057f-165">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1057f-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1057f-166">CommonParameters</span></span>
<span data-ttu-id="1057f-167">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1057f-168">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1057f-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1057f-169">입력</span><span class="sxs-lookup"><span data-stu-id="1057f-169">INPUTS</span></span>

### <span data-ttu-id="1057f-170">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="1057f-170">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="1057f-171">출력</span><span class="sxs-lookup"><span data-stu-id="1057f-171">OUTPUTS</span></span>

### <span data-ttu-id="1057f-172">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="1057f-172">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="1057f-173">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1057f-173">NOTES</span></span>

<span data-ttu-id="1057f-174">별칭</span><span class="sxs-lookup"><span data-stu-id="1057f-174">ALIASES</span></span>

<span data-ttu-id="1057f-175">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="1057f-175">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1057f-176">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-176">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1057f-177">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1057f-177">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1057f-178">INPUTOBJECT <IMySqlIdentity> : ID 매개 변수.</span><span class="sxs-lookup"><span data-stu-id="1057f-178">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="1057f-179">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-179">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="1057f-180">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-180">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="1057f-181">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-181">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="1057f-182">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="1057f-182">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1057f-183">`[KeyName <String>]`: 서버 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-183">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="1057f-184">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-184">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="1057f-185">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-185">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="1057f-186">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-186">The name is case insensitive.</span></span>
  - <span data-ttu-id="1057f-187">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-187">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="1057f-188">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-188">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="1057f-189">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-189">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="1057f-190">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1057f-190">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="1057f-191">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1057f-191">RELATED LINKS</span></span>

