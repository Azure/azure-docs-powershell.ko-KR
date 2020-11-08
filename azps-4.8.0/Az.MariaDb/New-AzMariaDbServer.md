---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbServer.md
ms.openlocfilehash: e6416fd67091fc86a5fe9844d3b1d366aaa6cb58
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048190"
---
# <span data-ttu-id="ee2a2-101">New-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="ee2a2-101">New-AzMariaDbServer</span></span>

## <span data-ttu-id="ee2a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee2a2-102">SYNOPSIS</span></span>
<span data-ttu-id="ee2a2-103">새을 (를) 새로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ee2a2-103">Creates a new MariaDB.</span></span>

## <span data-ttu-id="ee2a2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ee2a2-104">SYNTAX</span></span>

```
New-AzMariaDbServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUsername <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ee2a2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ee2a2-105">DESCRIPTION</span></span>
<span data-ttu-id="ee2a2-106">새을 (를) 새로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ee2a2-106">Creates a new MariaDB.</span></span>

## <span data-ttu-id="ee2a2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ee2a2-107">EXAMPLES</span></span>

### <span data-ttu-id="ee2a2-108">예제 1: 새 작업 만들기 a b</span><span class="sxs-lookup"><span data-stu-id="ee2a2-108">Example 1: Create a new MariaDB</span></span>
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

<span data-ttu-id="ee2a2-109">이 명령은 새로운 새를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ee2a2-109">This command creates a new MariaDB.</span></span>

## <span data-ttu-id="ee2a2-110">변수</span><span class="sxs-lookup"><span data-stu-id="ee2a2-110">PARAMETERS</span></span>

### <span data-ttu-id="ee2a2-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="ee2a2-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="ee2a2-112">관리자의 암호는 SecureString 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee2a2-112">Password of administrator, should be SecureString.</span></span>

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

### <span data-ttu-id="ee2a2-113">-관리자 이름</span><span class="sxs-lookup"><span data-stu-id="ee2a2-113">-AdministratorUsername</span></span>
<span data-ttu-id="ee2a2-114">관리자의 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee2a2-114">Username of administrator.</span></span>

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

### <span data-ttu-id="ee2a2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee2a2-115">-AsJob</span></span>
<span data-ttu-id="ee2a2-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="ee2a2-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ee2a2-117">-Backup보존 일정</span><span class="sxs-lookup"><span data-stu-id="ee2a2-117">-BackupRetentionDay</span></span>
<span data-ttu-id="ee2a2-118">서버에 대 한 백업 보존 일입니다.</span><span class="sxs-lookup"><span data-stu-id="ee2a2-118">Backup retention days for the server.</span></span>

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

### <span data-ttu-id="ee2a2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee2a2-119">-DefaultProfile</span></span>
<span data-ttu-id="ee2a2-120">region DefaultParameters Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ee2a2-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee2a2-121">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="ee2a2-121">-GeoRedundantBackup</span></span>
<span data-ttu-id="ee2a2-122">지역 중복을 사용 하거나 서버 백업에 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ee2a2-122">Enable Geo-redundant or not for server backup.</span></span>

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

### <span data-ttu-id="ee2a2-123">-위치</span><span class="sxs-lookup"><span data-stu-id="ee2a2-123">-Location</span></span>
<span data-ttu-id="ee2a2-124">리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="ee2a2-124">The location the resource resides in.</span></span>

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

### <span data-ttu-id="ee2a2-125">-이름</span><span class="sxs-lookup"><span data-stu-id="ee2a2-125">-Name</span></span>
<span data-ttu-id="ee2a2-126">E 2 Iadb 서버 이름.</span><span class="sxs-lookup"><span data-stu-id="ee2a2-126">MariaDB server name.</span></span>

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

### <span data-ttu-id="ee2a2-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ee2a2-127">-NoWait</span></span>
<span data-ttu-id="ee2a2-128">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="ee2a2-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ee2a2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee2a2-129">-ResourceGroupName</span></span>
<span data-ttu-id="ee2a2-130">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee2a2-130">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="ee2a2-131">-Sku</span><span class="sxs-lookup"><span data-stu-id="ee2a2-131">-Sku</span></span>
<span data-ttu-id="ee2a2-132">Sku (일반적으로 계층 + 패밀리 + 코어)의 이름 (예: B_Gen4_1 GP_Gen5_8)입니다.</span><span class="sxs-lookup"><span data-stu-id="ee2a2-132">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="ee2a2-133">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="ee2a2-133">-SslEnforcement</span></span>
<span data-ttu-id="ee2a2-134">서버에 연결할 때 ssl 적용 여부를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee2a2-134">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="ee2a2-135">-StorageAutogrow 증가</span><span class="sxs-lookup"><span data-stu-id="ee2a2-135">-StorageAutogrow</span></span>
<span data-ttu-id="ee2a2-136">저장소 자동 증가를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee2a2-136">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="ee2a2-137">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="ee2a2-137">-StorageInMb</span></span>
<span data-ttu-id="ee2a2-138">서버에 허용 되는 최대 저장소.</span><span class="sxs-lookup"><span data-stu-id="ee2a2-138">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="ee2a2-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ee2a2-139">-SubscriptionId</span></span>
<span data-ttu-id="ee2a2-140">구독 ID는 모든 서비스 통화에 대 한 URI의 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="ee2a2-140">The subscription ID is part of the URI for every service call</span></span>

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

### <span data-ttu-id="ee2a2-141">태그</span><span class="sxs-lookup"><span data-stu-id="ee2a2-141">-Tag</span></span>
<span data-ttu-id="ee2a2-142">키-값 쌍의 형식으로 된 응용 프로그램 관련 메타 데이터</span><span class="sxs-lookup"><span data-stu-id="ee2a2-142">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="ee2a2-143">-버전</span><span class="sxs-lookup"><span data-stu-id="ee2a2-143">-Version</span></span>
<span data-ttu-id="ee2a2-144">서버 버전.</span><span class="sxs-lookup"><span data-stu-id="ee2a2-144">Server version.</span></span>

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

### <span data-ttu-id="ee2a2-145">-확인</span><span class="sxs-lookup"><span data-stu-id="ee2a2-145">-Confirm</span></span>
<span data-ttu-id="ee2a2-146">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee2a2-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee2a2-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee2a2-147">-WhatIf</span></span>
<span data-ttu-id="ee2a2-148">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ee2a2-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee2a2-149">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ee2a2-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee2a2-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee2a2-150">CommonParameters</span></span>
<span data-ttu-id="ee2a2-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee2a2-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee2a2-152">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ee2a2-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee2a2-153">입력</span><span class="sxs-lookup"><span data-stu-id="ee2a2-153">INPUTS</span></span>

## <span data-ttu-id="ee2a2-154">출력</span><span class="sxs-lookup"><span data-stu-id="ee2a2-154">OUTPUTS</span></span>

### <span data-ttu-id="ee2a2-155">Api20180601Preview Iadb. i r i. IServer</span><span class="sxs-lookup"><span data-stu-id="ee2a2-155">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="ee2a2-156">상속자</span><span class="sxs-lookup"><span data-stu-id="ee2a2-156">NOTES</span></span>

<span data-ttu-id="ee2a2-157">별칭과</span><span class="sxs-lookup"><span data-stu-id="ee2a2-157">ALIASES</span></span>

## <span data-ttu-id="ee2a2-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ee2a2-158">RELATED LINKS</span></span>

