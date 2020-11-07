---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmsqlserverautobackupconfig
schema: 2.0.0
ms.openlocfilehash: bb00a3e4fc953510d2ec32b7c213d07d6c8801c3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882685"
---
# <span data-ttu-id="a1c81-101">New-AzureRmVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="a1c81-101">New-AzureRmVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="a1c81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1c81-102">SYNOPSIS</span></span>
<span data-ttu-id="a1c81-103">SQL Server 자동 백업에 대 한 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a1c81-103">Creates a configuration object for SQL Server automatic backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1c81-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a1c81-104">SYNTAX</span></span>

### <span data-ttu-id="a1c81-105">StorageUriSqlServerAutoBackup (기본값)</span><span class="sxs-lookup"><span data-stu-id="a1c81-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzureRmVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1c81-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="a1c81-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzureRmVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageContext] <IStorageContext>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs]
 [-BackupScheduleType <String>] [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>]
 [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1c81-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a1c81-107">DESCRIPTION</span></span>
<span data-ttu-id="a1c81-108">**AzureRmVMSqlServerAutoBackupConfig** CMDLET은 SQL Server 자동 백업에 대 한 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a1c81-108">The **New-AzureRmVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="a1c81-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a1c81-109">EXAMPLES</span></span>

### <span data-ttu-id="a1c81-110">예제 1: 저장소 URI 및 계정 키를 사용 하 여 자동 백업 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="a1c81-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureRmVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="a1c81-111">이 명령은 저장소 URI 및 계정 키를 지정 하 여 자동 백업 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a1c81-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="a1c81-112">자동 백업을 사용할 수 있으며 자동 백업이 10 일 동안 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a1c81-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="a1c81-113">명령이 $AutoBackupConfig 변수에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1c81-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="a1c81-114">Set-AzureRmVMSqlServerExtension cmdlet 등의 다른 cmdlet에 대해이 구성 항목을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a1c81-114">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="a1c81-115">예제 2: 저장소 컨텍스트를 사용 하 여 자동 백업 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="a1c81-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzureRmVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="a1c81-116">첫 번째 명령은 저장소 컨텍스트를 만든 다음 $StorageContext 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1c81-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="a1c81-117">자세한 내용은 새 AzureStorageContext를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a1c81-117">For more information, see New-AzureStorageContext.</span></span>

<span data-ttu-id="a1c81-118">두 번째 명령은 $StorageContext에서 저장소 컨텍스트를 지정 하 여 자동 백업 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a1c81-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="a1c81-119">자동 백업을 사용할 수 있으며 자동 백업이 10 일 동안 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a1c81-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="a1c81-120">예제 3: 암호화 및 암호를 사용 하 여 저장소 컨텍스트를 사용 하 여 자동 백업 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="a1c81-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzureRmVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="a1c81-121">이 명령은 자동 백업 구성 개체를 만들고 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1c81-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="a1c81-122">명령은 이전 예제에서 만든 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1c81-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="a1c81-123">명령이 암호로 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1c81-123">The command enables encryption with password.</span></span>
<span data-ttu-id="a1c81-124">암호가 이전에 $CertificatePassword 변수에 보안 문자열로 저장 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a1c81-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="a1c81-125">보안 문자열을 만들려면 ConvertTo-SecureString cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1c81-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="a1c81-126">변수</span><span class="sxs-lookup"><span data-stu-id="a1c81-126">PARAMETERS</span></span>

### <span data-ttu-id="a1c81-127">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="a1c81-127">-BackupScheduleType</span></span>
<span data-ttu-id="a1c81-128">백업 일정 유형, 수동 또는 자동</span><span class="sxs-lookup"><span data-stu-id="a1c81-128">Backup schedule type, manual or automated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Manual, Automated

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1c81-129">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="a1c81-129">-BackupSystemDbs</span></span>
<span data-ttu-id="a1c81-130">시스템 데이터베이스 백업</span><span class="sxs-lookup"><span data-stu-id="a1c81-130">Backup system databases</span></span>

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

### <span data-ttu-id="a1c81-131">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="a1c81-131">-CertificatePassword</span></span>
<span data-ttu-id="a1c81-132">SQL Server 암호화 백업을 수행 하는 데 사용 되는 인증서를 암호화 하는 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1c81-132">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c81-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1c81-133">-DefaultProfile</span></span>
<span data-ttu-id="a1c81-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a1c81-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1c81-135">-사용</span><span class="sxs-lookup"><span data-stu-id="a1c81-135">-Enable</span></span>
<span data-ttu-id="a1c81-136">SQL Server 가상 컴퓨터에 대해 자동화 된 백업을 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a1c81-136">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="a1c81-137">이 매개 변수를 지정 하면 자동 백업이 모든 현재 및 새 데이터베이스에 대 한 백업 일정을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1c81-137">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="a1c81-138">이렇게 하면 관리 되는 백업 설정이 다음 일정을 따라 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a1c81-138">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1c81-139">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="a1c81-139">-EnableEncryption</span></span>
<span data-ttu-id="a1c81-140">이 cmdlet이 암호화를 사용 하도록 설정 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a1c81-140">Indicates that this cmdlet enables encryption.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1c81-141">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="a1c81-141">-FullBackupFrequency</span></span>
<span data-ttu-id="a1c81-142">Sql Server 전체 백업 빈도 (매일 또는 매주)</span><span class="sxs-lookup"><span data-stu-id="a1c81-142">Sql Server Full Backup frequency, daily or weekly</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Daily, Weekly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1c81-143">-Fullbackupstarth</span><span class="sxs-lookup"><span data-stu-id="a1c81-143">-FullBackupStartHour</span></span>
<span data-ttu-id="a1c81-144">Sql Server 전체 백업을 시작 해야 하는 날짜의 시간 (0-23)</span><span class="sxs-lookup"><span data-stu-id="a1c81-144">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

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

### <span data-ttu-id="a1c81-145">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="a1c81-145">-FullBackupWindowInHours</span></span>
<span data-ttu-id="a1c81-146">Sql Server 전체 백업 창 (시간)</span><span class="sxs-lookup"><span data-stu-id="a1c81-146">Sql Server Full Backup window in hours</span></span>

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

### <span data-ttu-id="a1c81-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="a1c81-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="a1c81-148">Sql Server 로그 백업 빈도 (1-60 분 마다 한 번)</span><span class="sxs-lookup"><span data-stu-id="a1c81-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

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

### <span data-ttu-id="a1c81-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1c81-149">-ResourceGroupName</span></span>
<span data-ttu-id="a1c81-150">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1c81-150">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1c81-151">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="a1c81-151">-RetentionPeriodInDays</span></span>
<span data-ttu-id="a1c81-152">백업을 유지할 일 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1c81-152">Specifies the number of days to retain a backup.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1c81-153">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="a1c81-153">-StorageContext</span></span>
<span data-ttu-id="a1c81-154">백업을 저장 하는 데 사용 되는 저장소 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1c81-154">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="a1c81-155">**Azurestoragecontext** 개체를 가져오려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1c81-155">To obtain an **AzureStorageContext** object, use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="a1c81-156">기본값은 SQL Server 가상 컴퓨터와 연결 된 저장소 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="a1c81-156">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1c81-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="a1c81-157">-StorageKey</span></span>
<span data-ttu-id="a1c81-158">Blob 저장소 계정의 저장소 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1c81-158">Specifies the storage key of the blob storage account.</span></span>

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

### <span data-ttu-id="a1c81-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="a1c81-159">-StorageUri</span></span>
<span data-ttu-id="a1c81-160">Blob 저장소 계정의 URI (Uniform Resource Identifier)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1c81-160">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

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

### <span data-ttu-id="a1c81-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1c81-161">CommonParameters</span></span>
<span data-ttu-id="a1c81-162">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1c81-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1c81-163">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1c81-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1c81-164">입력</span><span class="sxs-lookup"><span data-stu-id="a1c81-164">INPUTS</span></span>

### <span data-ttu-id="a1c81-165">않아야</span><span class="sxs-lookup"><span data-stu-id="a1c81-165">None</span></span>
<span data-ttu-id="a1c81-166">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a1c81-166">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a1c81-167">출력</span><span class="sxs-lookup"><span data-stu-id="a1c81-167">OUTPUTS</span></span>

### <span data-ttu-id="a1c81-168">AutoBackupSettings를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1c81-168">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

## <span data-ttu-id="a1c81-169">상속자</span><span class="sxs-lookup"><span data-stu-id="a1c81-169">NOTES</span></span>

## <span data-ttu-id="a1c81-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a1c81-170">RELATED LINKS</span></span>



[<span data-ttu-id="a1c81-171">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="a1c81-171">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


