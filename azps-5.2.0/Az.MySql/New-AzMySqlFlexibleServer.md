---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
ms.openlocfilehash: 1dbd998cdafc92de6541e25c2cb2bf6477e2d5b2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329496"
---
# <span data-ttu-id="b1860-101">New-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="b1860-101">New-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="b1860-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1860-102">SYNOPSIS</span></span>
<span data-ttu-id="b1860-103">새 MySQL 유연한 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1860-103">Creates a new MySQL flexible server</span></span>

## <span data-ttu-id="b1860-104">구문</span><span class="sxs-lookup"><span data-stu-id="b1860-104">SYNTAX</span></span>

```
New-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> -AdministratorUserName <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-Location <String>] [-Sku <String>] [-SkuTier <String>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b1860-105">설명</span><span class="sxs-lookup"><span data-stu-id="b1860-105">DESCRIPTION</span></span>
<span data-ttu-id="b1860-106">새 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1860-106">Creates a new server.</span></span>

## <span data-ttu-id="b1860-107">예제</span><span class="sxs-lookup"><span data-stu-id="b1860-107">EXAMPLES</span></span>

### <span data-ttu-id="b1860-108">예제 1: 새 MySql 유연한 서버 만들기</span><span class="sxs-lookup"><span data-stu-id="b1860-108">Example 1: Create a new MySql flexible server</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest \
-Location eastus -AdministratorUserName mysqltest -AdministratorLoginPassword $password -Sku Standard_B1ms -SkuTier Burstable -Version 12 -StorageInMb 10240

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName         SkuTier     
----            -------- ------------------ ------- ----------------------- ------------    -------------        
mysql-test      West US 2   mysqltest    5.7      10240                  Standard_B1ms   Burstable
```



### <span data-ttu-id="b1860-109">예제 2: 기본 설정을 사용하여 새 MySql 유연한 서버 만들기</span><span class="sxs-lookup"><span data-stu-id="b1860-109">Example 2: Create a new MySql flexible server with default setting</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest \
-AdministratorUserName mysqltest -AdministratorLoginPassword $password

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName         SkuTier     
----            -------- ------------------ ------- ----------------------- ------------    -------------        
mysql-test      West US 2   mysqltest    5.7      131072                  Standard_B1ms   Burstable
```

<span data-ttu-id="b1860-110">기본값으로 MySql 서버를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1860-110">Create MySql server with default values.</span></span>
<span data-ttu-id="b1860-111">위치의 기본값은 미국 서부 2, SKU는 Standard_B1ms, SKU 계층은 버스터블, 저장소 크기는 10GiB입니다.</span><span class="sxs-lookup"><span data-stu-id="b1860-111">The default values of location is West US 2, Sku is Standard_B1ms, Sku tier is Burstable, and storage size is 10GiB.</span></span>

## <span data-ttu-id="b1860-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1860-112">PARAMETERS</span></span>

### <span data-ttu-id="b1860-113">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="b1860-113">-AdministratorLoginPassword</span></span>
<span data-ttu-id="b1860-114">관리자의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="b1860-114">The password of the administrator.</span></span>
<span data-ttu-id="b1860-115">최소 8자 및 최대 128자입니다.</span><span class="sxs-lookup"><span data-stu-id="b1860-115">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="b1860-116">암호는 영어 대문자, 영어 소문자, 숫자 및 영문자 이 세 가지 범주의 문자를 포함해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1860-116">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="b1860-117">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="b1860-117">-AdministratorUserName</span></span>
<span data-ttu-id="b1860-118">서버에 대한 관리자 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1860-118">Administrator username for the server.</span></span>
<span data-ttu-id="b1860-119">설정하면 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b1860-119">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="b1860-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1860-120">-AsJob</span></span>
<span data-ttu-id="b1860-121">명령을 작업으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="b1860-121">Run the command as a job.</span></span>

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

### <span data-ttu-id="b1860-122">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="b1860-122">-BackupRetentionDay</span></span>
<span data-ttu-id="b1860-123">서버에 대한 백업 보존 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="b1860-123">Backup retention days for the server.</span></span>
<span data-ttu-id="b1860-124">일 수는 7에서 35 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="b1860-124">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="b1860-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1860-125">-DefaultProfile</span></span>
<span data-ttu-id="b1860-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b1860-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1860-127">-Location</span><span class="sxs-lookup"><span data-stu-id="b1860-127">-Location</span></span>
<span data-ttu-id="b1860-128">리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b1860-128">The location the resource resides in.</span></span>

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

### <span data-ttu-id="b1860-129">-Name</span><span class="sxs-lookup"><span data-stu-id="b1860-129">-Name</span></span>
<span data-ttu-id="b1860-130">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1860-130">The name of the server.</span></span>

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

### <span data-ttu-id="b1860-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b1860-131">-NoWait</span></span>
<span data-ttu-id="b1860-132">명령을 비동기적으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="b1860-132">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="b1860-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1860-133">-ResourceGroupName</span></span>
<span data-ttu-id="b1860-134">리소스가 포함된 리소스 그룹의 이름입니다. Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1860-134">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b1860-135">-Sku</span><span class="sxs-lookup"><span data-stu-id="b1860-135">-Sku</span></span>
<span data-ttu-id="b1860-136">SKU의 이름(일반적으로 계층 + 패밀리 + 코어)입니다(예: Standard_B1ms, Standard_D2ds_v4.</span><span class="sxs-lookup"><span data-stu-id="b1860-136">The name of the sku, typically, tier + family + cores, e.g. Standard_B1ms, Standard_D2ds_v4.</span></span>

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

### <span data-ttu-id="b1860-137">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="b1860-137">-SkuTier</span></span>
<span data-ttu-id="b1860-138">서버의 계산 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="b1860-138">Compute tier of the server.</span></span>
<span data-ttu-id="b1860-139">허용되는 값: 버스터블, GeneralPurpose, 메모리 최적화.</span><span class="sxs-lookup"><span data-stu-id="b1860-139">Accepted values: Burstable, GeneralPurpose, Memory Optimized.</span></span>
<span data-ttu-id="b1860-140">기본값: 버스터블.</span><span class="sxs-lookup"><span data-stu-id="b1860-140">Default: Burstable.</span></span>

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

### <span data-ttu-id="b1860-141">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="b1860-141">-StorageInMb</span></span>
<span data-ttu-id="b1860-142">서버에 허용되는 최대 저장소입니다.</span><span class="sxs-lookup"><span data-stu-id="b1860-142">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="b1860-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b1860-143">-SubscriptionId</span></span>
<span data-ttu-id="b1860-144">Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b1860-144">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="b1860-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="b1860-145">-Tag</span></span>
<span data-ttu-id="b1860-146">키-값 쌍의 형태로 애플리케이션별 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="b1860-146">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="b1860-147">-Version</span><span class="sxs-lookup"><span data-stu-id="b1860-147">-Version</span></span>
<span data-ttu-id="b1860-148">서버 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="b1860-148">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1860-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1860-149">-Confirm</span></span>
<span data-ttu-id="b1860-150">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1860-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1860-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1860-151">-WhatIf</span></span>
<span data-ttu-id="b1860-152">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b1860-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1860-153">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1860-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1860-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1860-154">CommonParameters</span></span>
<span data-ttu-id="b1860-155">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b1860-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1860-156">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b1860-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1860-157">입력</span><span class="sxs-lookup"><span data-stu-id="b1860-157">INPUTS</span></span>

## <span data-ttu-id="b1860-158">출력</span><span class="sxs-lookup"><span data-stu-id="b1860-158">OUTPUTS</span></span>

### <span data-ttu-id="b1860-159">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="b1860-159">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="b1860-160">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b1860-160">NOTES</span></span>

<span data-ttu-id="b1860-161">별칭</span><span class="sxs-lookup"><span data-stu-id="b1860-161">ALIASES</span></span>

## <span data-ttu-id="b1860-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1860-162">RELATED LINKS</span></span>

