---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
ms.openlocfilehash: e23cc8b942033805d8ed8cd122b19e6a59bf457c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217615"
---
# <span data-ttu-id="886ae-101">Update-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="886ae-101">Update-AzMySqlServer</span></span>

## <span data-ttu-id="886ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="886ae-102">SYNOPSIS</span></span>
<span data-ttu-id="886ae-103">기존 서버를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-103">Updates an existing server.</span></span>
<span data-ttu-id="886ae-104">요청 본문에는 일반 서버 정의에 있는 속성 중 상당수가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="886ae-105">Wait_timeout 또는 net_retry_count 등의 서버 매개 변수를 업데이트 하려면 대신 Update-AzMySqlConfiguration를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-105">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="886ae-106">구문과</span><span class="sxs-lookup"><span data-stu-id="886ae-106">SYNTAX</span></span>

### <span data-ttu-id="886ae-107">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="886ae-107">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="886ae-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="886ae-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlServer -InputObject <IMySqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-ReplicationRole <String>] [-Sku <String>] [-SkuCapacity <Int32>]
 [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="886ae-109">설명은</span><span class="sxs-lookup"><span data-stu-id="886ae-109">DESCRIPTION</span></span>
<span data-ttu-id="886ae-110">기존 서버를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-110">Updates an existing server.</span></span>
<span data-ttu-id="886ae-111">요청 본문에는 일반 서버 정의에 있는 속성 중 상당수가 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="886ae-112">Wait_timeout 또는 net_retry_count 등의 서버 매개 변수를 업데이트 하려면 대신 Update-AzMySqlConfiguration를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-112">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="886ae-113">예제의</span><span class="sxs-lookup"><span data-stu-id="886ae-113">EXAMPLES</span></span>

### <span data-ttu-id="886ae-114">예제 1: 리소스 그룹 및 서버 이름에 따라 MySql 서버 업데이트</span><span class="sxs-lookup"><span data-stu-id="886ae-114">Example 1: Update MySql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -SslEnforcement Disabled

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="886ae-115">이 cmdlet은 리소스 그룹 및 서버 이름에 따라 MySql 서버를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-115">This cmdlet updates MySql server by resource group and server name.</span></span>

### <span data-ttu-id="886ae-116">예제 2: id를 기준으로 MySql 서버 업데이트</span><span class="sxs-lookup"><span data-stu-id="886ae-116">Example 2: Update MySql server by identity.</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Update-AzMySqlServer -BackupRetentionDay 23 -StorageMb 10240

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="886ae-117">이 cmdlet은 id를 기준으로 MySql 서버를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-117">This cmdlet updates MySql server by identity.</span></span>

## <span data-ttu-id="886ae-118">변수</span><span class="sxs-lookup"><span data-stu-id="886ae-118">PARAMETERS</span></span>

### <span data-ttu-id="886ae-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="886ae-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="886ae-120">관리자 로그인의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="886ae-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="886ae-121">-AsJob</span></span>
<span data-ttu-id="886ae-122">명령을 작업으로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="886ae-123">-Backup보존 일정</span><span class="sxs-lookup"><span data-stu-id="886ae-123">-BackupRetentionDay</span></span>
<span data-ttu-id="886ae-124">서버에 대 한 백업 보존 일입니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-124">Backup retention days for the server.</span></span>
<span data-ttu-id="886ae-125">일 수는 7 ~ 35입니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="886ae-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="886ae-126">-DefaultProfile</span></span>
<span data-ttu-id="886ae-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="886ae-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="886ae-128">-InputObject</span></span>
<span data-ttu-id="886ae-129">Id 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-129">Identity Parameter.</span></span>
<span data-ttu-id="886ae-130">생성 하려면 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="886ae-131">-이름</span><span class="sxs-lookup"><span data-stu-id="886ae-131">-Name</span></span>
<span data-ttu-id="886ae-132">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-132">The name of the server.</span></span>

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

### <span data-ttu-id="886ae-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="886ae-133">-NoWait</span></span>
<span data-ttu-id="886ae-134">비동기적으로 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-134">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="886ae-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="886ae-135">-ReplicationRole</span></span>
<span data-ttu-id="886ae-136">서버의 복제 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="886ae-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="886ae-137">-ResourceGroupName</span></span>
<span data-ttu-id="886ae-138">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-138">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="886ae-139">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-139">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="886ae-140">-Sku</span><span class="sxs-lookup"><span data-stu-id="886ae-140">-Sku</span></span>
<span data-ttu-id="886ae-141">Sku (일반적으로 계층 + 패밀리 + 코어)의 이름 (예: B_Gen4_1 GP_Gen5_8)입니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-141">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="886ae-142">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="886ae-142">-SkuCapacity</span></span>
<span data-ttu-id="886ae-143">크기 조정 용량으로, 서버의 계산 단위를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-143">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="886ae-144">-용 U가족</span><span class="sxs-lookup"><span data-stu-id="886ae-144">-SkuFamily</span></span>
<span data-ttu-id="886ae-145">하드웨어 패밀리.</span><span class="sxs-lookup"><span data-stu-id="886ae-145">The family of hardware.</span></span>

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

### <span data-ttu-id="886ae-146">-서 고 U계층</span><span class="sxs-lookup"><span data-stu-id="886ae-146">-SkuTier</span></span>
<span data-ttu-id="886ae-147">특정 SKU (예: 기본)의 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-147">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="886ae-148">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="886ae-148">-SslEnforcement</span></span>
<span data-ttu-id="886ae-149">서버에 연결할 때 ssl 적용 여부를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-149">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="886ae-150">-StorageAutogrow 증가</span><span class="sxs-lookup"><span data-stu-id="886ae-150">-StorageAutogrow</span></span>
<span data-ttu-id="886ae-151">저장소 자동 증가를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-151">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="886ae-152">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="886ae-152">-StorageInMb</span></span>
<span data-ttu-id="886ae-153">서버에 허용 되는 최대 저장소.</span><span class="sxs-lookup"><span data-stu-id="886ae-153">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="886ae-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="886ae-154">-SubscriptionId</span></span>
<span data-ttu-id="886ae-155">Azure 구독을 식별 하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-155">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="886ae-156">태그</span><span class="sxs-lookup"><span data-stu-id="886ae-156">-Tag</span></span>
<span data-ttu-id="886ae-157">키-값 쌍의 형식으로 된 응용 프로그램 관련 메타 데이터</span><span class="sxs-lookup"><span data-stu-id="886ae-157">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="886ae-158">-확인</span><span class="sxs-lookup"><span data-stu-id="886ae-158">-Confirm</span></span>
<span data-ttu-id="886ae-159">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="886ae-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="886ae-160">-WhatIf</span></span>
<span data-ttu-id="886ae-161">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="886ae-162">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="886ae-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="886ae-163">CommonParameters</span></span>
<span data-ttu-id="886ae-164">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="886ae-165">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="886ae-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="886ae-166">입력</span><span class="sxs-lookup"><span data-stu-id="886ae-166">INPUTS</span></span>

### <span data-ttu-id="886ae-167">IMySqlIdentity (Microsoft. PowerShell)</span><span class="sxs-lookup"><span data-stu-id="886ae-167">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="886ae-168">출력</span><span class="sxs-lookup"><span data-stu-id="886ae-168">OUTPUTS</span></span>

### <span data-ttu-id="886ae-169">Api20171201 (Microsoft. i m/. i m/. i m/. 서버)</span><span class="sxs-lookup"><span data-stu-id="886ae-169">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="886ae-170">상속자</span><span class="sxs-lookup"><span data-stu-id="886ae-170">NOTES</span></span>

<span data-ttu-id="886ae-171">별칭과</span><span class="sxs-lookup"><span data-stu-id="886ae-171">ALIASES</span></span>

<span data-ttu-id="886ae-172">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="886ae-172">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="886ae-173">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-173">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="886ae-174">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="886ae-174">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="886ae-175">INPUTOBJECT <IMySqlIdentity> : Identity 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-175">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="886ae-176">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-176">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="886ae-177">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-177">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="886ae-178">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-178">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="886ae-179">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="886ae-179">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="886ae-180">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-180">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="886ae-181">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-181">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="886ae-182">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-182">The name is case insensitive.</span></span>
  - <span data-ttu-id="886ae-183">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-183">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="886ae-184">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-184">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="886ae-185">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-185">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="886ae-186">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="886ae-186">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="886ae-187">관련 링크</span><span class="sxs-lookup"><span data-stu-id="886ae-187">RELATED LINKS</span></span>

