---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3A7B0280-CE6E-4374-87AF-4C1015EB88FA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 803299a64fb98aecc249bc7bb2f505ada74a5573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535492"
---
# <span data-ttu-id="f7b6d-101">New-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f7b6d-101">New-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="f7b6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7b6d-102">SYNOPSIS</span></span>
<span data-ttu-id="f7b6d-103">백업 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-103">Creates a Backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7b6d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f7b6d-104">SYNTAX</span></span>

### <span data-ttu-id="f7b6d-105">NoScheduleParamSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f7b6d-105">NoScheduleParamSet (Default)</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-BackupTime] <DateTime>
 [[-DaysOfWeek] <String[]>] [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7b6d-106">DailyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="f7b6d-106">DailyScheduleParamSet</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Daily] [-BackupTime] <DateTime>
 [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7b6d-107">WeeklyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="f7b6d-107">WeeklyScheduleParamSet</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Weekly] [-BackupTime] <DateTime>
 [-DaysOfWeek] <String[]> [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7b6d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f7b6d-108">DESCRIPTION</span></span>
<span data-ttu-id="f7b6d-109">**AzureRmBackupProtectionPolicy** cmdlet는 azure Backup 정책을 azure PowerShell 개체로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-109">The **New-AzureRmBackupProtectionPolicy** cmdlet creates an Azure Backup policy as an Azure PowerShell object.</span></span>

<span data-ttu-id="f7b6d-110">백업 정책은 백업이 항목을 얼마나 자주 백업 하는 지를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-110">A backup policy defines when and how often Backup backs up an item.</span></span>
<span data-ttu-id="f7b6d-111">Enable-AzureRmBackupProtection cmdlet은 백업 정책을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-111">The Enable-AzureRmBackupProtection cmdlet uses a backup policy.</span></span>

## <span data-ttu-id="f7b6d-112">예제의</span><span class="sxs-lookup"><span data-stu-id="f7b6d-112">EXAMPLES</span></span>

### <span data-ttu-id="f7b6d-113">예제 1: 일일 및 월간 보존을 사용 하 여 일일 백업 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="f7b6d-113">Example 1: Create a daily backup policy with daily and monthly retention</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Monthly = New-AzureRmBackupRetentionPolicyObject -MonthlyRetentionInDailyFormat -DaysOfMonth (10, 20) -Retention 12
PS C:\> $ProtectionPolicy = New-AzureRmBackupProtectionPolicy -Name DailyBackup01 -Type AzureVM -Daily -BackupTime ([datetime]"3:30 PM") -RetentionPolicy ($Daily,$Monthly) -Vault $Vault
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
DailyBkp                  AzureVM            Daily              26-Aug-15 3:00:00 PM
```

<span data-ttu-id="f7b6d-114">첫 번째 명령은 Get-AzureRmBackupVault cmdlet을 사용 하 여 Vault03 이라는 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-114">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="f7b6d-115">명령이 $Vault 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-115">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="f7b6d-116">두 번째 명령은 일일 보존 기간에 30 일간 보존 정책을 만든 다음 $Daily 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-116">The second command creates a retention policy for 30 days of daily retention, and then stores it in the $Daily variable.</span></span>

<span data-ttu-id="f7b6d-117">세 번째 명령은 각 월의 10 번째/20 개월 동안 백업을 유지 하는 보존 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-117">The third command creates a retention policy that keeps the backup on the tenth and the twentieth of each month for twelve months.</span></span>
<span data-ttu-id="f7b6d-118">명령은 보존 정책을 $Monthly 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-118">The command stores the retention policy in the $Monthly variable.</span></span>

<span data-ttu-id="f7b6d-119">마지막 명령은 일일 백업 시간이 3:00 PM 인 $Vault의 자격 증명 모음에 대 한 백업 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-119">The final command creates a backup policy for the vault in $Vault that has a daily backup time of 3:00 PM.</span></span>
<span data-ttu-id="f7b6d-120">이 명령은 $Daily 및 $Monthly에 저장 된 보존 정책을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-120">The command assigns the retention policies stored in $Daily and $Monthly.</span></span>
<span data-ttu-id="f7b6d-121">명령이 $ProtectionPolicy 변수에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-121">The command stores the result in the $ProtectionPolicy variable.</span></span>

## <span data-ttu-id="f7b6d-122">변수</span><span class="sxs-lookup"><span data-stu-id="f7b6d-122">PARAMETERS</span></span>

### <span data-ttu-id="f7b6d-123">백 가동 시간</span><span class="sxs-lookup"><span data-stu-id="f7b6d-123">-BackupTime</span></span>
<span data-ttu-id="f7b6d-124">백업 작업에 대 한 시간을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-124">Specifies the time of day, as a **DateTime** object, for the backup operation.</span></span>
<span data-ttu-id="f7b6d-125">**DateTime** 을 얻으려면 Get-Date cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-125">To obtain a **DateTime** , use the Get-Date cmdlet.</span></span>
<span data-ttu-id="f7b6d-126">**DateTime** 개체에 대 한 자세한 내용은를 입력 `Get-Help Get-Date` 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-126">For information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7b6d-127">-매일</span><span class="sxs-lookup"><span data-stu-id="f7b6d-127">-Daily</span></span>
<span data-ttu-id="f7b6d-128">백업 작업이 일별 일정에 실행 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-128">Indicates that the backup operation runs on a Daily schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7b6d-129">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="f7b6d-129">-DaysOfWeek</span></span>
<span data-ttu-id="f7b6d-130">요일의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-130">Specifies an array of days of the week.</span></span>
<span data-ttu-id="f7b6d-131">이 정책은이 매개 변수에 지정 된 일 동안 백업을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-131">This policy runs backups on the days specified by this parameter.</span></span>
<span data-ttu-id="f7b6d-132">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f7b6d-133">월요일</span><span class="sxs-lookup"><span data-stu-id="f7b6d-133">Monday</span></span> 
- <span data-ttu-id="f7b6d-134">시간은</span><span class="sxs-lookup"><span data-stu-id="f7b6d-134">Tuesday</span></span> 
- <span data-ttu-id="f7b6d-135">일</span><span class="sxs-lookup"><span data-stu-id="f7b6d-135">Wednesday</span></span> 
- <span data-ttu-id="f7b6d-136">목요일</span><span class="sxs-lookup"><span data-stu-id="f7b6d-136">Thursday</span></span> 
- <span data-ttu-id="f7b6d-137">금요일</span><span class="sxs-lookup"><span data-stu-id="f7b6d-137">Friday</span></span> 
- <span data-ttu-id="f7b6d-138">토요일</span><span class="sxs-lookup"><span data-stu-id="f7b6d-138">Saturday</span></span> 
- <span data-ttu-id="f7b6d-139">나타내고</span><span class="sxs-lookup"><span data-stu-id="f7b6d-139">Sunday</span></span>

<span data-ttu-id="f7b6d-140">*주간* 매개 변수를 지정 하는 경우이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-140">If you specify the *Weekly* parameter, specify this parameter.</span></span>

```yaml
Type: System.String[]
Parameter Sets: NoScheduleParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7b6d-141">-이름</span><span class="sxs-lookup"><span data-stu-id="f7b6d-141">-Name</span></span>
<span data-ttu-id="f7b6d-142">백업 정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-142">Specifies a name for the backup policy.</span></span>
<span data-ttu-id="f7b6d-143">자격 증명 모음에서 고유한 이름을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-143">Select a name that is unique in the vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7b6d-144">-보존 정책</span><span class="sxs-lookup"><span data-stu-id="f7b6d-144">-RetentionPolicy</span></span>
<span data-ttu-id="f7b6d-145">백업 정책에 대 한 보존 정책의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-145">Specifies an array of retention policies for the backup policy.</span></span>
<span data-ttu-id="f7b6d-146">**AzureRmBackupRetentionPolicy** 을 얻으려면 New-AzureRmBackupRetentionPolicyObject cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-146">To obtain an **AzureRmBackupRetentionPolicy** , use the New-AzureRmBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7b6d-147">-Type</span><span class="sxs-lookup"><span data-stu-id="f7b6d-147">-Type</span></span>
<span data-ttu-id="f7b6d-148">정책이 적용 되는 백업 항목의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-148">Specifies the type of backup item to which the policy applies.</span></span>
<span data-ttu-id="f7b6d-149">현재만 지원 되는 값은 Add-azurevm입니다.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-149">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7b6d-150">-저장실</span><span class="sxs-lookup"><span data-stu-id="f7b6d-150">-Vault</span></span>
<span data-ttu-id="f7b6d-151">백업 정책이 속한 Azure Backup 자격 증명 모음을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-151">Specifies the Azure Backup vault to which the backup policy belongs.</span></span>
<span data-ttu-id="f7b6d-152">**AzureRmBackupVault** 개체를 가져오려면 Get-AzureRmBackupVault cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-152">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7b6d-153">-주간</span><span class="sxs-lookup"><span data-stu-id="f7b6d-153">-Weekly</span></span>
<span data-ttu-id="f7b6d-154">백업 정책이 일주일에 한 번 이상 매주 트리거 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-154">Indicates that the backup policy is triggered weekly on one or more days of the week.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7b6d-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7b6d-155">-DefaultProfile</span></span>
<span data-ttu-id="f7b6d-156">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7b6d-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7b6d-157">CommonParameters</span></span>
<span data-ttu-id="f7b6d-158">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7b6d-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7b6d-159">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7b6d-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7b6d-160">입력</span><span class="sxs-lookup"><span data-stu-id="f7b6d-160">INPUTS</span></span>

### <span data-ttu-id="f7b6d-161">않아야</span><span class="sxs-lookup"><span data-stu-id="f7b6d-161">None</span></span>

## <span data-ttu-id="f7b6d-162">출력</span><span class="sxs-lookup"><span data-stu-id="f7b6d-162">OUTPUTS</span></span>

### <span data-ttu-id="f7b6d-163">AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f7b6d-163">AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="f7b6d-164">상속자</span><span class="sxs-lookup"><span data-stu-id="f7b6d-164">NOTES</span></span>
* <span data-ttu-id="f7b6d-165">않아야</span><span class="sxs-lookup"><span data-stu-id="f7b6d-165">None</span></span>

## <span data-ttu-id="f7b6d-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f7b6d-166">RELATED LINKS</span></span>

[<span data-ttu-id="f7b6d-167">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="f7b6d-167">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="f7b6d-168">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f7b6d-168">Get-AzureRmBackupProtectionPolicy</span></span>](./Get-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="f7b6d-169">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="f7b6d-169">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="f7b6d-170">새로운 AzureRmBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="f7b6d-170">New-AzureRmBackupRetentionPolicyObject</span></span>](./New-AzureRmBackupRetentionPolicyObject.md)

[<span data-ttu-id="f7b6d-171">제거-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f7b6d-171">Remove-AzureRmBackupProtectionPolicy</span></span>](./Remove-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="f7b6d-172">Set-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="f7b6d-172">Set-AzureRmBackupProtectionPolicy</span></span>](./Set-AzureRmBackupProtectionPolicy.md)


