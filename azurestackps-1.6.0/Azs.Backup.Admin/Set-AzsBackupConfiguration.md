---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 271426278c561ede4778e0ad69cf9ee4e6c0607e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523927"
---
# <span data-ttu-id="b5e02-101">Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="b5e02-101">Set-AzsBackupConfiguration</span></span>

## <span data-ttu-id="b5e02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5e02-102">SYNOPSIS</span></span>
<span data-ttu-id="b5e02-103">지정 된 위치에서 백업 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5e02-103">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="b5e02-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b5e02-104">SYNTAX</span></span>

### <span data-ttu-id="b5e02-105">업데이트 (기본값)</span><span class="sxs-lookup"><span data-stu-id="b5e02-105">Update (Default)</span></span>
```
Set-AzsBackupConfiguration [-ResourceGroupName <String>] [-Location <String>] [-Path <String>]
 [-Username <String>] [-Password <SecureString>] [-EncryptionKey <SecureString>]
 [-IsBackupSchedulerEnabled <Boolean>] [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>]
 [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5e02-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b5e02-106">InputObject</span></span>
```
Set-AzsBackupConfiguration -InputObject <BackupLocation> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionKey <SecureString>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b5e02-107">리소스</span><span class="sxs-lookup"><span data-stu-id="b5e02-107">ResourceId</span></span>
```
Set-AzsBackupConfiguration -ResourceId <String> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionKey <SecureString>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5e02-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b5e02-108">DESCRIPTION</span></span>
<span data-ttu-id="b5e02-109">지정 된 위치에서 백업 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5e02-109">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="b5e02-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b5e02-110">EXAMPLES</span></span>

### <span data-ttu-id="b5e02-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b5e02-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsBackupConfiguration -Path "\\***.***.***.***\Share" -Username "asdomain1\azurestackadmin" -Password $password  -EncryptionKey $encryptionKey
```

<span data-ttu-id="b5e02-112">Azure 스택 백업 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5e02-112">Set Azure Stack backup configuration.</span></span>

## <span data-ttu-id="b5e02-113">변수</span><span class="sxs-lookup"><span data-stu-id="b5e02-113">PARAMETERS</span></span>

### <span data-ttu-id="b5e02-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5e02-114">-AsJob</span></span>
<span data-ttu-id="b5e02-115">비동기를 작업으로 실행 하 고 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5e02-115">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e02-116">-BackupFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="b5e02-116">-BackupFrequencyInHours</span></span>
<span data-ttu-id="b5e02-117">스케줄러에서 백업을 수행 하는 빈도에 대 한 간격 (시간)입니다.</span><span class="sxs-lookup"><span data-stu-id="b5e02-117">The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e02-118">-BackupRetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="b5e02-118">-BackupRetentionPeriodInDays</span></span>
<span data-ttu-id="b5e02-119">저장소 위치의 백업 보존 기간 (일)입니다.</span><span class="sxs-lookup"><span data-stu-id="b5e02-119">The retention period, in days, for backups in the storage location.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e02-120">-Encryption.encryptionkey</span><span class="sxs-lookup"><span data-stu-id="b5e02-120">-EncryptionKey</span></span>
<span data-ttu-id="b5e02-121">백업을 암호화 하는 데 사용 되는 암호화 키입니다.</span><span class="sxs-lookup"><span data-stu-id="b5e02-121">Encryption key used to encrypt backups.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e02-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5e02-122">-InputObject</span></span>
<span data-ttu-id="b5e02-123">AzsBackupConfiguration에서 반환 하는 백업 위치 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="b5e02-123">Backup location configuration returned by Get-AzsBackupConfiguration.</span></span>

```yaml
Type: BackupLocation
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5e02-124">-IsBackupSchedulerEnabled</span><span class="sxs-lookup"><span data-stu-id="b5e02-124">-IsBackupSchedulerEnabled</span></span>
<span data-ttu-id="b5e02-125">백업 스케줄러를 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5e02-125">Whether the backup scheduler should be enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e02-126">-위치</span><span class="sxs-lookup"><span data-stu-id="b5e02-126">-Location</span></span>
<span data-ttu-id="b5e02-127">구성할 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b5e02-127">Location to configure.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e02-128">-암호</span><span class="sxs-lookup"><span data-stu-id="b5e02-128">-Password</span></span>
<span data-ttu-id="b5e02-129">백업 위치에 액세스 하는 데 암호가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5e02-129">Password required to access backup location.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e02-130">-Path</span><span class="sxs-lookup"><span data-stu-id="b5e02-130">-Path</span></span>
<span data-ttu-id="b5e02-131">백업이 저장 되는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b5e02-131">Location where backups will be stored.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: BackupShare

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e02-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5e02-132">-ResourceGroupName</span></span>
<span data-ttu-id="b5e02-133">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b5e02-133">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e02-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5e02-134">-ResourceId</span></span>
<span data-ttu-id="b5e02-135">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="b5e02-135">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5e02-136">-사용자 이름</span><span class="sxs-lookup"><span data-stu-id="b5e02-136">-Username</span></span>
<span data-ttu-id="b5e02-137">백업 위치에 액세스 하는 데 필요한 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b5e02-137">Username required to access backup location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e02-138">-확인</span><span class="sxs-lookup"><span data-stu-id="b5e02-138">-Confirm</span></span>
<span data-ttu-id="b5e02-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5e02-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e02-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5e02-140">-WhatIf</span></span>
<span data-ttu-id="b5e02-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b5e02-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5e02-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b5e02-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5e02-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5e02-143">CommonParameters</span></span>
<span data-ttu-id="b5e02-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5e02-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5e02-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5e02-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5e02-146">입력</span><span class="sxs-lookup"><span data-stu-id="b5e02-146">INPUTS</span></span>

## <span data-ttu-id="b5e02-147">출력</span><span class="sxs-lookup"><span data-stu-id="b5e02-147">OUTPUTS</span></span>

### <span data-ttu-id="b5e02-148">BackupLocation. 관리자. m a. 관리</span><span class="sxs-lookup"><span data-stu-id="b5e02-148">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="b5e02-149">상속자</span><span class="sxs-lookup"><span data-stu-id="b5e02-149">NOTES</span></span>

## <span data-ttu-id="b5e02-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b5e02-150">RELATED LINKS</span></span>

