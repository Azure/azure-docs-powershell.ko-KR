---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/set-azsbackupconfiguration
schema: 2.0.0
ms.openlocfilehash: c99e2c549cc865a5f7f9ad0d7c3252cbf6651e98
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94047038"
---
# <span data-ttu-id="09649-101">Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="09649-101">Set-AzsBackupConfiguration</span></span>

## <span data-ttu-id="09649-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09649-102">SYNOPSIS</span></span>
<span data-ttu-id="09649-103">백업 위치를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="09649-103">Update a backup location.</span></span>

## <span data-ttu-id="09649-104">구문과</span><span class="sxs-lookup"><span data-stu-id="09649-104">SYNTAX</span></span>

### <span data-ttu-id="09649-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="09649-105">UpdateExpanded (Default)</span></span>
```
Set-AzsBackupConfiguration [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-EncryptionCertPath <String>]
 [-IsBackupSchedulerEnabled] [-Password <SecureString>] [-Path <String>] [-Tag <Hashtable>]
 [-UserName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="09649-106">Update</span><span class="sxs-lookup"><span data-stu-id="09649-106">Update</span></span>
```
Set-AzsBackupConfiguration -Backup <IBackupLocation> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="09649-107">설명은</span><span class="sxs-lookup"><span data-stu-id="09649-107">DESCRIPTION</span></span>
<span data-ttu-id="09649-108">백업 위치를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="09649-108">Update a backup location.</span></span>

## <span data-ttu-id="09649-109">예제의</span><span class="sxs-lookup"><span data-stu-id="09649-109">EXAMPLES</span></span>

### <span data-ttu-id="09649-110">예제 1: 백업 구성 설정</span><span class="sxs-lookup"><span data-stu-id="09649-110">Example 1: Set backup configuration</span></span>
```powershell
PS C:\> Set-AzsBackupConfiguration -Path "\\***.***.***.***\Share" -Username "asdomain1\azurestackadmin" -Password $password  -EncryptionCertPath $encryptionCertPath

```

<span data-ttu-id="09649-111">Azure 스택 백업 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="09649-111">Set Azure Stack backup configuration.</span></span>

## <span data-ttu-id="09649-112">변수</span><span class="sxs-lookup"><span data-stu-id="09649-112">PARAMETERS</span></span>

### <span data-ttu-id="09649-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="09649-113">-AsJob</span></span>
<span data-ttu-id="09649-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="09649-114">Run the command as a job</span></span>

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

### <span data-ttu-id="09649-115">-백업</span><span class="sxs-lookup"><span data-stu-id="09649-115">-Backup</span></span>
<span data-ttu-id="09649-116">백업 위치에 대 한 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="09649-116">Information about the backup location.</span></span>
<span data-ttu-id="09649-117">생성 하려면 백업 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="09649-117">To construct, see NOTES section for BACKUP properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="09649-118">-BackupFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="09649-118">-BackupFrequencyInHours</span></span>
<span data-ttu-id="09649-119">스케줄러에서 백업을 수행 하는 빈도에 대 한 간격 (시간)입니다.</span><span class="sxs-lookup"><span data-stu-id="09649-119">The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="09649-120">-BackupRetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="09649-120">-BackupRetentionPeriodInDays</span></span>
<span data-ttu-id="09649-121">저장소 위치의 백업 보존 기간 (일)입니다.</span><span class="sxs-lookup"><span data-stu-id="09649-121">The retention period, in days, for backs in the storage location.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="09649-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09649-122">-DefaultProfile</span></span>
<span data-ttu-id="09649-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="09649-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09649-124">-# Certpath</span><span class="sxs-lookup"><span data-stu-id="09649-124">-EncryptionCertPath</span></span>
<span data-ttu-id="09649-125">공개 키 (.cer)를 사용 하 여 암호화 인증서 파일에 대 한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="09649-125">Path to the encryption cert file with public key (.cer).</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="09649-126">-IsBackupSchedulerEnabled</span><span class="sxs-lookup"><span data-stu-id="09649-126">-IsBackupSchedulerEnabled</span></span>
<span data-ttu-id="09649-127">백업 스케줄러를 사용할 수 있는 경우 True입니다.</span><span class="sxs-lookup"><span data-stu-id="09649-127">True if the backup scheduler is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="09649-128">-위치</span><span class="sxs-lookup"><span data-stu-id="09649-128">-Location</span></span>
<span data-ttu-id="09649-129">백업 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="09649-129">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="09649-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="09649-130">-NoWait</span></span>
<span data-ttu-id="09649-131">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="09649-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="09649-132">-암호</span><span class="sxs-lookup"><span data-stu-id="09649-132">-Password</span></span>
<span data-ttu-id="09649-133">위치에 액세스 하기 위한 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="09649-133">Password to access the location.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="09649-134">-Path</span><span class="sxs-lookup"><span data-stu-id="09649-134">-Path</span></span>
<span data-ttu-id="09649-135">업데이트 위치의 경로</span><span class="sxs-lookup"><span data-stu-id="09649-135">Path to the update location</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="09649-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09649-136">-ResourceGroupName</span></span>
<span data-ttu-id="09649-137">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="09649-137">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="09649-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="09649-138">-SubscriptionId</span></span>
<span data-ttu-id="09649-139">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="09649-139">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="09649-140">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="09649-140">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="09649-141">태그</span><span class="sxs-lookup"><span data-stu-id="09649-141">-Tag</span></span>
<span data-ttu-id="09649-142">키 값 쌍의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="09649-142">List of key value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="09649-143">-사용자 이름</span><span class="sxs-lookup"><span data-stu-id="09649-143">-UserName</span></span>
<span data-ttu-id="09649-144">위치에 액세스할 수 있는 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="09649-144">Username to access the location.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="09649-145">-확인</span><span class="sxs-lookup"><span data-stu-id="09649-145">-Confirm</span></span>
<span data-ttu-id="09649-146">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="09649-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09649-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09649-147">-WhatIf</span></span>
<span data-ttu-id="09649-148">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="09649-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09649-149">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="09649-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09649-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09649-150">CommonParameters</span></span>
<span data-ttu-id="09649-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="09649-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09649-152">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="09649-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09649-153">입력</span><span class="sxs-lookup"><span data-stu-id="09649-153">INPUTS</span></span>

### <span data-ttu-id="09649-154">Api20180901. IBackupLocation에 대 한 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="09649-154">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation</span></span>

## <span data-ttu-id="09649-155">출력</span><span class="sxs-lookup"><span data-stu-id="09649-155">OUTPUTS</span></span>

### <span data-ttu-id="09649-156">Api20180901. IBackupLocation에 대 한 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="09649-156">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation</span></span>



## <span data-ttu-id="09649-157">상속자</span><span class="sxs-lookup"><span data-stu-id="09649-157">NOTES</span></span>

<span data-ttu-id="09649-158">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="09649-158">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="09649-159">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="09649-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="09649-160">백업 <IBackupLocation> : 백업 위치에 대 한 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="09649-160">BACKUP <IBackupLocation>: Information about the backup location.</span></span>
  - <span data-ttu-id="09649-161">`[Location <String>]`: 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="09649-161">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="09649-162">`[Tag <IResourceTags>]`: 키 값 쌍의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="09649-162">`[Tag <IResourceTags>]`: List of key value pairs.</span></span>
    - <span data-ttu-id="09649-163">`[(Any) <String>]`:이 개체에 모든 속성이 추가 될 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="09649-163">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="09649-164">`[BackupFrequencyInHours <Int32?>]`: 스케줄러에서 백업을 수행 하는 빈도에 대 한 간격 (시간)입니다.</span><span class="sxs-lookup"><span data-stu-id="09649-164">`[BackupFrequencyInHours <Int32?>]`: The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>
  - <span data-ttu-id="09649-165">`[BackupRetentionPeriodInDays <Int32?>]`: 저장소 위치의 백업 보존 기간 (일)입니다.</span><span class="sxs-lookup"><span data-stu-id="09649-165">`[BackupRetentionPeriodInDays <Int32?>]`: The retention period, in days, for backs in the storage location.</span></span>
  - <span data-ttu-id="09649-166">`[EncryptionCertBase64 <String>]`: 백업 암호화 인증서에 대 한 base64 원시 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="09649-166">`[EncryptionCertBase64 <String>]`: The base64 raw data for the backup encryption certificate.</span></span>
  - <span data-ttu-id="09649-167">`[IsBackupSchedulerEnabled <Boolean?>]`: 백업 스케줄러를 사용할 수 있는 경우 True입니다.</span><span class="sxs-lookup"><span data-stu-id="09649-167">`[IsBackupSchedulerEnabled <Boolean?>]`: True if the backup scheduler is enabled.</span></span>
  - <span data-ttu-id="09649-168">`[Password <String>]`: 위치에 액세스 하기 위한 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="09649-168">`[Password <String>]`: Password to access the location.</span></span>
  - <span data-ttu-id="09649-169">`[Path <String>]`: 업데이트 위치의 경로</span><span class="sxs-lookup"><span data-stu-id="09649-169">`[Path <String>]`: Path to the update location</span></span>
  - <span data-ttu-id="09649-170">`[UserName <String>]`: 위치에 액세스 하기 위한 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="09649-170">`[UserName <String>]`: Username to access the location.</span></span>

## <span data-ttu-id="09649-171">관련 링크</span><span class="sxs-lookup"><span data-stu-id="09649-171">RELATED LINKS</span></span>

