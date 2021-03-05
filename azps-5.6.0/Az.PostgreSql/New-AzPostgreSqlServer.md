---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/new-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlServer.md
ms.openlocfilehash: 71aa5886035164dee5b011be8a90b18e33e055e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987681"
---
# <span data-ttu-id="b959e-101">New-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="b959e-101">New-AzPostgreSqlServer</span></span>

## <span data-ttu-id="b959e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b959e-102">SYNOPSIS</span></span>
<span data-ttu-id="b959e-103">새 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b959e-103">Creates a new server.</span></span>

## <span data-ttu-id="b959e-104">구문</span><span class="sxs-lookup"><span data-stu-id="b959e-104">SYNTAX</span></span>

```
New-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUserName <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-Version <ServerVersion>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b959e-105">설명</span><span class="sxs-lookup"><span data-stu-id="b959e-105">DESCRIPTION</span></span>
<span data-ttu-id="b959e-106">새 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b959e-106">Creates a new server.</span></span>

## <span data-ttu-id="b959e-107">예제</span><span class="sxs-lookup"><span data-stu-id="b959e-107">EXAMPLES</span></span>

### <span data-ttu-id="b959e-108">예제 1: 새 PostgreSql 서버 만들기</span><span class="sxs-lookup"><span data-stu-id="b959e-108">Example 1: Create a new PostgreSql server</span></span>
```powershell
PS C:\> New-AzPostgreSqlServer -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG -Location eastus -AdministratorUserName pwsh -AdministratorLoginPassword $password -Sku GP_Gen5_4

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="b959e-109">이러한 cmdlet은 새 PostgreSql 서버를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b959e-109">These cmdlets create a new PostgreSql server.</span></span>

## <span data-ttu-id="b959e-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b959e-110">PARAMETERS</span></span>

### <span data-ttu-id="b959e-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="b959e-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="b959e-112">관리자의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="b959e-112">The password of the administrator.</span></span>
<span data-ttu-id="b959e-113">최소 8자, 최대 128자</span><span class="sxs-lookup"><span data-stu-id="b959e-113">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="b959e-114">암호에는 영어 대문자, 영어 소문자, 숫자 및 영자 문자가 아닌 세 가지 범주의 문자가 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b959e-114">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="b959e-115">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="b959e-115">-AdministratorUserName</span></span>
<span data-ttu-id="b959e-116">서버에 대한 관리자 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b959e-116">Administrator username for the server.</span></span>
<span data-ttu-id="b959e-117">설정하면 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b959e-117">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="b959e-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b959e-118">-AsJob</span></span>
<span data-ttu-id="b959e-119">명령을 작업으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="b959e-119">Run the command as a job.</span></span>

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

### <span data-ttu-id="b959e-120">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="b959e-120">-BackupRetentionDay</span></span>
<span data-ttu-id="b959e-121">서버에 대한 백업 보존 일입니다.</span><span class="sxs-lookup"><span data-stu-id="b959e-121">Backup retention days for the server.</span></span>
<span data-ttu-id="b959e-122">일 수는 7에서 35 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="b959e-122">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="b959e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b959e-123">-DefaultProfile</span></span>
<span data-ttu-id="b959e-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b959e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b959e-125">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="b959e-125">-GeoRedundantBackup</span></span>
<span data-ttu-id="b959e-126">서버 백업에 대해 지역 중복을 사용하도록 설정하거나 사용 안 하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b959e-126">Enable Geo-redundant or not for server backup.</span></span>

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

### <span data-ttu-id="b959e-127">-Location</span><span class="sxs-lookup"><span data-stu-id="b959e-127">-Location</span></span>
<span data-ttu-id="b959e-128">리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b959e-128">The location the resource resides in.</span></span>

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

### <span data-ttu-id="b959e-129">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="b959e-129">-MinimalTlsVersion</span></span>
<span data-ttu-id="b959e-130">SSL을 사용하도록 설정하면 서버에 대한 연결에 대한 최소 TLS 버전을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b959e-130">Set the minimal TLS version for connections to server when SSL is enabled.</span></span>
<span data-ttu-id="b959e-131">기본값은 TLSEnforcementDisabled.accepted 값입니다. TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled입니다.</span><span class="sxs-lookup"><span data-stu-id="b959e-131">Default is TLSEnforcementDisabled.accepted values: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span></span>

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

### <span data-ttu-id="b959e-132">-Name</span><span class="sxs-lookup"><span data-stu-id="b959e-132">-Name</span></span>
<span data-ttu-id="b959e-133">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b959e-133">The name of the server.</span></span>

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

### <span data-ttu-id="b959e-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b959e-134">-NoWait</span></span>
<span data-ttu-id="b959e-135">명령을 비동기적으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="b959e-135">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="b959e-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b959e-136">-ResourceGroupName</span></span>
<span data-ttu-id="b959e-137">리소스를 포함하는 리소스 그룹의 이름, Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b959e-137">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b959e-138">-Sku</span><span class="sxs-lookup"><span data-stu-id="b959e-138">-Sku</span></span>
<span data-ttu-id="b959e-139">sku의 이름은 일반적으로 계층 + 패밀리 + 코어(예: B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="b959e-139">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="b959e-140">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="b959e-140">-SslEnforcement</span></span>
<span data-ttu-id="b959e-141">서버에 연결할 때 ssl 적용을 사용하도록 설정하거나 활성화하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b959e-141">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="b959e-142">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="b959e-142">-StorageAutogrow</span></span>
<span data-ttu-id="b959e-143">저장소 자동 증가를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b959e-143">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="b959e-144">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="b959e-144">-StorageInMb</span></span>
<span data-ttu-id="b959e-145">서버에 대해 허용되는 최대 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="b959e-145">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="b959e-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b959e-146">-SubscriptionId</span></span>
<span data-ttu-id="b959e-147">Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b959e-147">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="b959e-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="b959e-148">-Tag</span></span>
<span data-ttu-id="b959e-149">키-값 쌍의 형태로 애플리케이션별 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="b959e-149">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="b959e-150">-Version</span><span class="sxs-lookup"><span data-stu-id="b959e-150">-Version</span></span>
<span data-ttu-id="b959e-151">서버 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="b959e-151">Server version.</span></span>

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

### <span data-ttu-id="b959e-152">-확인</span><span class="sxs-lookup"><span data-stu-id="b959e-152">-Confirm</span></span>
<span data-ttu-id="b959e-153">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b959e-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b959e-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b959e-154">-WhatIf</span></span>
<span data-ttu-id="b959e-155">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b959e-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b959e-156">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b959e-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b959e-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b959e-157">CommonParameters</span></span>
<span data-ttu-id="b959e-158">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b959e-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b959e-159">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b959e-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b959e-160">입력</span><span class="sxs-lookup"><span data-stu-id="b959e-160">INPUTS</span></span>

## <span data-ttu-id="b959e-161">출력</span><span class="sxs-lookup"><span data-stu-id="b959e-161">OUTPUTS</span></span>

### <span data-ttu-id="b959e-162">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="b959e-162">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="b959e-163">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b959e-163">NOTES</span></span>

<span data-ttu-id="b959e-164">별칭</span><span class="sxs-lookup"><span data-stu-id="b959e-164">ALIASES</span></span>

## <span data-ttu-id="b959e-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b959e-165">RELATED LINKS</span></span>

