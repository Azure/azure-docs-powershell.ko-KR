---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautobackupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: 952a9160a20492fe49e7f79019ca68e3bc241e57
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331370"
---
# <span data-ttu-id="0e8ac-101">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="0e8ac-101">New-AzVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="0e8ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e8ac-102">SYNOPSIS</span></span>
<span data-ttu-id="0e8ac-103">자동 백업에 대한 SQL Server 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ac-103">Creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="0e8ac-104">구문</span><span class="sxs-lookup"><span data-stu-id="0e8ac-104">SYNTAX</span></span>

### <span data-ttu-id="0e8ac-105">StorageUriSqlServerAutoBackup(기본값)</span><span class="sxs-lookup"><span data-stu-id="0e8ac-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e8ac-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="0e8ac-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageContext] <IStorageContext>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e8ac-107">설명</span><span class="sxs-lookup"><span data-stu-id="0e8ac-107">DESCRIPTION</span></span>
<span data-ttu-id="0e8ac-108">**New-AzVMSqlServerAutoBackupConfig** cmdlet은 자동 백업에 대한 SQL Server 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ac-108">The **New-AzVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="0e8ac-109">예제</span><span class="sxs-lookup"><span data-stu-id="0e8ac-109">EXAMPLES</span></span>

### <span data-ttu-id="0e8ac-110">예제 1: 저장소 URI 및 계정 키를 사용하여 자동 백업 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="0e8ac-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="0e8ac-111">이 명령은 저장소 URI 및 계정 키를 지정하여 자동 백업 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ac-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="0e8ac-112">자동 백업이 사용하도록 설정되어 있으며 자동 백업은 10일 동안 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ac-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="0e8ac-113">이 명령은 결과 값을 $AutoBackupConfig 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ac-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="0e8ac-114">Set-AzVMSqlServerExtension cmdlet과 같은 다른 cmdlet에 대해 이 구성 항목을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ac-114">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="0e8ac-115">예제 2: 저장소 컨텍스트를 사용하여 자동 백업 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="0e8ac-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="0e8ac-116">첫 번째 명령은 저장소 컨텍스트를 만든 다음 저장소 $StorageContext 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ac-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="0e8ac-117">자세한 내용은 New-AzStorageContext를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0e8ac-117">For more information, see New-AzStorageContext.</span></span>
<span data-ttu-id="0e8ac-118">두 번째 명령은 저장소 컨텍스트를 지정하여 자동 백업 구성 개체를 $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="0e8ac-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="0e8ac-119">자동 백업이 사용하도록 설정되어 있으며 자동 백업은 10일 동안 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ac-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="0e8ac-120">예제 3: 암호화 및 암호가 있는 저장소 컨텍스트를 사용하여 자동 백업 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="0e8ac-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="0e8ac-121">이 명령은 자동 백업 구성 개체를 만들고 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ac-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="0e8ac-122">이 명령은 이전 예제에서 만든 저장소 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ac-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="0e8ac-123">이 명령은 암호로 암호화를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ac-123">The command enables encryption with password.</span></span>
<span data-ttu-id="0e8ac-124">암호는 이전에 $CertificatePassword 변수에 보안 문자열로 $CertificatePassword.</span><span class="sxs-lookup"><span data-stu-id="0e8ac-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="0e8ac-125">보안 문자열을 만들 경우 ConvertTo-SecureString cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ac-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="0e8ac-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e8ac-126">PARAMETERS</span></span>

### <span data-ttu-id="0e8ac-127">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="0e8ac-127">-BackupScheduleType</span></span>
<span data-ttu-id="0e8ac-128">Backup 일정 유형, 수동 또는 자동화</span><span class="sxs-lookup"><span data-stu-id="0e8ac-128">Backup schedule type, manual or automated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Manual, Automated

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e8ac-129">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="0e8ac-129">-BackupSystemDbs</span></span>
<span data-ttu-id="0e8ac-130">시스템 데이터베이스 백업</span><span class="sxs-lookup"><span data-stu-id="0e8ac-130">Backup system databases</span></span>

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

### <span data-ttu-id="0e8ac-131">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="0e8ac-131">-CertificatePassword</span></span>
<span data-ttu-id="0e8ac-132">암호화된 백업을 수행하는 데 사용되는 인증서를 암호화하는 SQL Server 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ac-132">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e8ac-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e8ac-133">-DefaultProfile</span></span>
<span data-ttu-id="0e8ac-134">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ac-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e8ac-135">-Enable</span><span class="sxs-lookup"><span data-stu-id="0e8ac-135">-Enable</span></span>
<span data-ttu-id="0e8ac-136">가상 머신에 대한 자동화된 SQL Server 사용하도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ac-136">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="0e8ac-137">이 매개 변수를 지정하는 경우 자동화된 백업은 모든 현재 및 새 데이터베이스에 대한 백업 일정을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ac-137">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="0e8ac-138">그러면 이 일정에 따라 관리되는 Backup 설정이 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ac-138">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e8ac-139">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="0e8ac-139">-EnableEncryption</span></span>
<span data-ttu-id="0e8ac-140">이 cmdlet에서 암호화를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ac-140">Indicates that this cmdlet enables encryption.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e8ac-141">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="0e8ac-141">-FullBackupFrequency</span></span>
<span data-ttu-id="0e8ac-142">Sql Server 전체 백업 빈도( 매일 또는 매주)</span><span class="sxs-lookup"><span data-stu-id="0e8ac-142">Sql Server Full Backup frequency, daily or weekly</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Daily, Weekly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e8ac-143">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="0e8ac-143">-FullBackupStartHour</span></span>
<span data-ttu-id="0e8ac-144">Sql Server 전체 백업이 시작되는 하루 중 시간(0-23)</span><span class="sxs-lookup"><span data-stu-id="0e8ac-144">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

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

### <span data-ttu-id="0e8ac-145">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="0e8ac-145">-FullBackupWindowInHours</span></span>
<span data-ttu-id="0e8ac-146">Sql Server 전체 백업 창(시간)</span><span class="sxs-lookup"><span data-stu-id="0e8ac-146">Sql Server Full Backup window in hours</span></span>

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

### <span data-ttu-id="0e8ac-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="0e8ac-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="0e8ac-148">Sql Server 로그 백업 빈도(1-60분마다 한 번)</span><span class="sxs-lookup"><span data-stu-id="0e8ac-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

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

### <span data-ttu-id="0e8ac-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e8ac-149">-ResourceGroupName</span></span>
<span data-ttu-id="0e8ac-150">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ac-150">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e8ac-151">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="0e8ac-151">-RetentionPeriodInDays</span></span>
<span data-ttu-id="0e8ac-152">백업을 유지할 일 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ac-152">Specifies the number of days to retain a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e8ac-153">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="0e8ac-153">-StorageContext</span></span>
<span data-ttu-id="0e8ac-154">백업을 저장하는 데 사용할 저장소 계정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ac-154">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="0e8ac-155">**AzureStorageContext** 개체를 얻습니다. New-AzStorageContext cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ac-155">To obtain an **AzureStorageContext** object, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="0e8ac-156">기본값은 가상 머신의 가상 머신과 연결된 SQL Server 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ac-156">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e8ac-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="0e8ac-157">-StorageKey</span></span>
<span data-ttu-id="0e8ac-158">Blob Storage 계정의 스토리지 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ac-158">Specifies the storage key of the blob storage account.</span></span>

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

### <span data-ttu-id="0e8ac-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="0e8ac-159">-StorageUri</span></span>
<span data-ttu-id="0e8ac-160">Blob Storage 계정의 URI(Uniform Resource Identifier)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ac-160">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

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

### <span data-ttu-id="0e8ac-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e8ac-161">CommonParameters</span></span>
<span data-ttu-id="0e8ac-162">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0e8ac-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e8ac-163">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0e8ac-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e8ac-164">입력</span><span class="sxs-lookup"><span data-stu-id="0e8ac-164">INPUTS</span></span>

### <span data-ttu-id="0e8ac-165">System.String</span><span class="sxs-lookup"><span data-stu-id="0e8ac-165">System.String</span></span>

### <span data-ttu-id="0e8ac-166">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0e8ac-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="0e8ac-167">System.Int32</span><span class="sxs-lookup"><span data-stu-id="0e8ac-167">System.Int32</span></span>

### <span data-ttu-id="0e8ac-168">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0e8ac-168">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="0e8ac-169">System.Uri</span><span class="sxs-lookup"><span data-stu-id="0e8ac-169">System.Uri</span></span>

### <span data-ttu-id="0e8ac-170">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="0e8ac-170">System.Security.SecureString</span></span>

### <span data-ttu-id="0e8ac-171">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0e8ac-171">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="0e8ac-172">출력</span><span class="sxs-lookup"><span data-stu-id="0e8ac-172">OUTPUTS</span></span>

### <span data-ttu-id="0e8ac-173">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="0e8ac-173">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

## <span data-ttu-id="0e8ac-174">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0e8ac-174">NOTES</span></span>

## <span data-ttu-id="0e8ac-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0e8ac-175">RELATED LINKS</span></span>

[<span data-ttu-id="0e8ac-176">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="0e8ac-176">New-AzVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="0e8ac-177">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="0e8ac-177">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)

