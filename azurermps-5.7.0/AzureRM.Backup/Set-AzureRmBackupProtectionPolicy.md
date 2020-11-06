---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3BF6DB10-6020-4324-A177-F07BB52AF040
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/set-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 7d41abd1d56bab4df0d716c3a9d11ea14140b784
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533719"
---
# <span data-ttu-id="56268-101">Set-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="56268-101">Set-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="56268-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56268-102">SYNOPSIS</span></span>
<span data-ttu-id="56268-103">기존 보호 정책을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56268-103">Modifies an existing protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56268-104">구문과</span><span class="sxs-lookup"><span data-stu-id="56268-104">SYNTAX</span></span>

### <span data-ttu-id="56268-105">NoScheduleParamSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="56268-105">NoScheduleParamSet (Default)</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56268-106">DailyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="56268-106">DailyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Daily] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56268-107">WeeklyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="56268-107">WeeklyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Weekly] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [[-DaysOfWeek] <String[]>]
 [-ProtectionPolicy] <AzureRMBackupProtectionPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="56268-108">설명은</span><span class="sxs-lookup"><span data-stu-id="56268-108">DESCRIPTION</span></span>
<span data-ttu-id="56268-109">**Set-AzureRmBackupProtectionPolicy** Cmdlet은 Azure Backup의 기존 보호 정책을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56268-109">The **Set-AzureRmBackupProtectionPolicy** cmdlet modifies an existing protection policy in Azure Backup.</span></span>
<span data-ttu-id="56268-110">다음 보호 정책 구성 요소를 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56268-110">You can modify the following protection policy components:</span></span> 

- <span data-ttu-id="56268-111">성을</span><span class="sxs-lookup"><span data-stu-id="56268-111">Name</span></span>
- <span data-ttu-id="56268-112">백업 일정</span><span class="sxs-lookup"><span data-stu-id="56268-112">Backup schedule</span></span>
- <span data-ttu-id="56268-113">보존 정책</span><span class="sxs-lookup"><span data-stu-id="56268-113">Retention policies</span></span>

<span data-ttu-id="56268-114">변경 내용이 정책에 연결 된 항목의 백업 및 보존에 영향을 줄 수가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56268-114">Any change might affect the backup and retention of the items associated with the policy.</span></span>

## <span data-ttu-id="56268-115">예제의</span><span class="sxs-lookup"><span data-stu-id="56268-115">EXAMPLES</span></span>

## <span data-ttu-id="56268-116">변수</span><span class="sxs-lookup"><span data-stu-id="56268-116">PARAMETERS</span></span>

### <span data-ttu-id="56268-117">백 가동 시간</span><span class="sxs-lookup"><span data-stu-id="56268-117">-BackupTime</span></span>
<span data-ttu-id="56268-118">새 백업 시간을 정책에 대 한 날짜 **/시간** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56268-118">Specifies the new backup time of day, as a **DateTime** object, for the policy.</span></span>
<span data-ttu-id="56268-119">**DateTime** 개체를 가져오려면 Get-Date cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="56268-119">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="56268-120">**DateTime** 개체에 대 한 자세한 내용은를 입력 `Get-Help Get-Date` 합니다.</span><span class="sxs-lookup"><span data-stu-id="56268-120">For information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56268-121">-매일</span><span class="sxs-lookup"><span data-stu-id="56268-121">-Daily</span></span>
<span data-ttu-id="56268-122">백업 작업이 일별 일정에 실행 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="56268-122">Indicates that the backup operation runs on a Daily schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56268-123">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="56268-123">-DaysOfWeek</span></span>
<span data-ttu-id="56268-124">요일의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56268-124">Specifies an array of days of the week.</span></span>
<span data-ttu-id="56268-125">이 정책은이 매개 변수에 지정 된 일 동안 백업을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="56268-125">This policy runs backups on the days specified by this parameter.</span></span>
<span data-ttu-id="56268-126">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="56268-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="56268-127">월요일</span><span class="sxs-lookup"><span data-stu-id="56268-127">Monday</span></span> 
- <span data-ttu-id="56268-128">시간은</span><span class="sxs-lookup"><span data-stu-id="56268-128">Tuesday</span></span> 
- <span data-ttu-id="56268-129">일</span><span class="sxs-lookup"><span data-stu-id="56268-129">Wednesday</span></span> 
- <span data-ttu-id="56268-130">목요일</span><span class="sxs-lookup"><span data-stu-id="56268-130">Thursday</span></span> 
- <span data-ttu-id="56268-131">금요일</span><span class="sxs-lookup"><span data-stu-id="56268-131">Friday</span></span> 
- <span data-ttu-id="56268-132">토요일</span><span class="sxs-lookup"><span data-stu-id="56268-132">Saturday</span></span> 
- <span data-ttu-id="56268-133">나타내고</span><span class="sxs-lookup"><span data-stu-id="56268-133">Sunday</span></span>

```yaml
Type: String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56268-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56268-134">-DefaultProfile</span></span>
<span data-ttu-id="56268-135">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="56268-135">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56268-136">-NewName</span><span class="sxs-lookup"><span data-stu-id="56268-136">-NewName</span></span>
<span data-ttu-id="56268-137">정책의 새 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56268-137">Specifies the new name for the policy.</span></span>
<span data-ttu-id="56268-138">이 이름은 자격 증명 모음에서 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="56268-138">This name must be unique in a vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56268-139">-ProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="56268-139">-ProtectionPolicy</span></span>
<span data-ttu-id="56268-140">이 cmdlet이 수정 하는 보호 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56268-140">Specifies protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="56268-141">**AzureRmBackupProtectionPolicy** 개체를 가져오려면 Get-AzureRmBackupProtectionPolicy cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="56268-141">To obtain an **AzureRmBackupProtectionPolicy** object, use the Get-AzureRmBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56268-142">-보존 정책</span><span class="sxs-lookup"><span data-stu-id="56268-142">-RetentionPolicy</span></span>
<span data-ttu-id="56268-143">백업 정책에 대 한 보존 정책의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56268-143">Specifies an array of retention policies for the backup policy.</span></span>
<span data-ttu-id="56268-144">**AzureRmBackupRetentionPolicy** 개체를 가져오려면 New-AzureRmBackupRetentionPolicyObject cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="56268-144">To obtain **AzureRmBackupRetentionPolicy** objects, use the New-AzureRmBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56268-145">-주간</span><span class="sxs-lookup"><span data-stu-id="56268-145">-Weekly</span></span>
<span data-ttu-id="56268-146">백업 작업이 주간 일정에 따라 실행 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="56268-146">Indicates that the backup operation runs on a Weekly schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56268-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56268-147">CommonParameters</span></span>
<span data-ttu-id="56268-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="56268-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56268-149">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56268-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56268-150">입력</span><span class="sxs-lookup"><span data-stu-id="56268-150">INPUTS</span></span>

### <span data-ttu-id="56268-151">AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="56268-151">AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="56268-152">출력</span><span class="sxs-lookup"><span data-stu-id="56268-152">OUTPUTS</span></span>

### <span data-ttu-id="56268-153">않아야</span><span class="sxs-lookup"><span data-stu-id="56268-153">None</span></span>

## <span data-ttu-id="56268-154">상속자</span><span class="sxs-lookup"><span data-stu-id="56268-154">NOTES</span></span>

## <span data-ttu-id="56268-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="56268-155">RELATED LINKS</span></span>

[<span data-ttu-id="56268-156">새로운 AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="56268-156">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)


