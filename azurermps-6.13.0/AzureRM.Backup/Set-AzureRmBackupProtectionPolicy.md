---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3BF6DB10-6020-4324-A177-F07BB52AF040
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/set-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: caf6394ce84b18bd8e36b4504173fe7f7bb07fac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528639"
---
# <span data-ttu-id="725e1-101">Set-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="725e1-101">Set-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="725e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="725e1-102">SYNOPSIS</span></span>
<span data-ttu-id="725e1-103">기존 보호 정책을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="725e1-103">Modifies an existing protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="725e1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="725e1-104">SYNTAX</span></span>

### <span data-ttu-id="725e1-105">NoScheduleParamSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="725e1-105">NoScheduleParamSet (Default)</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="725e1-106">DailyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="725e1-106">DailyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Daily] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="725e1-107">WeeklyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="725e1-107">WeeklyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Weekly] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [[-DaysOfWeek] <String[]>]
 [-ProtectionPolicy] <AzureRMBackupProtectionPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="725e1-108">설명은</span><span class="sxs-lookup"><span data-stu-id="725e1-108">DESCRIPTION</span></span>
<span data-ttu-id="725e1-109">**Set-AzureRmBackupProtectionPolicy** Cmdlet은 Azure Backup의 기존 보호 정책을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="725e1-109">The **Set-AzureRmBackupProtectionPolicy** cmdlet modifies an existing protection policy in Azure Backup.</span></span>
<span data-ttu-id="725e1-110">다음 보호 정책 구성 요소를 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="725e1-110">You can modify the following protection policy components:</span></span> 
- <span data-ttu-id="725e1-111">성을</span><span class="sxs-lookup"><span data-stu-id="725e1-111">Name</span></span>
- <span data-ttu-id="725e1-112">백업 일정</span><span class="sxs-lookup"><span data-stu-id="725e1-112">Backup schedule</span></span>
- <span data-ttu-id="725e1-113">보존 정책 변경 사항이 있으면 정책과 관련 된 항목의 백업 및 보존에 영향을 줄 수가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="725e1-113">Retention policies Any change might affect the backup and retention of the items associated with the policy.</span></span>

## <span data-ttu-id="725e1-114">예제의</span><span class="sxs-lookup"><span data-stu-id="725e1-114">EXAMPLES</span></span>

## <span data-ttu-id="725e1-115">변수</span><span class="sxs-lookup"><span data-stu-id="725e1-115">PARAMETERS</span></span>

### <span data-ttu-id="725e1-116">백 가동 시간</span><span class="sxs-lookup"><span data-stu-id="725e1-116">-BackupTime</span></span>
<span data-ttu-id="725e1-117">새 백업 시간을 정책에 대 한 날짜 **/시간** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="725e1-117">Specifies the new backup time of day, as a **DateTime** object, for the policy.</span></span>
<span data-ttu-id="725e1-118">**DateTime** 개체를 가져오려면 Get-Date cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="725e1-118">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="725e1-119">**DateTime** 개체에 대 한 자세한 내용은를 입력 `Get-Help Get-Date` 합니다.</span><span class="sxs-lookup"><span data-stu-id="725e1-119">For information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="725e1-120">-매일</span><span class="sxs-lookup"><span data-stu-id="725e1-120">-Daily</span></span>
<span data-ttu-id="725e1-121">백업 작업이 일별 일정에 실행 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="725e1-121">Indicates that the backup operation runs on a Daily schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="725e1-122">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="725e1-122">-DaysOfWeek</span></span>
<span data-ttu-id="725e1-123">요일의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="725e1-123">Specifies an array of days of the week.</span></span>
<span data-ttu-id="725e1-124">이 정책은이 매개 변수에 지정 된 일 동안 백업을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="725e1-124">This policy runs backups on the days specified by this parameter.</span></span>
<span data-ttu-id="725e1-125">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="725e1-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="725e1-126">월요일</span><span class="sxs-lookup"><span data-stu-id="725e1-126">Monday</span></span> 
- <span data-ttu-id="725e1-127">시간은</span><span class="sxs-lookup"><span data-stu-id="725e1-127">Tuesday</span></span> 
- <span data-ttu-id="725e1-128">일</span><span class="sxs-lookup"><span data-stu-id="725e1-128">Wednesday</span></span> 
- <span data-ttu-id="725e1-129">목요일</span><span class="sxs-lookup"><span data-stu-id="725e1-129">Thursday</span></span> 
- <span data-ttu-id="725e1-130">금요일</span><span class="sxs-lookup"><span data-stu-id="725e1-130">Friday</span></span> 
- <span data-ttu-id="725e1-131">토요일</span><span class="sxs-lookup"><span data-stu-id="725e1-131">Saturday</span></span> 
- <span data-ttu-id="725e1-132">나타내고</span><span class="sxs-lookup"><span data-stu-id="725e1-132">Sunday</span></span>

```yaml
Type: System.String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="725e1-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="725e1-133">-DefaultProfile</span></span>
<span data-ttu-id="725e1-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="725e1-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="725e1-135">-NewName</span><span class="sxs-lookup"><span data-stu-id="725e1-135">-NewName</span></span>
<span data-ttu-id="725e1-136">정책의 새 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="725e1-136">Specifies the new name for the policy.</span></span>
<span data-ttu-id="725e1-137">이 이름은 자격 증명 모음에서 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="725e1-137">This name must be unique in a vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="725e1-138">-ProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="725e1-138">-ProtectionPolicy</span></span>
<span data-ttu-id="725e1-139">이 cmdlet이 수정 하는 보호 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="725e1-139">Specifies protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="725e1-140">**AzureRmBackupProtectionPolicy** 개체를 가져오려면 Get-AzureRmBackupProtectionPolicy cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="725e1-140">To obtain an **AzureRmBackupProtectionPolicy** object, use the Get-AzureRmBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="725e1-141">-보존 정책</span><span class="sxs-lookup"><span data-stu-id="725e1-141">-RetentionPolicy</span></span>
<span data-ttu-id="725e1-142">백업 정책에 대 한 보존 정책의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="725e1-142">Specifies an array of retention policies for the backup policy.</span></span>
<span data-ttu-id="725e1-143">**AzureRmBackupRetentionPolicy** 개체를 가져오려면 New-AzureRmBackupRetentionPolicyObject cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="725e1-143">To obtain **AzureRmBackupRetentionPolicy** objects, use the New-AzureRmBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="725e1-144">-주간</span><span class="sxs-lookup"><span data-stu-id="725e1-144">-Weekly</span></span>
<span data-ttu-id="725e1-145">백업 작업이 주간 일정에 따라 실행 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="725e1-145">Indicates that the backup operation runs on a Weekly schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="725e1-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="725e1-146">CommonParameters</span></span>
<span data-ttu-id="725e1-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="725e1-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="725e1-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="725e1-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="725e1-149">입력</span><span class="sxs-lookup"><span data-stu-id="725e1-149">INPUTS</span></span>

### <span data-ttu-id="725e1-150">AzureRMBackupProtectionPolicy를 통한 명령.</span><span class="sxs-lookup"><span data-stu-id="725e1-150">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy</span></span>
<span data-ttu-id="725e1-151">매개 변수: ProtectionPolicy (ByValue)</span><span class="sxs-lookup"><span data-stu-id="725e1-151">Parameters: ProtectionPolicy (ByValue)</span></span>

## <span data-ttu-id="725e1-152">출력</span><span class="sxs-lookup"><span data-stu-id="725e1-152">OUTPUTS</span></span>

### <span data-ttu-id="725e1-153">AzureRMBackupJob를 통한 명령.</span><span class="sxs-lookup"><span data-stu-id="725e1-153">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="725e1-154">상속자</span><span class="sxs-lookup"><span data-stu-id="725e1-154">NOTES</span></span>

## <span data-ttu-id="725e1-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="725e1-155">RELATED LINKS</span></span>

[<span data-ttu-id="725e1-156">새로운 AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="725e1-156">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)


