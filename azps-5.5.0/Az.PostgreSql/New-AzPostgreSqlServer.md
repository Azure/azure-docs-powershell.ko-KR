---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlServer.md
ms.openlocfilehash: ed7b8e9db63adb92af6aaae1f780fd1aca7f0022
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193129"
---
# <span data-ttu-id="175a6-101">New-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="175a6-101">New-AzPostgreSqlServer</span></span>

## <span data-ttu-id="175a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="175a6-102">SYNOPSIS</span></span>
<span data-ttu-id="175a6-103">새 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="175a6-103">Creates a new server.</span></span>

## <span data-ttu-id="175a6-104">구문</span><span class="sxs-lookup"><span data-stu-id="175a6-104">SYNTAX</span></span>

```
New-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUserName <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-Version <ServerVersion>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="175a6-105">설명</span><span class="sxs-lookup"><span data-stu-id="175a6-105">DESCRIPTION</span></span>
<span data-ttu-id="175a6-106">새 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="175a6-106">Creates a new server.</span></span>

## <span data-ttu-id="175a6-107">예제</span><span class="sxs-lookup"><span data-stu-id="175a6-107">EXAMPLES</span></span>

### <span data-ttu-id="175a6-108">예제 1: 새 PostgreSql 서버 만들기</span><span class="sxs-lookup"><span data-stu-id="175a6-108">Example 1: Create a new PostgreSql server</span></span>
```powershell
PS C:\> New-AzPostgreSqlServer -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG -Location eastus -AdministratorUserName pwsh -AdministratorLoginPassword $password -Sku GP_Gen5_4

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="175a6-109">이러한 cmdlet은 새 PostgreSql 서버를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="175a6-109">These cmdlets create a new PostgreSql server.</span></span>

## <span data-ttu-id="175a6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="175a6-110">PARAMETERS</span></span>

### <span data-ttu-id="175a6-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="175a6-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="175a6-112">관리자의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="175a6-112">The password of the administrator.</span></span>
<span data-ttu-id="175a6-113">최소 8자 및 최대 128자입니다.</span><span class="sxs-lookup"><span data-stu-id="175a6-113">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="175a6-114">암호는 영어 대문자, 영어 소문자, 숫자 및 영문자 이 세 가지 범주의 문자를 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="175a6-114">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="175a6-115">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="175a6-115">-AdministratorUserName</span></span>
<span data-ttu-id="175a6-116">서버에 대한 관리자 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="175a6-116">Administrator username for the server.</span></span>
<span data-ttu-id="175a6-117">설정하면 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="175a6-117">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="175a6-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="175a6-118">-AsJob</span></span>
<span data-ttu-id="175a6-119">명령을 작업으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="175a6-119">Run the command as a job.</span></span>

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

### <span data-ttu-id="175a6-120">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="175a6-120">-BackupRetentionDay</span></span>
<span data-ttu-id="175a6-121">서버에 대한 백업 보존 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="175a6-121">Backup retention days for the server.</span></span>
<span data-ttu-id="175a6-122">일 수는 7에서 35 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="175a6-122">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="175a6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="175a6-123">-DefaultProfile</span></span>
<span data-ttu-id="175a6-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="175a6-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="175a6-125">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="175a6-125">-GeoRedundantBackup</span></span>
<span data-ttu-id="175a6-126">서버 백업에 지역 중복을 사용하도록 설정하거나 사용하도록 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="175a6-126">Enable Geo-redundant or not for server backup.</span></span>

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

### <span data-ttu-id="175a6-127">-Location</span><span class="sxs-lookup"><span data-stu-id="175a6-127">-Location</span></span>
<span data-ttu-id="175a6-128">리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="175a6-128">The location the resource resides in.</span></span>

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

### <span data-ttu-id="175a6-129">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="175a6-129">-MinimalTlsVersion</span></span>
<span data-ttu-id="175a6-130">SSL을 사용할 때 서버에 연결하기 위한 최소 TLS 버전을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="175a6-130">Set the minimal TLS version for connections to server when SSL is enabled.</span></span>
<span data-ttu-id="175a6-131">기본값은 TLSEnforcementDisabled.accepted 값(TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled)입니다.</span><span class="sxs-lookup"><span data-stu-id="175a6-131">Default is TLSEnforcementDisabled.accepted values: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span></span>

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

### <span data-ttu-id="175a6-132">-Name</span><span class="sxs-lookup"><span data-stu-id="175a6-132">-Name</span></span>
<span data-ttu-id="175a6-133">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="175a6-133">The name of the server.</span></span>

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

### <span data-ttu-id="175a6-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="175a6-134">-NoWait</span></span>
<span data-ttu-id="175a6-135">명령을 비동기적으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="175a6-135">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="175a6-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="175a6-136">-ResourceGroupName</span></span>
<span data-ttu-id="175a6-137">리소스가 포함된 리소스 그룹의 이름입니다. Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="175a6-137">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="175a6-138">-Sku</span><span class="sxs-lookup"><span data-stu-id="175a6-138">-Sku</span></span>
<span data-ttu-id="175a6-139">SKU의 이름(일반적으로 계층 + 패밀리 + 코어)입니다(예: B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="175a6-139">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="175a6-140">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="175a6-140">-SslEnforcement</span></span>
<span data-ttu-id="175a6-141">서버에 연결할 때 ssl 적용을 사용하도록 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="175a6-141">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="175a6-142">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="175a6-142">-StorageAutogrow</span></span>
<span data-ttu-id="175a6-143">저장소 자동 증가를 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="175a6-143">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="175a6-144">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="175a6-144">-StorageInMb</span></span>
<span data-ttu-id="175a6-145">서버에 허용되는 최대 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="175a6-145">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="175a6-146">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="175a6-146">-SubscriptionId</span></span>
<span data-ttu-id="175a6-147">Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="175a6-147">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="175a6-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="175a6-148">-Tag</span></span>
<span data-ttu-id="175a6-149">키-값 쌍의 형태로 애플리케이션별 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="175a6-149">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="175a6-150">-Version</span><span class="sxs-lookup"><span data-stu-id="175a6-150">-Version</span></span>
<span data-ttu-id="175a6-151">서버 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="175a6-151">Server version.</span></span>

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

### <span data-ttu-id="175a6-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="175a6-152">-Confirm</span></span>
<span data-ttu-id="175a6-153">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="175a6-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="175a6-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="175a6-154">-WhatIf</span></span>
<span data-ttu-id="175a6-155">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="175a6-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="175a6-156">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="175a6-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="175a6-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="175a6-157">CommonParameters</span></span>
<span data-ttu-id="175a6-158">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="175a6-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="175a6-159">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="175a6-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="175a6-160">입력</span><span class="sxs-lookup"><span data-stu-id="175a6-160">INPUTS</span></span>

## <span data-ttu-id="175a6-161">출력</span><span class="sxs-lookup"><span data-stu-id="175a6-161">OUTPUTS</span></span>

### <span data-ttu-id="175a6-162">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="175a6-162">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="175a6-163">참고 사항</span><span class="sxs-lookup"><span data-stu-id="175a6-163">NOTES</span></span>

<span data-ttu-id="175a6-164">별칭</span><span class="sxs-lookup"><span data-stu-id="175a6-164">ALIASES</span></span>

## <span data-ttu-id="175a6-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="175a6-165">RELATED LINKS</span></span>

