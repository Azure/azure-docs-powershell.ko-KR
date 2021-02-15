---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbServer.md
ms.openlocfilehash: e6416fd67091fc86a5fe9844d3b1d366aaa6cb58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207189"
---
# <span data-ttu-id="bd28c-101">New-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="bd28c-101">New-AzMariaDbServer</span></span>

## <span data-ttu-id="bd28c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd28c-102">SYNOPSIS</span></span>
<span data-ttu-id="bd28c-103">새 MariaDB를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bd28c-103">Creates a new MariaDB.</span></span>

## <span data-ttu-id="bd28c-104">구문</span><span class="sxs-lookup"><span data-stu-id="bd28c-104">SYNTAX</span></span>

```
New-AzMariaDbServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUsername <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bd28c-105">설명</span><span class="sxs-lookup"><span data-stu-id="bd28c-105">DESCRIPTION</span></span>
<span data-ttu-id="bd28c-106">새 MariaDB를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bd28c-106">Creates a new MariaDB.</span></span>

## <span data-ttu-id="bd28c-107">예제</span><span class="sxs-lookup"><span data-stu-id="bd28c-107">EXAMPLES</span></span>

### <span data-ttu-id="bd28c-108">예제 1: 새 MariaDB 만들기</span><span class="sxs-lookup"><span data-stu-id="bd28c-108">Example 1: Create a new MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbServer -Name mariadb-aassd-01 -ResourceGroupName lucas-manual-test -Sku 'B_Gen5_1' -Location eastus
cmdlet New-AzMariaDbServer at command pipeline position 1
Supply values for the following parameters:
AdministratorUsername: adminuser
AdministratorLoginPassword: ************

Name             Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----             -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-aassd-01 eastus   adminuser          10.2    5120                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="bd28c-109">이 명령은 새 MariaDB를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bd28c-109">This command creates a new MariaDB.</span></span>

## <span data-ttu-id="bd28c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd28c-110">PARAMETERS</span></span>

### <span data-ttu-id="bd28c-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="bd28c-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="bd28c-112">관리자의 암호는 SecureString입니다.</span><span class="sxs-lookup"><span data-stu-id="bd28c-112">Password of administrator, should be SecureString.</span></span>

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

### <span data-ttu-id="bd28c-113">-AdministratorUsername</span><span class="sxs-lookup"><span data-stu-id="bd28c-113">-AdministratorUsername</span></span>
<span data-ttu-id="bd28c-114">관리자의 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bd28c-114">Username of administrator.</span></span>

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

### <span data-ttu-id="bd28c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bd28c-115">-AsJob</span></span>
<span data-ttu-id="bd28c-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="bd28c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="bd28c-117">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="bd28c-117">-BackupRetentionDay</span></span>
<span data-ttu-id="bd28c-118">서버에 대한 백업 보존 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="bd28c-118">Backup retention days for the server.</span></span>

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

### <span data-ttu-id="bd28c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd28c-119">-DefaultProfile</span></span>
<span data-ttu-id="bd28c-120">region DefaultParameters Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bd28c-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd28c-121">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="bd28c-121">-GeoRedundantBackup</span></span>
<span data-ttu-id="bd28c-122">서버 백업에 지역 중복을 사용하도록 설정하거나 사용하도록 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bd28c-122">Enable Geo-redundant or not for server backup.</span></span>

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

### <span data-ttu-id="bd28c-123">-Location</span><span class="sxs-lookup"><span data-stu-id="bd28c-123">-Location</span></span>
<span data-ttu-id="bd28c-124">리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="bd28c-124">The location the resource resides in.</span></span>

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

### <span data-ttu-id="bd28c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="bd28c-125">-Name</span></span>
<span data-ttu-id="bd28c-126">MariaDB 서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bd28c-126">MariaDB server name.</span></span>

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

### <span data-ttu-id="bd28c-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bd28c-127">-NoWait</span></span>
<span data-ttu-id="bd28c-128">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="bd28c-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bd28c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd28c-129">-ResourceGroupName</span></span>
<span data-ttu-id="bd28c-130">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bd28c-130">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="bd28c-131">-Sku</span><span class="sxs-lookup"><span data-stu-id="bd28c-131">-Sku</span></span>
<span data-ttu-id="bd28c-132">SKU의 이름(일반적으로 계층 + 패밀리 + 코어)입니다(예: B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="bd28c-132">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="bd28c-133">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="bd28c-133">-SslEnforcement</span></span>
<span data-ttu-id="bd28c-134">서버에 연결할 때 ssl 적용을 사용하도록 설정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bd28c-134">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="bd28c-135">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="bd28c-135">-StorageAutogrow</span></span>
<span data-ttu-id="bd28c-136">저장소 자동 증가를 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="bd28c-136">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="bd28c-137">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="bd28c-137">-StorageInMb</span></span>
<span data-ttu-id="bd28c-138">서버에 허용되는 최대 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="bd28c-138">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="bd28c-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bd28c-139">-SubscriptionId</span></span>
<span data-ttu-id="bd28c-140">구독 ID는 모든 서비스 호출에 대한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="bd28c-140">The subscription ID is part of the URI for every service call</span></span>

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

### <span data-ttu-id="bd28c-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="bd28c-141">-Tag</span></span>
<span data-ttu-id="bd28c-142">키-값 쌍의 형태로 애플리케이션별 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="bd28c-142">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="bd28c-143">-Version</span><span class="sxs-lookup"><span data-stu-id="bd28c-143">-Version</span></span>
<span data-ttu-id="bd28c-144">서버 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="bd28c-144">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd28c-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd28c-145">-Confirm</span></span>
<span data-ttu-id="bd28c-146">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd28c-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd28c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd28c-147">-WhatIf</span></span>
<span data-ttu-id="bd28c-148">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="bd28c-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd28c-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bd28c-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd28c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd28c-150">CommonParameters</span></span>
<span data-ttu-id="bd28c-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bd28c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd28c-152">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bd28c-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd28c-153">입력</span><span class="sxs-lookup"><span data-stu-id="bd28c-153">INPUTS</span></span>

## <span data-ttu-id="bd28c-154">출력</span><span class="sxs-lookup"><span data-stu-id="bd28c-154">OUTPUTS</span></span>

### <span data-ttu-id="bd28c-155">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="bd28c-155">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="bd28c-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bd28c-156">NOTES</span></span>

<span data-ttu-id="bd28c-157">별칭</span><span class="sxs-lookup"><span data-stu-id="bd28c-157">ALIASES</span></span>

## <span data-ttu-id="bd28c-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bd28c-158">RELATED LINKS</span></span>

