---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlServer.md
ms.openlocfilehash: 3b9ca8c4aa236b690bbe0dfe09c35f0ebc8a5b22
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048174"
---
# <span data-ttu-id="0ed52-101">New-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="0ed52-101">New-AzMySqlServer</span></span>

## <span data-ttu-id="0ed52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ed52-102">SYNOPSIS</span></span>
<span data-ttu-id="0ed52-103">새 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0ed52-103">Creates a new server.</span></span>

## <span data-ttu-id="0ed52-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0ed52-104">SYNTAX</span></span>

```
New-AzMySqlServer -Name <String> -ResourceGroupName <String> -AdministratorLoginPassword <SecureString>
 -AdministratorUserName <String> -Location <String> -Sku <String> [-SubscriptionId <String>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-Version <ServerVersion>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0ed52-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0ed52-105">DESCRIPTION</span></span>
<span data-ttu-id="0ed52-106">새 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0ed52-106">Creates a new server.</span></span>

## <span data-ttu-id="0ed52-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0ed52-107">EXAMPLES</span></span>

### <span data-ttu-id="0ed52-108">예제 1: 새 MySql 서버 만들기</span><span class="sxs-lookup"><span data-stu-id="0ed52-108">Example 1: Create a new MySql server</span></span>
```powershell
PS C:\> New-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -Location eastus -AdministratorUser mysql_test -AdministratorLoginPassword $password -Sku GP_Gen5_4

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="0ed52-109">이러한 cmdlet은 새 MySql 서버를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0ed52-109">These cmdlets create a new MySql server.</span></span>

## <span data-ttu-id="0ed52-110">변수</span><span class="sxs-lookup"><span data-stu-id="0ed52-110">PARAMETERS</span></span>

### <span data-ttu-id="0ed52-111">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="0ed52-111">-AdministratorLoginPassword</span></span>
<span data-ttu-id="0ed52-112">리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="0ed52-112">The location the resource resides in.</span></span>

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

### <span data-ttu-id="0ed52-113">-관리자 이름</span><span class="sxs-lookup"><span data-stu-id="0ed52-113">-AdministratorUserName</span></span>
<span data-ttu-id="0ed52-114">리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="0ed52-114">The location the resource resides in.</span></span>

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

### <span data-ttu-id="0ed52-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0ed52-115">-AsJob</span></span>
<span data-ttu-id="0ed52-116">명령을 작업으로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ed52-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="0ed52-117">-Backup보존 일정</span><span class="sxs-lookup"><span data-stu-id="0ed52-117">-BackupRetentionDay</span></span>
<span data-ttu-id="0ed52-118">서버에 대 한 백업 보존 일입니다.</span><span class="sxs-lookup"><span data-stu-id="0ed52-118">Backup retention days for the server.</span></span>
<span data-ttu-id="0ed52-119">일 수는 7 ~ 35입니다.</span><span class="sxs-lookup"><span data-stu-id="0ed52-119">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="0ed52-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ed52-120">-DefaultProfile</span></span>
<span data-ttu-id="0ed52-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0ed52-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ed52-122">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="0ed52-122">-GeoRedundantBackup</span></span>
<span data-ttu-id="0ed52-123">지역 중복을 사용 하거나 서버 백업에 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0ed52-123">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ed52-124">-위치</span><span class="sxs-lookup"><span data-stu-id="0ed52-124">-Location</span></span>
<span data-ttu-id="0ed52-125">리소스가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="0ed52-125">The location the resource resides in.</span></span>

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

### <span data-ttu-id="0ed52-126">-이름</span><span class="sxs-lookup"><span data-stu-id="0ed52-126">-Name</span></span>
<span data-ttu-id="0ed52-127">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ed52-127">The name of the server.</span></span>

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

### <span data-ttu-id="0ed52-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0ed52-128">-NoWait</span></span>
<span data-ttu-id="0ed52-129">비동기적으로 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ed52-129">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="0ed52-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ed52-130">-ResourceGroupName</span></span>
<span data-ttu-id="0ed52-131">리소스가 포함 된 리소스 그룹의 이름입니다. Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ed52-131">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="0ed52-132">-Sku</span><span class="sxs-lookup"><span data-stu-id="0ed52-132">-Sku</span></span>
<span data-ttu-id="0ed52-133">Sku (일반적으로 계층 + 패밀리 + 코어)의 이름 (예: B_Gen4_1 GP_Gen5_8)입니다.</span><span class="sxs-lookup"><span data-stu-id="0ed52-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="0ed52-134">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="0ed52-134">-SslEnforcement</span></span>
<span data-ttu-id="0ed52-135">서버에 연결할 때 ssl 적용 여부를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ed52-135">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="0ed52-136">-StorageAutogrow 증가</span><span class="sxs-lookup"><span data-stu-id="0ed52-136">-StorageAutogrow</span></span>
<span data-ttu-id="0ed52-137">저장소 자동 증가를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ed52-137">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="0ed52-138">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="0ed52-138">-StorageInMb</span></span>
<span data-ttu-id="0ed52-139">서버에 허용 되는 최대 저장소.</span><span class="sxs-lookup"><span data-stu-id="0ed52-139">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="0ed52-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0ed52-140">-SubscriptionId</span></span>
<span data-ttu-id="0ed52-141">Azure 구독을 식별 하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0ed52-141">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="0ed52-142">태그</span><span class="sxs-lookup"><span data-stu-id="0ed52-142">-Tag</span></span>
<span data-ttu-id="0ed52-143">키-값 쌍의 형식으로 된 응용 프로그램 관련 메타 데이터</span><span class="sxs-lookup"><span data-stu-id="0ed52-143">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="0ed52-144">-버전</span><span class="sxs-lookup"><span data-stu-id="0ed52-144">-Version</span></span>
<span data-ttu-id="0ed52-145">서버 버전.</span><span class="sxs-lookup"><span data-stu-id="0ed52-145">Server version.</span></span>

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

### <span data-ttu-id="0ed52-146">-확인</span><span class="sxs-lookup"><span data-stu-id="0ed52-146">-Confirm</span></span>
<span data-ttu-id="0ed52-147">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ed52-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ed52-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ed52-148">-WhatIf</span></span>
<span data-ttu-id="0ed52-149">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0ed52-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ed52-150">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0ed52-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ed52-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ed52-151">CommonParameters</span></span>
<span data-ttu-id="0ed52-152">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ed52-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ed52-153">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0ed52-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ed52-154">입력</span><span class="sxs-lookup"><span data-stu-id="0ed52-154">INPUTS</span></span>

## <span data-ttu-id="0ed52-155">출력</span><span class="sxs-lookup"><span data-stu-id="0ed52-155">OUTPUTS</span></span>

### <span data-ttu-id="0ed52-156">Api20171201 (Microsoft. i m/. i m/. i m/. 서버)</span><span class="sxs-lookup"><span data-stu-id="0ed52-156">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="0ed52-157">상속자</span><span class="sxs-lookup"><span data-stu-id="0ed52-157">NOTES</span></span>

<span data-ttu-id="0ed52-158">별칭과</span><span class="sxs-lookup"><span data-stu-id="0ed52-158">ALIASES</span></span>

## <span data-ttu-id="0ed52-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ed52-159">RELATED LINKS</span></span>

