---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 55E097F4-1F49-4196-9A8B-949FD5D9108A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4035487fa0363e6a7802966d9bc6422429723d94
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046199"
---
# <span data-ttu-id="51116-101">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="51116-101">New-AzureVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="51116-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51116-102">SYNOPSIS</span></span>
<span data-ttu-id="51116-103">SQL Server 자동 백업에 대 한 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51116-103">Creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="51116-104">구문과</span><span class="sxs-lookup"><span data-stu-id="51116-104">SYNTAX</span></span>

### <span data-ttu-id="51116-105">StorageUriSqlServerAutoBackup (기본값)</span><span class="sxs-lookup"><span data-stu-id="51116-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>]
 [-BackupSystemDbs] [-BackupScheduleType <String>] [-FullBackupFrequency <String>]
 [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="51116-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="51116-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageContext] <AzureStorageContext>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="51116-107">설명은</span><span class="sxs-lookup"><span data-stu-id="51116-107">DESCRIPTION</span></span>
<span data-ttu-id="51116-108">**AzureVMSqlServerAutoBackupConfig** CMDLET은 SQL Server 자동 백업에 대 한 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51116-108">The **New-AzureVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="51116-109">예제의</span><span class="sxs-lookup"><span data-stu-id="51116-109">EXAMPLES</span></span>

### <span data-ttu-id="51116-110">예제 1: 저장소 URI 및 계정 키를 사용 하 여 자동 백업 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="51116-110">Example 1: Create an auto-backup configuration using storage URI and account key</span></span>
```
PS C:\> $ABS = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="51116-111">이 명령은 저장소 URL 및 계정 키를 지정 하 여 자동 백업 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51116-111">This command creates an auto-backup configuration object by specifying storage URL and account key.</span></span>

### <span data-ttu-id="51116-112">예제 2: 저장소 컨텍스트를 사용 하 여 자동 백업 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="51116-112">Example 2: Create an auto-backup configuration using storage context</span></span>
```
PS C:\> $ABS = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="51116-113">이 명령은 저장소 컨텍스트를 지정 하 여 자동 백업 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51116-113">This command creates an auto-backup configuration object by specifying storage context.</span></span>

### <span data-ttu-id="51116-114">예제 3: 암호화 및 암호를 사용 하 여 저장소 컨텍스트를 사용 하 여 자동 백업 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="51116-114">Example 3: Create an auto-backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $ABS = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertPasswd
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="51116-115">이 명령은 저장소 컨텍스트를 지정 하 고 암호를 사용 하 여 암호화 옵션을 사용 하도록 설정 하 여 자동 백업 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="51116-115">This command creates an auto-backup configuration object by specifying Storage context and enabling encryption option with password.</span></span>
<span data-ttu-id="51116-116">$CertPasswd 이라는 변수에 저장 된 certificatepassword를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51116-116">The certificatepassword ist stored in the variable named $CertPasswd.</span></span>

## <span data-ttu-id="51116-117">변수</span><span class="sxs-lookup"><span data-stu-id="51116-117">PARAMETERS</span></span>

### <span data-ttu-id="51116-118">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="51116-118">-BackupScheduleType</span></span>
<span data-ttu-id="51116-119">백업 일정 유형, 수동 또는 자동</span><span class="sxs-lookup"><span data-stu-id="51116-119">Backup schedule type, manual or automated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51116-120">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="51116-120">-BackupSystemDbs</span></span>
<span data-ttu-id="51116-121">시스템 데이터베이스 백업</span><span class="sxs-lookup"><span data-stu-id="51116-121">Backup system databases</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51116-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="51116-122">-CertificatePassword</span></span>
<span data-ttu-id="51116-123">SQL Server 암호화 백업을 수행 하는 데 사용 되는 인증서를 암호화 하는 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51116-123">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51116-124">-사용</span><span class="sxs-lookup"><span data-stu-id="51116-124">-Enable</span></span>
<span data-ttu-id="51116-125">SQL Server 가상 컴퓨터에 대해 자동화 된 백업을 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="51116-125">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="51116-126">이 매개 변수를 사용 하는 경우 자동 백업은 모든 현재 및 새 데이터베이스에 대 한 백업 일정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51116-126">If you use this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="51116-127">이렇게 하면 관리 되는 백업 설정이 다음 일정을 따라 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="51116-127">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51116-128">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="51116-128">-EnableEncryption</span></span>
<span data-ttu-id="51116-129">암호화가 사용 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="51116-129">Indicates that encryption is enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51116-130">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="51116-130">-FullBackupFrequency</span></span>
<span data-ttu-id="51116-131">Sql Server 전체 백업 빈도 (매일 또는 주)</span><span class="sxs-lookup"><span data-stu-id="51116-131">Sql Server Full Backup frequency, daily or week</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51116-132">-Fullbackupstarth</span><span class="sxs-lookup"><span data-stu-id="51116-132">-FullBackupStartHour</span></span>
<span data-ttu-id="51116-133">Sql Server 전체 백업을 시작 해야 하는 날짜의 시간 (0-23)</span><span class="sxs-lookup"><span data-stu-id="51116-133">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51116-134">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="51116-134">-FullBackupWindowInHours</span></span>
<span data-ttu-id="51116-135">Sql Server 전체 백업 창 (시간)</span><span class="sxs-lookup"><span data-stu-id="51116-135">Sql Server Full Backup window in hours</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51116-136">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="51116-136">-InformationAction</span></span>
<span data-ttu-id="51116-137">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51116-137">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="51116-138">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="51116-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="51116-139">하기로</span><span class="sxs-lookup"><span data-stu-id="51116-139">Continue</span></span>
- <span data-ttu-id="51116-140">숨기기</span><span class="sxs-lookup"><span data-stu-id="51116-140">Ignore</span></span>
- <span data-ttu-id="51116-141">Inquire</span><span class="sxs-lookup"><span data-stu-id="51116-141">Inquire</span></span>
- <span data-ttu-id="51116-142">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="51116-142">SilentlyContinue</span></span>
- <span data-ttu-id="51116-143">중지가</span><span class="sxs-lookup"><span data-stu-id="51116-143">Stop</span></span>
- <span data-ttu-id="51116-144">대기</span><span class="sxs-lookup"><span data-stu-id="51116-144">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51116-145">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="51116-145">-InformationVariable</span></span>
<span data-ttu-id="51116-146">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51116-146">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51116-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="51116-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="51116-148">Sql Server 로그 백업 빈도 (1-60 분 마다 한 번)</span><span class="sxs-lookup"><span data-stu-id="51116-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51116-149">-프로필</span><span class="sxs-lookup"><span data-stu-id="51116-149">-Profile</span></span>
<span data-ttu-id="51116-150">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51116-150">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="51116-151">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="51116-151">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51116-152">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="51116-152">-RetentionPeriodInDays</span></span>
<span data-ttu-id="51116-153">보존 기간의 기간 (일)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51116-153">Specifies the length of the retention period in days.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51116-154">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="51116-154">-StorageContext</span></span>
<span data-ttu-id="51116-155">백업을 저장 하는 데 사용할 저장소 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51116-155">Specifies the storage account to be used to store backups.</span></span>
<span data-ttu-id="51116-156">기본값은 SQL Server 가상 머신과 연결 된 저장소 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="51116-156">Default is the storage account associated with the SQL Server virtual machine.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51116-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="51116-157">-StorageKey</span></span>
<span data-ttu-id="51116-158">Blob 저장소 계정의 저장소 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51116-158">Specifies the storage key of the blob storage account.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51116-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="51116-159">-StorageUri</span></span>
<span data-ttu-id="51116-160">Blob 저장소 계정에 대 한 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="51116-160">Specifies a URI to the blob storage account.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51116-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51116-161">CommonParameters</span></span>
<span data-ttu-id="51116-162">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="51116-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51116-163">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51116-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51116-164">입력</span><span class="sxs-lookup"><span data-stu-id="51116-164">INPUTS</span></span>

## <span data-ttu-id="51116-165">출력</span><span class="sxs-lookup"><span data-stu-id="51116-165">OUTPUTS</span></span>

## <span data-ttu-id="51116-166">상속자</span><span class="sxs-lookup"><span data-stu-id="51116-166">NOTES</span></span>

## <span data-ttu-id="51116-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="51116-167">RELATED LINKS</span></span>

[<span data-ttu-id="51116-168">새로운 AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="51116-168">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)


