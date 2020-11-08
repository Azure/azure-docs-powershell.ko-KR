---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
ms.openlocfilehash: 0a6286c7574a2bf7226f8d4b80a5cac62c535a47
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226808"
---
# <span data-ttu-id="68a31-101">Update-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="68a31-101">Update-AzMariaDbServer</span></span>

## <span data-ttu-id="68a31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68a31-102">SYNOPSIS</span></span>
<span data-ttu-id="68a31-103">기존 서버를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a31-103">Updates an existing server.</span></span>
<span data-ttu-id="68a31-104">요청 본문에는 일반 서버 정의에 있는 속성 중 상당수가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68a31-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="68a31-105">Wait_timeout 또는 net_retry_count 등의 서버 매개 변수를 업데이트 하려면 대신 Update-AzMariaDbConfiguration를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a31-105">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="68a31-106">구문과</span><span class="sxs-lookup"><span data-stu-id="68a31-106">SYNTAX</span></span>

### <span data-ttu-id="68a31-107">ServerName (기본값)</span><span class="sxs-lookup"><span data-stu-id="68a31-107">ServerName (Default)</span></span>
```
Update-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>] [-Sku <String>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="68a31-108">ServerObject</span><span class="sxs-lookup"><span data-stu-id="68a31-108">ServerObject</span></span>
```
Update-AzMariaDbServer -InputObject <IMariaDbIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>]
 [-Sku <String>] [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>]
 [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="68a31-109">설명은</span><span class="sxs-lookup"><span data-stu-id="68a31-109">DESCRIPTION</span></span>
<span data-ttu-id="68a31-110">기존 서버를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a31-110">Updates an existing server.</span></span>
<span data-ttu-id="68a31-111">요청 본문에는 일반 서버 정의에 있는 속성 중 상당수가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68a31-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="68a31-112">Wait_timeout 또는 net_retry_count 등의 서버 매개 변수를 업데이트 하려면 대신 Update-AzMariaDbConfiguration를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a31-112">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="68a31-113">예제의</span><span class="sxs-lookup"><span data-stu-id="68a31-113">EXAMPLES</span></span>

### <span data-ttu-id="68a31-114">예제 1:이을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a31-114">Example 1: Update MariaDB</span></span>
```powershell
PS C:\> Update-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StorageInMb 8192

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    8192                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="68a31-115">이 명령은을 (를) 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a31-115">This command updates a MariaDB.</span></span>

### <span data-ttu-id="68a31-116">예제 2: 업데이트 2 Iadb</span><span class="sxs-lookup"><span data-stu-id="68a31-116">Example 2: Update MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 | Update-AzMariaDbServer -StorageInMb (8192+1024)

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    9216                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="68a31-117">이 명령은을 (를) 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a31-117">This command updates a MariaDB.</span></span>

## <span data-ttu-id="68a31-118">변수</span><span class="sxs-lookup"><span data-stu-id="68a31-118">PARAMETERS</span></span>

### <span data-ttu-id="68a31-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="68a31-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="68a31-120">관리자 로그인의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="68a31-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="68a31-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="68a31-121">-AsJob</span></span>
<span data-ttu-id="68a31-122">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="68a31-122">Run the command as a job</span></span>

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

### <span data-ttu-id="68a31-123">-Backup보존 일정</span><span class="sxs-lookup"><span data-stu-id="68a31-123">-BackupRetentionDay</span></span>
<span data-ttu-id="68a31-124">서버에 대 한 백업 보존 일입니다.</span><span class="sxs-lookup"><span data-stu-id="68a31-124">Backup retention days for the server.</span></span>

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

### <span data-ttu-id="68a31-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68a31-125">-DefaultProfile</span></span>
<span data-ttu-id="68a31-126">region DefaultParameters Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="68a31-126">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68a31-127">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="68a31-127">-GeoRedundantBackup</span></span>
<span data-ttu-id="68a31-128">지역 중복을 사용 하거나 서버 백업에 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="68a31-128">Enable Geo-redundant or not for server backup.</span></span>

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

### <span data-ttu-id="68a31-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68a31-129">-InputObject</span></span>
<span data-ttu-id="68a31-130">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="68a31-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="68a31-131">-이름</span><span class="sxs-lookup"><span data-stu-id="68a31-131">-Name</span></span>
<span data-ttu-id="68a31-132">E 2 Iadb 서버 이름</span><span class="sxs-lookup"><span data-stu-id="68a31-132">MariaDB server name</span></span>

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

### <span data-ttu-id="68a31-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="68a31-133">-NoWait</span></span>
<span data-ttu-id="68a31-134">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="68a31-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="68a31-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="68a31-135">-ReplicationRole</span></span>
<span data-ttu-id="68a31-136">서버의 복제 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="68a31-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="68a31-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68a31-137">-ResourceGroupName</span></span>
<span data-ttu-id="68a31-138">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68a31-138">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="68a31-139">-Sku</span><span class="sxs-lookup"><span data-stu-id="68a31-139">-Sku</span></span>
<span data-ttu-id="68a31-140">Sku (일반적으로 계층 + 패밀리 + 코어)의 이름 (예: B_Gen4_1 GP_Gen5_8)입니다.</span><span class="sxs-lookup"><span data-stu-id="68a31-140">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="68a31-141">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="68a31-141">-SslEnforcement</span></span>
<span data-ttu-id="68a31-142">서버에 연결할 때 ssl 적용 여부를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a31-142">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="68a31-143">-StorageAutogrow 증가</span><span class="sxs-lookup"><span data-stu-id="68a31-143">-StorageAutogrow</span></span>
<span data-ttu-id="68a31-144">저장소 자동 증가를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a31-144">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="68a31-145">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="68a31-145">-StorageInMb</span></span>
<span data-ttu-id="68a31-146">서버에 허용 되는 최대 저장소.</span><span class="sxs-lookup"><span data-stu-id="68a31-146">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="68a31-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="68a31-147">-SubscriptionId</span></span>
<span data-ttu-id="68a31-148">구독 ID는 모든 서비스 통화에 대 한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="68a31-148">The subscription ID is part of the URI for every service call</span></span>

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

### <span data-ttu-id="68a31-149">태그</span><span class="sxs-lookup"><span data-stu-id="68a31-149">-Tag</span></span>
<span data-ttu-id="68a31-150">키-값 쌍의 형식으로 된 응용 프로그램 관련 메타 데이터</span><span class="sxs-lookup"><span data-stu-id="68a31-150">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="68a31-151">-확인</span><span class="sxs-lookup"><span data-stu-id="68a31-151">-Confirm</span></span>
<span data-ttu-id="68a31-152">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a31-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68a31-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68a31-153">-WhatIf</span></span>
<span data-ttu-id="68a31-154">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="68a31-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68a31-155">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="68a31-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68a31-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68a31-156">CommonParameters</span></span>
<span data-ttu-id="68a31-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a31-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68a31-158">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="68a31-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68a31-159">입력</span><span class="sxs-lookup"><span data-stu-id="68a31-159">INPUTS</span></span>

### <span data-ttu-id="68a31-160">IMariaDbIdentity (Microsoft. PowerShell. m b.</span><span class="sxs-lookup"><span data-stu-id="68a31-160">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="68a31-161">출력</span><span class="sxs-lookup"><span data-stu-id="68a31-161">OUTPUTS</span></span>

### <span data-ttu-id="68a31-162">Api20180601Preview Iadb. i r i. IServer</span><span class="sxs-lookup"><span data-stu-id="68a31-162">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="68a31-163">상속자</span><span class="sxs-lookup"><span data-stu-id="68a31-163">NOTES</span></span>

<span data-ttu-id="68a31-164">별칭과</span><span class="sxs-lookup"><span data-stu-id="68a31-164">ALIASES</span></span>

<span data-ttu-id="68a31-165">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="68a31-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="68a31-166">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="68a31-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="68a31-167">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="68a31-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="68a31-168">INPUTOBJECT <IMariaDbIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="68a31-168">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="68a31-169">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68a31-169">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="68a31-170">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68a31-170">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="68a31-171">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68a31-171">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="68a31-172">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="68a31-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="68a31-173">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68a31-173">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="68a31-174">`[ResourceGroupName <String>]`: 리소스를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68a31-174">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="68a31-175">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68a31-175">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="68a31-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68a31-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="68a31-177">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68a31-177">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="68a31-178">`[SubscriptionId <String>]`: Azure 구독을 식별 하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="68a31-178">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="68a31-179">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68a31-179">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="68a31-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68a31-180">RELATED LINKS</span></span>

