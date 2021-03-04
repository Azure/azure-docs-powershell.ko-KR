---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmsqlserverautobackupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: 6d9047679f4286e0e2212ca8e599237825326dd7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975920"
---
# <span data-ttu-id="45635-101">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="45635-101">New-AzVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="45635-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45635-102">SYNOPSIS</span></span>
<span data-ttu-id="45635-103">자동 백업에 SQL Server 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="45635-103">Creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="45635-104">구문</span><span class="sxs-lookup"><span data-stu-id="45635-104">SYNTAX</span></span>

### <span data-ttu-id="45635-105">StorageUriSqlServerAutoBackup(기본값)</span><span class="sxs-lookup"><span data-stu-id="45635-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45635-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="45635-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageContext] <IStorageContext>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45635-107">설명</span><span class="sxs-lookup"><span data-stu-id="45635-107">DESCRIPTION</span></span>
<span data-ttu-id="45635-108">**New-AzVMSqlServerAutoBackupConfig** cmdlet은 자동 백업을 위한 구성 SQL Server 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="45635-108">The **New-AzVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="45635-109">예제</span><span class="sxs-lookup"><span data-stu-id="45635-109">EXAMPLES</span></span>

### <span data-ttu-id="45635-110">예제 1: 저장소 URI 및 계정 키를 사용하여 자동 백업 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="45635-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="45635-111">이 명령은 저장소 URI 및 계정 키를 지정하여 자동 백업 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="45635-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="45635-112">자동 백업이 활성화되어 있으며 자동 백업은 10일 동안 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="45635-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="45635-113">명령은 결과를 $AutoBackupConfig 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="45635-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="45635-114">다른 cmdlet(예: cmdlet)에 대해 이 Set-AzVMSqlServerExtension 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="45635-114">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="45635-115">예제 2: 저장소 컨텍스트를 사용하여 자동 백업 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="45635-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="45635-116">첫 번째 명령은 저장소 컨텍스트를 만든 다음, 저장소 $StorageContext 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="45635-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="45635-117">자세한 내용은 New-AzStorageContext를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="45635-117">For more information, see New-AzStorageContext.</span></span>
<span data-ttu-id="45635-118">두 번째 명령은 저장소 컨텍스트를 지정하여 자동 백업 구성 개체를 $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="45635-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="45635-119">자동 백업이 활성화되어 있으며 자동 백업은 10일 동안 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="45635-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="45635-120">예제 3: 암호화 및 암호로 저장소 컨텍스트를 사용하여 자동 백업 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="45635-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="45635-121">이 명령은 자동 백업 구성 개체를 만들고 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="45635-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="45635-122">명령은 이전 예제에서 만든 저장소 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="45635-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="45635-123">이 명령은 암호로 암호화를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="45635-123">The command enables encryption with password.</span></span>
<span data-ttu-id="45635-124">암호는 이전에 보안 문자열로 저장되어 $CertificatePassword 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="45635-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="45635-125">보안 문자열을 만들 경우 ConvertTo-SecureString cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="45635-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="45635-126">매개 변수</span><span class="sxs-lookup"><span data-stu-id="45635-126">PARAMETERS</span></span>

### <span data-ttu-id="45635-127">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="45635-127">-BackupScheduleType</span></span>
<span data-ttu-id="45635-128">백업 일정 유형, 수동 또는 자동화</span><span class="sxs-lookup"><span data-stu-id="45635-128">Backup schedule type, manual or automated</span></span>

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

### <span data-ttu-id="45635-129">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="45635-129">-BackupSystemDbs</span></span>
<span data-ttu-id="45635-130">백업 시스템 데이터베이스</span><span class="sxs-lookup"><span data-stu-id="45635-130">Backup system databases</span></span>

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

### <span data-ttu-id="45635-131">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="45635-131">-CertificatePassword</span></span>
<span data-ttu-id="45635-132">암호화된 백업을 수행하는 데 사용되는 인증서를 암호화하는 SQL Server 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="45635-132">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

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

### <span data-ttu-id="45635-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45635-133">-DefaultProfile</span></span>
<span data-ttu-id="45635-134">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="45635-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45635-135">-사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="45635-135">-Enable</span></span>
<span data-ttu-id="45635-136">가상 머신에 대한 자동화된 백업을 SQL Server 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="45635-136">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="45635-137">이 매개 변수를 지정하면 자동화된 백업은 모든 현재 및 새 데이터베이스에 대한 백업 일정을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="45635-137">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="45635-138">이 일정에 따라 Managed Backup 설정이 업데이트됩니다.</span><span class="sxs-lookup"><span data-stu-id="45635-138">This updates your Managed Backup settings to follow this schedule.</span></span>

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

### <span data-ttu-id="45635-139">-enableEncryption</span><span class="sxs-lookup"><span data-stu-id="45635-139">-EnableEncryption</span></span>
<span data-ttu-id="45635-140">이 cmdlet에서 암호화를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="45635-140">Indicates that this cmdlet enables encryption.</span></span>

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

### <span data-ttu-id="45635-141">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="45635-141">-FullBackupFrequency</span></span>
<span data-ttu-id="45635-142">Sql Server 전체 백업 빈도( 매일 또는 매주)</span><span class="sxs-lookup"><span data-stu-id="45635-142">Sql Server Full Backup frequency, daily or weekly</span></span>

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

### <span data-ttu-id="45635-143">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="45635-143">-FullBackupStartHour</span></span>
<span data-ttu-id="45635-144">Sql Server 전체 백업을 시작해야 하는 하루 중 시간(0-23)입니다.</span><span class="sxs-lookup"><span data-stu-id="45635-144">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

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

### <span data-ttu-id="45635-145">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="45635-145">-FullBackupWindowInHours</span></span>
<span data-ttu-id="45635-146">Sql Server 전체 백업 기간(몇 시간)</span><span class="sxs-lookup"><span data-stu-id="45635-146">Sql Server Full Backup window in hours</span></span>

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

### <span data-ttu-id="45635-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="45635-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="45635-148">Sql Server Log Backup 빈도(1-60분마다 한 번씩)</span><span class="sxs-lookup"><span data-stu-id="45635-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

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

### <span data-ttu-id="45635-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45635-149">-ResourceGroupName</span></span>
<span data-ttu-id="45635-150">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="45635-150">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="45635-151">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="45635-151">-RetentionPeriodInDays</span></span>
<span data-ttu-id="45635-152">백업을 유지할 일 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="45635-152">Specifies the number of days to retain a backup.</span></span>

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

### <span data-ttu-id="45635-153">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="45635-153">-StorageContext</span></span>
<span data-ttu-id="45635-154">백업을 저장하는 데 사용할 저장소 계정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="45635-154">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="45635-155">**AzureStorageContext** 개체를 얻은 경우 New-AzStorageContext cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="45635-155">To obtain an **AzureStorageContext** object, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="45635-156">기본값은 가상 머신과 연결된 SQL Server 계정입니다.</span><span class="sxs-lookup"><span data-stu-id="45635-156">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

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

### <span data-ttu-id="45635-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="45635-157">-StorageKey</span></span>
<span data-ttu-id="45635-158">Blob Storage 계정의 저장소 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="45635-158">Specifies the storage key of the blob storage account.</span></span>

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

### <span data-ttu-id="45635-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="45635-159">-StorageUri</span></span>
<span data-ttu-id="45635-160">Blob Storage 계정의 URI(균일한 리소스 식별자)를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="45635-160">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

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

### <span data-ttu-id="45635-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45635-161">CommonParameters</span></span>
<span data-ttu-id="45635-162">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="45635-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45635-163">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="45635-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45635-164">입력</span><span class="sxs-lookup"><span data-stu-id="45635-164">INPUTS</span></span>

### <span data-ttu-id="45635-165">System.String</span><span class="sxs-lookup"><span data-stu-id="45635-165">System.String</span></span>

### <span data-ttu-id="45635-166">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="45635-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="45635-167">System.Int32</span><span class="sxs-lookup"><span data-stu-id="45635-167">System.Int32</span></span>

### <span data-ttu-id="45635-168">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="45635-168">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="45635-169">System.Uri</span><span class="sxs-lookup"><span data-stu-id="45635-169">System.Uri</span></span>

### <span data-ttu-id="45635-170">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="45635-170">System.Security.SecureString</span></span>

### <span data-ttu-id="45635-171">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="45635-171">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="45635-172">출력</span><span class="sxs-lookup"><span data-stu-id="45635-172">OUTPUTS</span></span>

### <span data-ttu-id="45635-173">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="45635-173">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

## <span data-ttu-id="45635-174">참고 사항</span><span class="sxs-lookup"><span data-stu-id="45635-174">NOTES</span></span>

## <span data-ttu-id="45635-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="45635-175">RELATED LINKS</span></span>

[<span data-ttu-id="45635-176">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="45635-176">New-AzVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="45635-177">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="45635-177">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


