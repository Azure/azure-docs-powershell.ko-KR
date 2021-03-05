---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/update-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
ms.openlocfilehash: 0db4d25f224f1c6984ba9b57184859e8fa2c6c28
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003867"
---
# <span data-ttu-id="140a6-101">Update-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="140a6-101">Update-AzMariaDbServer</span></span>

## <span data-ttu-id="140a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="140a6-102">SYNOPSIS</span></span>
<span data-ttu-id="140a6-103">기존 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="140a6-103">Updates an existing server.</span></span>
<span data-ttu-id="140a6-104">요청 본문에는 일반 서버 정의에 있는 속성 중 하나에서 많은 속성이 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="140a6-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="140a6-105">서버 Update-AzMariaDbConfiguration 서버 매개 변수를 업데이트하려는 경우 대신 wait_timeout net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="140a6-105">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="140a6-106">구문</span><span class="sxs-lookup"><span data-stu-id="140a6-106">SYNTAX</span></span>

### <span data-ttu-id="140a6-107">ServerName(기본값)</span><span class="sxs-lookup"><span data-stu-id="140a6-107">ServerName (Default)</span></span>
```
Update-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>] [-Sku <String>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="140a6-108">ServerObject</span><span class="sxs-lookup"><span data-stu-id="140a6-108">ServerObject</span></span>
```
Update-AzMariaDbServer -InputObject <IMariaDbIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>]
 [-Sku <String>] [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>]
 [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="140a6-109">설명</span><span class="sxs-lookup"><span data-stu-id="140a6-109">DESCRIPTION</span></span>
<span data-ttu-id="140a6-110">기존 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="140a6-110">Updates an existing server.</span></span>
<span data-ttu-id="140a6-111">요청 본문에는 일반 서버 정의에 있는 속성 중 하나에서 많은 속성이 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="140a6-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="140a6-112">서버 Update-AzMariaDbConfiguration 서버 매개 변수를 업데이트하려는 경우 대신 wait_timeout net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="140a6-112">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="140a6-113">예제</span><span class="sxs-lookup"><span data-stu-id="140a6-113">EXAMPLES</span></span>

### <span data-ttu-id="140a6-114">예제 1: MariaDB 업데이트</span><span class="sxs-lookup"><span data-stu-id="140a6-114">Example 1: Update MariaDB</span></span>
```powershell
PS C:\> Update-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StorageInMb 8192

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    8192                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="140a6-115">이 명령은 MariaDB를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="140a6-115">This command updates a MariaDB.</span></span>

### <span data-ttu-id="140a6-116">예제 2: MariaDB 업데이트</span><span class="sxs-lookup"><span data-stu-id="140a6-116">Example 2: Update MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 | Update-AzMariaDbServer -StorageInMb (8192+1024)

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    9216                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="140a6-117">이 명령은 MariaDB를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="140a6-117">This command updates a MariaDB.</span></span>

## <span data-ttu-id="140a6-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="140a6-118">PARAMETERS</span></span>

### <span data-ttu-id="140a6-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="140a6-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="140a6-120">관리자 로그인의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="140a6-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="140a6-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="140a6-121">-AsJob</span></span>
<span data-ttu-id="140a6-122">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="140a6-122">Run the command as a job</span></span>

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

### <span data-ttu-id="140a6-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="140a6-123">-BackupRetentionDay</span></span>
<span data-ttu-id="140a6-124">서버에 대한 백업 보존 일입니다.</span><span class="sxs-lookup"><span data-stu-id="140a6-124">Backup retention days for the server.</span></span>

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

### <span data-ttu-id="140a6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="140a6-125">-DefaultProfile</span></span>
<span data-ttu-id="140a6-126">region DefaultParameters Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="140a6-126">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="140a6-127">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="140a6-127">-GeoRedundantBackup</span></span>
<span data-ttu-id="140a6-128">서버 백업에 대해 지역 중복을 사용하도록 설정하거나 사용 안 하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="140a6-128">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="140a6-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="140a6-129">-InputObject</span></span>
<span data-ttu-id="140a6-130">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="140a6-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: ServerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="140a6-131">-Name</span><span class="sxs-lookup"><span data-stu-id="140a6-131">-Name</span></span>
<span data-ttu-id="140a6-132">MariaDB 서버 이름</span><span class="sxs-lookup"><span data-stu-id="140a6-132">MariaDB server name</span></span>

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

### <span data-ttu-id="140a6-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="140a6-133">-NoWait</span></span>
<span data-ttu-id="140a6-134">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="140a6-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="140a6-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="140a6-135">-ReplicationRole</span></span>
<span data-ttu-id="140a6-136">서버의 복제 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="140a6-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="140a6-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="140a6-137">-ResourceGroupName</span></span>
<span data-ttu-id="140a6-138">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="140a6-138">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="140a6-139">-Sku</span><span class="sxs-lookup"><span data-stu-id="140a6-139">-Sku</span></span>
<span data-ttu-id="140a6-140">sku의 이름은 일반적으로 계층 + 패밀리 + 코어(예: B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="140a6-140">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="140a6-141">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="140a6-141">-SslEnforcement</span></span>
<span data-ttu-id="140a6-142">서버에 연결할 때 ssl 적용을 사용하도록 설정하거나 활성화하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="140a6-142">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="140a6-143">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="140a6-143">-StorageAutogrow</span></span>
<span data-ttu-id="140a6-144">저장소 자동 증가를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="140a6-144">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="140a6-145">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="140a6-145">-StorageInMb</span></span>
<span data-ttu-id="140a6-146">서버에 대해 허용되는 최대 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="140a6-146">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="140a6-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="140a6-147">-SubscriptionId</span></span>
<span data-ttu-id="140a6-148">구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="140a6-148">The subscription ID is part of the URI for every service call</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="140a6-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="140a6-149">-Tag</span></span>
<span data-ttu-id="140a6-150">키-값 쌍의 형태로 애플리케이션별 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="140a6-150">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="140a6-151">-확인</span><span class="sxs-lookup"><span data-stu-id="140a6-151">-Confirm</span></span>
<span data-ttu-id="140a6-152">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="140a6-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="140a6-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="140a6-153">-WhatIf</span></span>
<span data-ttu-id="140a6-154">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="140a6-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="140a6-155">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="140a6-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="140a6-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="140a6-156">CommonParameters</span></span>
<span data-ttu-id="140a6-157">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="140a6-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="140a6-158">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="140a6-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="140a6-159">입력</span><span class="sxs-lookup"><span data-stu-id="140a6-159">INPUTS</span></span>

### <span data-ttu-id="140a6-160">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="140a6-160">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="140a6-161">출력</span><span class="sxs-lookup"><span data-stu-id="140a6-161">OUTPUTS</span></span>

### <span data-ttu-id="140a6-162">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="140a6-162">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="140a6-163">참고 사항</span><span class="sxs-lookup"><span data-stu-id="140a6-163">NOTES</span></span>

<span data-ttu-id="140a6-164">별칭</span><span class="sxs-lookup"><span data-stu-id="140a6-164">ALIASES</span></span>

<span data-ttu-id="140a6-165">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="140a6-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="140a6-166">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="140a6-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="140a6-167">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="140a6-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="140a6-168">INPUTOBJECT <IMariaDbIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="140a6-168">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="140a6-169">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="140a6-169">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="140a6-170">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="140a6-170">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="140a6-171">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="140a6-171">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="140a6-172">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="140a6-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="140a6-173">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="140a6-173">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="140a6-174">`[ResourceGroupName <String>]`: 리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="140a6-174">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="140a6-175">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="140a6-175">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="140a6-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="140a6-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="140a6-177">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="140a6-177">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="140a6-178">`[SubscriptionId <String>]`: Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="140a6-178">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="140a6-179">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="140a6-179">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="140a6-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="140a6-180">RELATED LINKS</span></span>

