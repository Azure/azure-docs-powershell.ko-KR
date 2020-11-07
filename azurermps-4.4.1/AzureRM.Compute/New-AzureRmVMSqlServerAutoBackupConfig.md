---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
Module Name: Azure
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: 2617ca54050f6a37fcc5714fe80e2f2d50e33e40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711616"
---
# <span data-ttu-id="a3415-101">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="a3415-101">New-AzureVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="a3415-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3415-102">SYNOPSIS</span></span>
<span data-ttu-id="a3415-103">SQL Server 자동 백업에 대 한 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a3415-103">Creates a configuration object for SQL Server automatic backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3415-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a3415-104">SYNTAX</span></span>

### <span data-ttu-id="a3415-105">StorageUriSqlServerAutoBackup (기본값)</span><span class="sxs-lookup"><span data-stu-id="a3415-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>]
 [-BackupSystemDbs] [-BackupScheduleType <String>] [-FullBackupFrequency <String>]
 [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="a3415-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="a3415-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageContext] <IStorageContext>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a3415-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a3415-107">DESCRIPTION</span></span>
<span data-ttu-id="a3415-108">**AzureVMSqlServerAutoBackupConfig** CMDLET은 SQL Server 자동 백업에 대 한 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a3415-108">The **New-AzureVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="a3415-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a3415-109">EXAMPLES</span></span>

### <span data-ttu-id="a3415-110">예제 1: 저장소 URI 및 계정 키를 사용 하 여 자동 백업 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="a3415-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="a3415-111">이 명령은 저장소 URI 및 계정 키를 지정 하 여 자동 백업 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a3415-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="a3415-112">자동 백업을 사용할 수 있으며 자동 백업이 10 일 동안 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3415-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="a3415-113">명령이 $AutoBackupConfig 변수에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3415-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="a3415-114">Set-AzureRmVMSqlServerExtension cmdlet 등의 다른 cmdlet에 대해이 구성 항목을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3415-114">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="a3415-115">예제 2: 저장소 컨텍스트를 사용 하 여 자동 백업 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="a3415-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="a3415-116">첫 번째 명령은 저장소 컨텍스트를 만든 다음 $StorageContext 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3415-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="a3415-117">자세한 내용은 새 AzureStorageContext를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a3415-117">For more information, see New-AzureStorageContext.</span></span>

<span data-ttu-id="a3415-118">두 번째 명령은 $StorageContext에서 저장소 컨텍스트를 지정 하 여 자동 백업 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a3415-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="a3415-119">자동 백업을 사용할 수 있으며 자동 백업이 10 일 동안 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3415-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="a3415-120">예제 3: 암호화 및 암호를 사용 하 여 저장소 컨텍스트를 사용 하 여 자동 백업 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="a3415-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="a3415-121">이 명령은 자동 백업 구성 개체를 만들고 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3415-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="a3415-122">명령은 이전 예제에서 만든 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3415-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="a3415-123">명령이 암호로 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3415-123">The command enables encryption with password.</span></span>
<span data-ttu-id="a3415-124">암호가 이전에 $CertificatePassword 변수에 보안 문자열로 저장 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a3415-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="a3415-125">보안 문자열을 만들려면 ConvertTo-SecureString cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3415-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="a3415-126">변수</span><span class="sxs-lookup"><span data-stu-id="a3415-126">PARAMETERS</span></span>

### <span data-ttu-id="a3415-127">-사용</span><span class="sxs-lookup"><span data-stu-id="a3415-127">-Enable</span></span>
<span data-ttu-id="a3415-128">SQL Server 가상 컴퓨터에 대해 자동화 된 백업을 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a3415-128">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="a3415-129">이 매개 변수를 지정 하면 자동 백업이 모든 현재 및 새 데이터베이스에 대 한 백업 일정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3415-129">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="a3415-130">이렇게 하면 관리 되는 백업 설정이 다음 일정을 따라 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3415-130">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3415-131">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="a3415-131">-RetentionPeriodInDays</span></span>
<span data-ttu-id="a3415-132">백업을 유지할 일 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3415-132">Specifies the number of days to retain a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3415-133">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="a3415-133">-EnableEncryption</span></span>
<span data-ttu-id="a3415-134">이 cmdlet이 암호화를 사용 하도록 설정 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a3415-134">Indicates that this cmdlet enables encryption.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3415-135">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="a3415-135">-CertificatePassword</span></span>
<span data-ttu-id="a3415-136">SQL Server 암호화 백업을 수행 하는 데 사용 되는 인증서를 암호화 하는 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3415-136">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3415-137">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="a3415-137">-StorageUri</span></span>
<span data-ttu-id="a3415-138">Blob 저장소 계정의 URI (Uniform Resource Identifier)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3415-138">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3415-139">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="a3415-139">-StorageKey</span></span>
<span data-ttu-id="a3415-140">Blob 저장소 계정의 저장소 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3415-140">Specifies the storage key of the blob storage account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3415-141">-프로필</span><span class="sxs-lookup"><span data-stu-id="a3415-141">-Profile</span></span>
<span data-ttu-id="a3415-142">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3415-142">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="a3415-143">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="a3415-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Utilities.Common.AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3415-144">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a3415-144">-InformationAction</span></span>
<span data-ttu-id="a3415-145">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="a3415-145">@{Text=}</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3415-146">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a3415-146">-InformationVariable</span></span>
<span data-ttu-id="a3415-147">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="a3415-147">@{Text=}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3415-148">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="a3415-148">-StorageContext</span></span>
<span data-ttu-id="a3415-149">백업을 저장 하는 데 사용 되는 저장소 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3415-149">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="a3415-150">**Azurestoragecontext** 개체를 가져오려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3415-150">To obtain an **AzureStorageContext** object, use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="a3415-151">기본값은 SQL Server 가상 컴퓨터와 연결 된 저장소 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="a3415-151">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3415-152">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="a3415-152">-BackupScheduleType</span></span>
<span data-ttu-id="a3415-153">백업 일정 유형, 수동 또는 자동</span><span class="sxs-lookup"><span data-stu-id="a3415-153">Backup schedule type, manual or automated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3415-154">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="a3415-154">-BackupSystemDbs</span></span>
<span data-ttu-id="a3415-155">시스템 데이터베이스 백업</span><span class="sxs-lookup"><span data-stu-id="a3415-155">Backup system databases</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3415-156">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="a3415-156">-FullBackupFrequency</span></span>
<span data-ttu-id="a3415-157">Sql Server 전체 백업 빈도 (매일 또는 주)</span><span class="sxs-lookup"><span data-stu-id="a3415-157">Sql Server Full Backup frequency, daily or week</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3415-158">-Fullbackupstarth</span><span class="sxs-lookup"><span data-stu-id="a3415-158">-FullBackupStartHour</span></span>
<span data-ttu-id="a3415-159">Sql Server 전체 백업을 시작 해야 하는 날짜의 시간 (0-23)</span><span class="sxs-lookup"><span data-stu-id="a3415-159">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3415-160">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="a3415-160">-FullBackupWindowInHours</span></span>
<span data-ttu-id="a3415-161">Sql Server 전체 백업 창 (시간)</span><span class="sxs-lookup"><span data-stu-id="a3415-161">Sql Server Full Backup window in hours</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3415-162">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="a3415-162">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="a3415-163">Sql Server 로그 백업 빈도 (1-60 분 마다 한 번)</span><span class="sxs-lookup"><span data-stu-id="a3415-163">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3415-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3415-164">CommonParameters</span></span>
<span data-ttu-id="a3415-165">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3415-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3415-166">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3415-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3415-167">입력</span><span class="sxs-lookup"><span data-stu-id="a3415-167">INPUTS</span></span>

## <span data-ttu-id="a3415-168">출력</span><span class="sxs-lookup"><span data-stu-id="a3415-168">OUTPUTS</span></span>

## <span data-ttu-id="a3415-169">상속자</span><span class="sxs-lookup"><span data-stu-id="a3415-169">NOTES</span></span>

## <span data-ttu-id="a3415-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a3415-170">RELATED LINKS</span></span>

[<span data-ttu-id="a3415-171">새로운 AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="a3415-171">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="a3415-172">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="a3415-172">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


