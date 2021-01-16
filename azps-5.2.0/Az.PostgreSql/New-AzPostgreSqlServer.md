---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlServer.md
ms.openlocfilehash: cf9fbcdb665d3149ed4fcffe61c8c671bf8368ce
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331214"
---
# <span data-ttu-id="37e77-101">New-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="37e77-101">New-AzPostgreSqlServer</span></span>

## <span data-ttu-id="37e77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37e77-102">SYNOPSIS</span></span>
<span data-ttu-id="37e77-103">새 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="37e77-103">Creates a new server.</span></span>

## <span data-ttu-id="37e77-104">구문</span><span class="sxs-lookup"><span data-stu-id="37e77-104">SYNTAX</span></span>

```
New-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUserName <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="37e77-105">설명</span><span class="sxs-lookup"><span data-stu-id="37e77-105">DESCRIPTION</span></span>
<span data-ttu-id="37e77-106">새 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="37e77-106">Creates a new server.</span></span>

## <span data-ttu-id="37e77-107">예제</span><span class="sxs-lookup"><span data-stu-id="37e77-107">EXAMPLES</span></span>

### <span data-ttu-id="37e77-108">예제 1: 새 PostgreSql 서버 만들기</span><span class="sxs-lookup"><span data-stu-id="37e77-108">Example 1: Create a new PostgreSql server</span></span>
```powershell
PS C:\> New-AzPostgreSqlServer -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG -Location eastus -AdministratorUserName pwsh -AdministratorLoginPassword $password -Sku GP_Gen5_4

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="37e77-109">이러한 cmdlet은 새 PostgreSql 서버를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="37e77-109">These cmdlets create a new PostgreSql server.</span></span>

## <span data-ttu-id="37e77-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37e77-110">PARAMETERS</span></span>

### <span data-ttu-id="37e77-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="37e77-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="37e77-112">리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="37e77-112">The location the resource resides in.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37e77-113">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="37e77-113">-AdministratorUserName</span></span>
<span data-ttu-id="37e77-114">리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="37e77-114">The location the resource resides in.</span></span>

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

### <span data-ttu-id="37e77-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37e77-115">-AsJob</span></span>
<span data-ttu-id="37e77-116">명령을 작업으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="37e77-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="37e77-117">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="37e77-117">-BackupRetentionDay</span></span>
<span data-ttu-id="37e77-118">서버에 대한 백업 보존 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="37e77-118">Backup retention days for the server.</span></span>
<span data-ttu-id="37e77-119">일 수는 7에서 35 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="37e77-119">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="37e77-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37e77-120">-DefaultProfile</span></span>
<span data-ttu-id="37e77-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="37e77-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37e77-122">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="37e77-122">-GeoRedundantBackup</span></span>
<span data-ttu-id="37e77-123">서버 백업에 지역 중복을 사용하도록 설정하거나 사용하도록 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37e77-123">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37e77-124">-Location</span><span class="sxs-lookup"><span data-stu-id="37e77-124">-Location</span></span>
<span data-ttu-id="37e77-125">리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="37e77-125">The location the resource resides in.</span></span>

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

### <span data-ttu-id="37e77-126">-Name</span><span class="sxs-lookup"><span data-stu-id="37e77-126">-Name</span></span>
<span data-ttu-id="37e77-127">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37e77-127">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37e77-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="37e77-128">-NoWait</span></span>
<span data-ttu-id="37e77-129">명령을 비동기적으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="37e77-129">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="37e77-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37e77-130">-ResourceGroupName</span></span>
<span data-ttu-id="37e77-131">리소스가 포함된 리소스 그룹의 이름입니다. Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37e77-131">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="37e77-132">-Sku</span><span class="sxs-lookup"><span data-stu-id="37e77-132">-Sku</span></span>
<span data-ttu-id="37e77-133">SKU의 이름(일반적으로 계층 + 패밀리 + 코어)입니다(예: B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="37e77-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="37e77-134">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="37e77-134">-SslEnforcement</span></span>
<span data-ttu-id="37e77-135">서버에 연결할 때 ssl 적용을 사용하도록 설정하거나 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37e77-135">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="37e77-136">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="37e77-136">-StorageAutogrow</span></span>
<span data-ttu-id="37e77-137">저장소 자동 증가를 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="37e77-137">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="37e77-138">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="37e77-138">-StorageInMb</span></span>
<span data-ttu-id="37e77-139">서버에 허용되는 최대 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="37e77-139">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="37e77-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="37e77-140">-SubscriptionId</span></span>
<span data-ttu-id="37e77-141">Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="37e77-141">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="37e77-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="37e77-142">-Tag</span></span>
<span data-ttu-id="37e77-143">키-값 쌍의 형태로 애플리케이션별 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="37e77-143">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="37e77-144">-Version</span><span class="sxs-lookup"><span data-stu-id="37e77-144">-Version</span></span>
<span data-ttu-id="37e77-145">서버 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="37e77-145">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37e77-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37e77-146">-Confirm</span></span>
<span data-ttu-id="37e77-147">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="37e77-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37e77-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37e77-148">-WhatIf</span></span>
<span data-ttu-id="37e77-149">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="37e77-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37e77-150">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37e77-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37e77-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37e77-151">CommonParameters</span></span>
<span data-ttu-id="37e77-152">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="37e77-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37e77-153">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="37e77-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37e77-154">입력</span><span class="sxs-lookup"><span data-stu-id="37e77-154">INPUTS</span></span>

## <span data-ttu-id="37e77-155">출력</span><span class="sxs-lookup"><span data-stu-id="37e77-155">OUTPUTS</span></span>

### <span data-ttu-id="37e77-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="37e77-156">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="37e77-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="37e77-157">NOTES</span></span>

<span data-ttu-id="37e77-158">별칭</span><span class="sxs-lookup"><span data-stu-id="37e77-158">ALIASES</span></span>

## <span data-ttu-id="37e77-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="37e77-159">RELATED LINKS</span></span>

