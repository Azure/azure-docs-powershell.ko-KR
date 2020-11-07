---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fd5f27a942a33082b9488f74cac2779107f7371f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874542"
---
# <span data-ttu-id="32b79-101">Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="32b79-101">Set-AzsBackupConfiguration</span></span>

## <span data-ttu-id="32b79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32b79-102">SYNOPSIS</span></span>
<span data-ttu-id="32b79-103">지정 된 위치에서 백업 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32b79-103">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="32b79-104">구문과</span><span class="sxs-lookup"><span data-stu-id="32b79-104">SYNTAX</span></span>

### <span data-ttu-id="32b79-105">업데이트 (기본값)</span><span class="sxs-lookup"><span data-stu-id="32b79-105">Update (Default)</span></span>
```
Set-AzsBackupConfiguration [-ResourceGroupName <String>] [-Location <String>] [-Path <String>]
 [-Username <String>] [-Password <SecureString>] [-EncryptionCertPath <String>]
 [-IsBackupSchedulerEnabled <Boolean>] [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>]
 [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32b79-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="32b79-106">InputObject</span></span>
```
Set-AzsBackupConfiguration -InputObject <BackupLocation> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionCertPath <String>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="32b79-107">리소스</span><span class="sxs-lookup"><span data-stu-id="32b79-107">ResourceId</span></span>
```
Set-AzsBackupConfiguration -ResourceId <String> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionCertPath <String>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="32b79-108">설명은</span><span class="sxs-lookup"><span data-stu-id="32b79-108">DESCRIPTION</span></span>
<span data-ttu-id="32b79-109">지정 된 위치에서 백업 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32b79-109">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="32b79-110">예제의</span><span class="sxs-lookup"><span data-stu-id="32b79-110">EXAMPLES</span></span>

### <span data-ttu-id="32b79-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="32b79-111">EXAMPLE 1</span></span>
```
Set-AzsBackupConfiguration -Path "\\***.***.***.***\Share" -Username "asdomain1\azurestackadmin" -Password $password  -EncryptionCertPath $encryptionCertPath
```

<span data-ttu-id="32b79-112">Azure 스택 백업 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32b79-112">Set Azure Stack backup configuration.</span></span>

## <span data-ttu-id="32b79-113">변수</span><span class="sxs-lookup"><span data-stu-id="32b79-113">PARAMETERS</span></span>

### <span data-ttu-id="32b79-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32b79-114">-AsJob</span></span>
<span data-ttu-id="32b79-115">비동기를 작업으로 실행 하 고 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="32b79-115">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b79-116">-BackupFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="32b79-116">-BackupFrequencyInHours</span></span>
<span data-ttu-id="32b79-117">스케줄러에서 백업을 수행 하는 빈도에 대 한 간격 (시간)입니다.</span><span class="sxs-lookup"><span data-stu-id="32b79-117">The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b79-118">-BackupRetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="32b79-118">-BackupRetentionPeriodInDays</span></span>
<span data-ttu-id="32b79-119">저장소 위치의 백업 보존 기간 (일)입니다.</span><span class="sxs-lookup"><span data-stu-id="32b79-119">The retention period, in days, for backups in the storage location.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b79-120">-# Certpath</span><span class="sxs-lookup"><span data-stu-id="32b79-120">-EncryptionCertPath</span></span>
<span data-ttu-id="32b79-121">공개 키 (.cer)를 사용 하 여 암호화 인증서 파일에 대 한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="32b79-121">Path to the encryption cert file with public key (.cer).</span></span>

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

### <span data-ttu-id="32b79-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32b79-122">-InputObject</span></span>
<span data-ttu-id="32b79-123">AzsBackupConfiguration에서 반환 하는 백업 위치 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="32b79-123">Backup location configuration returned by Get-AzsBackupConfiguration.</span></span>

```yaml
Type: Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32b79-124">-IsBackupSchedulerEnabled</span><span class="sxs-lookup"><span data-stu-id="32b79-124">-IsBackupSchedulerEnabled</span></span>
<span data-ttu-id="32b79-125">백업 스케줄러를 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="32b79-125">Whether the backup scheduler should be enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b79-126">-위치</span><span class="sxs-lookup"><span data-stu-id="32b79-126">-Location</span></span>
<span data-ttu-id="32b79-127">구성할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="32b79-127">Location to configure.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b79-128">-암호</span><span class="sxs-lookup"><span data-stu-id="32b79-128">-Password</span></span>
<span data-ttu-id="32b79-129">백업 위치에 액세스 하는 데 암호가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="32b79-129">Password required to access backup location.</span></span>

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

### <span data-ttu-id="32b79-130">-Path</span><span class="sxs-lookup"><span data-stu-id="32b79-130">-Path</span></span>
<span data-ttu-id="32b79-131">백업이 저장 되는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="32b79-131">Location where backups will be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupShare

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b79-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32b79-132">-ResourceGroupName</span></span>
<span data-ttu-id="32b79-133">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32b79-133">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b79-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32b79-134">-ResourceId</span></span>
<span data-ttu-id="32b79-135">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="32b79-135">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32b79-136">-사용자 이름</span><span class="sxs-lookup"><span data-stu-id="32b79-136">-Username</span></span>
<span data-ttu-id="32b79-137">백업 위치에 액세스 하는 데 필요한 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32b79-137">Username required to access backup location.</span></span>

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

### <span data-ttu-id="32b79-138">-확인</span><span class="sxs-lookup"><span data-stu-id="32b79-138">-Confirm</span></span>
<span data-ttu-id="32b79-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="32b79-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32b79-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32b79-140">-WhatIf</span></span>
<span data-ttu-id="32b79-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="32b79-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32b79-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="32b79-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32b79-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32b79-143">CommonParameters</span></span>
<span data-ttu-id="32b79-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="32b79-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32b79-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32b79-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32b79-146">입력</span><span class="sxs-lookup"><span data-stu-id="32b79-146">INPUTS</span></span>

## <span data-ttu-id="32b79-147">출력</span><span class="sxs-lookup"><span data-stu-id="32b79-147">OUTPUTS</span></span>

### <span data-ttu-id="32b79-148">BackupLocation. 관리자. m a. 관리</span><span class="sxs-lookup"><span data-stu-id="32b79-148">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="32b79-149">상속자</span><span class="sxs-lookup"><span data-stu-id="32b79-149">NOTES</span></span>

## <span data-ttu-id="32b79-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="32b79-150">RELATED LINKS</span></span>
