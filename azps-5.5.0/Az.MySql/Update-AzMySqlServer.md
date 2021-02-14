---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
ms.openlocfilehash: 6168c557e3ae3a417f4c04195e6ef166ea3a01d8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190025"
---
# <span data-ttu-id="388e7-101">Update-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="388e7-101">Update-AzMySqlServer</span></span>

## <span data-ttu-id="388e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="388e7-102">SYNOPSIS</span></span>
<span data-ttu-id="388e7-103">기존 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-103">Updates an existing server.</span></span>
<span data-ttu-id="388e7-104">요청 본문은 일반 서버 정의에 있는 속성 중 하나에서 다수 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="388e7-105">서버 Update-AzMySqlConfiguration 업데이트하려는 경우 대신 wait_timeout 매개 변수를 net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="388e7-105">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="388e7-106">구문</span><span class="sxs-lookup"><span data-stu-id="388e7-106">SYNTAX</span></span>

### <span data-ttu-id="388e7-107">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="388e7-107">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>] [-Sku <String>]
 [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="388e7-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="388e7-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlServer -InputObject <IMySqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="388e7-109">설명</span><span class="sxs-lookup"><span data-stu-id="388e7-109">DESCRIPTION</span></span>
<span data-ttu-id="388e7-110">기존 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-110">Updates an existing server.</span></span>
<span data-ttu-id="388e7-111">요청 본문은 일반 서버 정의에 있는 속성 중 하나에서 다수 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="388e7-112">서버 Update-AzMySqlConfiguration 업데이트하려는 경우 대신 wait_timeout 매개 변수를 net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="388e7-112">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="388e7-113">예제</span><span class="sxs-lookup"><span data-stu-id="388e7-113">EXAMPLES</span></span>

### <span data-ttu-id="388e7-114">예제 1: 리소스 그룹 및 서버 이름으로 MySql 서버 업데이트</span><span class="sxs-lookup"><span data-stu-id="388e7-114">Example 1: Update MySql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -SslEnforcement Disabled

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="388e7-115">이 cmdlet은 리소스 그룹 및 서버 이름으로 MySql 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-115">This cmdlet updates MySql server by resource group and server name.</span></span>

### <span data-ttu-id="388e7-116">예제 2: ID로 MySql 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-116">Example 2: Update MySql server by identity.</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Update-AzMySqlServer -BackupRetentionDay 23 -StorageMb 10240

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="388e7-117">이 cmdlet은 ID로 MySql 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-117">This cmdlet updates MySql server by identity.</span></span>

## <span data-ttu-id="388e7-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="388e7-118">PARAMETERS</span></span>

### <span data-ttu-id="388e7-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="388e7-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="388e7-120">관리자 로그인의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="388e7-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="388e7-121">-AsJob</span></span>
<span data-ttu-id="388e7-122">명령을 작업으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="388e7-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="388e7-123">-BackupRetentionDay</span></span>
<span data-ttu-id="388e7-124">서버에 대한 백업 보존 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-124">Backup retention days for the server.</span></span>
<span data-ttu-id="388e7-125">일 수는 7에서 35 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="388e7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="388e7-126">-DefaultProfile</span></span>
<span data-ttu-id="388e7-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="388e7-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="388e7-128">-InputObject</span></span>
<span data-ttu-id="388e7-129">ID 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-129">Identity Parameter.</span></span>
<span data-ttu-id="388e7-130">생성을 위해 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="388e7-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="388e7-131">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="388e7-131">-MinimalTlsVersion</span></span>
<span data-ttu-id="388e7-132">SSL을 사용할 때 서버에 연결하기 위한 최소 TLS 버전을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-132">Set the minimal TLS version for connections to server when SSL is enabled.</span></span>
<span data-ttu-id="388e7-133">기본값은 TLSEnforcementDisabled.accepted 값(TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled)입니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-133">Default is TLSEnforcementDisabled.accepted values: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span></span>

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

### <span data-ttu-id="388e7-134">-Name</span><span class="sxs-lookup"><span data-stu-id="388e7-134">-Name</span></span>
<span data-ttu-id="388e7-135">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-135">The name of the server.</span></span>

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

### <span data-ttu-id="388e7-136">-NoWait</span><span class="sxs-lookup"><span data-stu-id="388e7-136">-NoWait</span></span>
<span data-ttu-id="388e7-137">명령을 비동기적으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-137">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="388e7-138">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="388e7-138">-ReplicationRole</span></span>
<span data-ttu-id="388e7-139">서버의 복제 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-139">The replication role of the server.</span></span>

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

### <span data-ttu-id="388e7-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="388e7-140">-ResourceGroupName</span></span>
<span data-ttu-id="388e7-141">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-141">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="388e7-142">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-142">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="388e7-143">-Sku</span><span class="sxs-lookup"><span data-stu-id="388e7-143">-Sku</span></span>
<span data-ttu-id="388e7-144">SKU의 이름(일반적으로 계층 + 패밀리 + 코어)입니다(예: B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="388e7-144">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="388e7-145">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="388e7-145">-SkuCapacity</span></span>
<span data-ttu-id="388e7-146">서버의 컴퓨팅 단위를 나타내는 확장/확장 용량입니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-146">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="388e7-147">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="388e7-147">-SkuFamily</span></span>
<span data-ttu-id="388e7-148">하드웨어의 패밀리입니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-148">The family of hardware.</span></span>

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

### <span data-ttu-id="388e7-149">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="388e7-149">-SkuTier</span></span>
<span data-ttu-id="388e7-150">특정 SKU의 계층(예: 기본)</span><span class="sxs-lookup"><span data-stu-id="388e7-150">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="388e7-151">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="388e7-151">-SslEnforcement</span></span>
<span data-ttu-id="388e7-152">서버에 연결할 때 ssl 적용을 사용하도록 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-152">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="388e7-153">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="388e7-153">-StorageAutogrow</span></span>
<span data-ttu-id="388e7-154">저장소 자동 증가를 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="388e7-154">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="388e7-155">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="388e7-155">-StorageInMb</span></span>
<span data-ttu-id="388e7-156">서버에 허용되는 최대 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-156">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="388e7-157">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="388e7-157">-SubscriptionId</span></span>
<span data-ttu-id="388e7-158">Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-158">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="388e7-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="388e7-159">-Tag</span></span>
<span data-ttu-id="388e7-160">키-값 쌍의 형태로 애플리케이션별 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-160">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="388e7-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="388e7-161">-Confirm</span></span>
<span data-ttu-id="388e7-162">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="388e7-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="388e7-163">-WhatIf</span></span>
<span data-ttu-id="388e7-164">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="388e7-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="388e7-165">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="388e7-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="388e7-166">CommonParameters</span></span>
<span data-ttu-id="388e7-167">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="388e7-168">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="388e7-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="388e7-169">입력</span><span class="sxs-lookup"><span data-stu-id="388e7-169">INPUTS</span></span>

### <span data-ttu-id="388e7-170">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="388e7-170">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="388e7-171">출력</span><span class="sxs-lookup"><span data-stu-id="388e7-171">OUTPUTS</span></span>

### <span data-ttu-id="388e7-172">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="388e7-172">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="388e7-173">참고 사항</span><span class="sxs-lookup"><span data-stu-id="388e7-173">NOTES</span></span>

<span data-ttu-id="388e7-174">별칭</span><span class="sxs-lookup"><span data-stu-id="388e7-174">ALIASES</span></span>

<span data-ttu-id="388e7-175">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="388e7-175">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="388e7-176">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-176">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="388e7-177">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="388e7-177">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="388e7-178">INPUTOBJECT: <IMySqlIdentity> ID 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-178">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="388e7-179">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-179">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="388e7-180">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-180">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="388e7-181">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-181">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="388e7-182">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="388e7-182">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="388e7-183">`[KeyName <String>]`: 서버 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-183">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="388e7-184">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-184">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="388e7-185">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-185">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="388e7-186">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-186">The name is case insensitive.</span></span>
  - <span data-ttu-id="388e7-187">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-187">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="388e7-188">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-188">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="388e7-189">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-189">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="388e7-190">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-190">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="388e7-191">관련 링크</span><span class="sxs-lookup"><span data-stu-id="388e7-191">RELATED LINKS</span></span>

