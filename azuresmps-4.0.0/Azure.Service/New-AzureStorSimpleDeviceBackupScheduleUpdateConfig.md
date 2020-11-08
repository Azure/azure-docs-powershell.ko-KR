---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 22C6845E-D7BD-4BBC-B373-394A23488A94
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0695dc42d9c540e30ddf9ac55bd6fc136c84bff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045524"
---
# <span data-ttu-id="cf20a-101">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="cf20a-101">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span></span>

## <span data-ttu-id="cf20a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf20a-102">SYNOPSIS</span></span>
<span data-ttu-id="cf20a-103">백업 일정 업데이트 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cf20a-103">Creates a backup schedule update configuration object.</span></span>

## <span data-ttu-id="cf20a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cf20a-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id <String> -BackupType <String> -RecurrenceType <String>
 -RecurrenceValue <Int32> -RetentionCount <Int64> [-StartFromDateTime <String>] [-Enabled <Boolean>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cf20a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cf20a-105">DESCRIPTION</span></span>
<span data-ttu-id="cf20a-106">**AzureStorSimpleDeviceBackupScheduleUpdateConfig** Cmdlet은 **BackupScheduleUpdateRequest** 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cf20a-106">The **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet creates a **BackupScheduleUpdateRequest** configuration object.</span></span>
<span data-ttu-id="cf20a-107">이 구성 개체를 사용 하 여 **Set-AzureStorSimpleDeviceBackupPolicy** cmdlet을 사용 하 여 백업 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf20a-107">Use this configuration object to update a backup policy by using the **Set-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

## <span data-ttu-id="cf20a-108">예제의</span><span class="sxs-lookup"><span data-stu-id="cf20a-108">EXAMPLES</span></span>

### <span data-ttu-id="cf20a-109">예제 1: 일정 업데이트 요청 만들기</span><span class="sxs-lookup"><span data-stu-id="cf20a-109">Example 1: Create a schedule update request</span></span>
```
PS C:\>New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id "147f734d-a31a-4473-8501-6ba38be2cb30" -BackupType CloudSnapshot -RecurrenceType Hourly -RecurrenceValue 1 -RetentionCount 50 -Enabled $True
VERBOSE: ClientRequestId: ef346641-54b4-4273-8898-7f863e7c5b7e_PS


BackupType     : CloudSnapshot
Id             : 147f734d-a31a-4473-8501-6ba38be2cb30
Recurrence     : Microsoft.WindowsAzure.Management.StorSimple.Models.ScheduleRecurrence
RetentionCount : 50
StartTime      : 2014-12-16T00:39:32+05:30
Status         : Enabled
```

<span data-ttu-id="cf20a-110">이 명령은 지정 된 ID를 갖는 일정에 대 한 백업 일정 업데이트 요청을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cf20a-110">This command creates a backup schedule update request for the schedule that has the specified ID.</span></span>
<span data-ttu-id="cf20a-111">이 요청은 1 시간 마다 되풀이 되는 클라우드 스냅샷 백업을 예약 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="cf20a-111">The request is to make the schedule a cloud snapshot backup that recurs every hour.</span></span>
<span data-ttu-id="cf20a-112">백업은 50 일간 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf20a-112">The backups are kept for 50 days.</span></span>
<span data-ttu-id="cf20a-113">이 일정은 기본 시간 (현재 시간)에서 사용 하도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf20a-113">This schedule is enabled from the default time, which is the current time.</span></span>

## <span data-ttu-id="cf20a-114">변수</span><span class="sxs-lookup"><span data-stu-id="cf20a-114">PARAMETERS</span></span>

### <span data-ttu-id="cf20a-115">-BackupType</span><span class="sxs-lookup"><span data-stu-id="cf20a-115">-BackupType</span></span>
<span data-ttu-id="cf20a-116">백업 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf20a-116">Specifies the backup type.</span></span>
<span data-ttu-id="cf20a-117">유효한 값은 LocalSnapshot 및 CloudSnapshot입니다.</span><span class="sxs-lookup"><span data-stu-id="cf20a-117">Valid values are: LocalSnapshot and CloudSnapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf20a-118">-사용</span><span class="sxs-lookup"><span data-stu-id="cf20a-118">-Enabled</span></span>
<span data-ttu-id="cf20a-119">백업 일정을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="cf20a-119">Indicates whether to enable the backup schedule.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf20a-120">-Id</span><span class="sxs-lookup"><span data-stu-id="cf20a-120">-Id</span></span>
<span data-ttu-id="cf20a-121">업데이트할 백업 일정의 인스턴스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf20a-121">Specifies the instance ID of the backup schedule to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf20a-122">-프로필</span><span class="sxs-lookup"><span data-stu-id="cf20a-122">-Profile</span></span>
<span data-ttu-id="cf20a-123">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf20a-123">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="cf20a-124">-RecurrenceType</span><span class="sxs-lookup"><span data-stu-id="cf20a-124">-RecurrenceType</span></span>
<span data-ttu-id="cf20a-125">이 백업 일정의 되풀이 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf20a-125">Specifies the type of recurrence for this backup schedule.</span></span>
<span data-ttu-id="cf20a-126">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="cf20a-126">Valid values are:</span></span> 

- <span data-ttu-id="cf20a-127">걸릴</span><span class="sxs-lookup"><span data-stu-id="cf20a-127">Minutes</span></span>
- <span data-ttu-id="cf20a-128">마다</span><span class="sxs-lookup"><span data-stu-id="cf20a-128">Hourly</span></span>
- <span data-ttu-id="cf20a-129">Daily</span><span class="sxs-lookup"><span data-stu-id="cf20a-129">Daily</span></span>
- <span data-ttu-id="cf20a-130">매주</span><span class="sxs-lookup"><span data-stu-id="cf20a-130">Weekly</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf20a-131">-RecurrenceValue</span><span class="sxs-lookup"><span data-stu-id="cf20a-131">-RecurrenceValue</span></span>
<span data-ttu-id="cf20a-132">백업을 만들 빈도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf20a-132">Specifies how often to make a backup.</span></span>
<span data-ttu-id="cf20a-133">이 매개 변수는 *RecurrenceType* 매개 변수로 지정 된 단위를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf20a-133">This parameter uses the unit specified by the *RecurrenceType* parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf20a-134">-보존 횟수</span><span class="sxs-lookup"><span data-stu-id="cf20a-134">-RetentionCount</span></span>
<span data-ttu-id="cf20a-135">백업을 유지할 일 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf20a-135">Specifies the number of days to keep a backup.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf20a-136">-StartFromDateTime</span><span class="sxs-lookup"><span data-stu-id="cf20a-136">-StartFromDateTime</span></span>
<span data-ttu-id="cf20a-137">백업 하기 시작 하는 날짜를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf20a-137">Specifies the date from which to start making backups.</span></span>
<span data-ttu-id="cf20a-138">기본값은 현재 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="cf20a-138">The default value is the current time.</span></span>

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

### <span data-ttu-id="cf20a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf20a-139">CommonParameters</span></span>
<span data-ttu-id="cf20a-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf20a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf20a-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf20a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf20a-142">입력</span><span class="sxs-lookup"><span data-stu-id="cf20a-142">INPUTS</span></span>

### <span data-ttu-id="cf20a-143">않아야</span><span class="sxs-lookup"><span data-stu-id="cf20a-143">None</span></span>

## <span data-ttu-id="cf20a-144">출력</span><span class="sxs-lookup"><span data-stu-id="cf20a-144">OUTPUTS</span></span>

### <span data-ttu-id="cf20a-145">BackupScheduleUpdateRequest</span><span class="sxs-lookup"><span data-stu-id="cf20a-145">BackupScheduleUpdateRequest</span></span>
<span data-ttu-id="cf20a-146">이 cmdlet은 업데이트 된 백업 일정에 대 한 정보를 포함 하는 **BackupScheduleUpdateRequest** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf20a-146">This cmdlet returns a **BackupScheduleUpdateRequest** object that contains information about updated backup schedules.</span></span>

## <span data-ttu-id="cf20a-147">상속자</span><span class="sxs-lookup"><span data-stu-id="cf20a-147">NOTES</span></span>

## <span data-ttu-id="cf20a-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cf20a-148">RELATED LINKS</span></span>

[<span data-ttu-id="cf20a-149">새로운 AzureStorSimpleDeviceBackupScheduleAddConfig</span><span class="sxs-lookup"><span data-stu-id="cf20a-149">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleAddConfig.md)

[<span data-ttu-id="cf20a-150">Set-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="cf20a-150">Set-AzureStorSimpleDeviceBackupPolicy</span></span>](./Set-AzureStorSimpleDeviceBackupPolicy.md)


