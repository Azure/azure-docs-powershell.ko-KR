---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: EE7EC812-640B-4672-B23C-673F912F0EDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 945d06ddc1be6d2b0864b0421a5a087e14d98218
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045528"
---
# <span data-ttu-id="0a736-101">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span><span class="sxs-lookup"><span data-stu-id="0a736-101">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span></span>

## <span data-ttu-id="0a736-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a736-102">SYNOPSIS</span></span>
<span data-ttu-id="0a736-103">백업 일정 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0a736-103">Creates a backup schedule configuration object.</span></span>

## <span data-ttu-id="0a736-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0a736-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType <String> -RecurrenceType <String>
 -RecurrenceValue <Int32> -RetentionCount <Int64> [-StartFromDateTime <String>] -Enabled <Boolean>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0a736-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0a736-105">DESCRIPTION</span></span>
<span data-ttu-id="0a736-106">**AzureStorSimpleDeviceBackupScheduleAddConfig** Cmdlet은 **BackupScheduleBase** 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0a736-106">The **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet creates a **BackupScheduleBase** configuration object.</span></span>
<span data-ttu-id="0a736-107">이 구성 개체를 사용 하 여 **새 AzureStorSimpleDeviceBackupPolicy** cmdlet을 사용 하 여 새 백업 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0a736-107">Use this configuration object to create new backup policy by using the **New-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

## <span data-ttu-id="0a736-108">예제의</span><span class="sxs-lookup"><span data-stu-id="0a736-108">EXAMPLES</span></span>

### <span data-ttu-id="0a736-109">예제 1: 백업 구성 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="0a736-109">Example 1: Create a backup configuration object</span></span>
```
PS C:\>New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType CloudSnapshot -RecurrenceType Daily -RecurrenceValue 1 -RetentionCount 100 -Enabled $True
VERBOSE: ClientRequestId: 426a79ee-fed3-4d3d-9123-e371f83222b3_PS


BackupType     : CloudSnapshot
Recurrence     : Microsoft.WindowsAzure.Management.StorSimple.Models.ScheduleRecurrence
RetentionCount : 100
StartTime      : 2014-12-16T00:37:19+05:30
Status         : Enabled
```

<span data-ttu-id="0a736-110">이 명령은 클라우드 스냅숏 백업에 대 한 백업 일정 기본 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0a736-110">This command creates a backup schedule base object for cloud snapshot backups.</span></span>
<span data-ttu-id="0a736-111">백업은 매일 수행 되며 백업은 100 일간 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a736-111">The backup occurs every day, and the backups are kept for 100 days.</span></span>
<span data-ttu-id="0a736-112">이 일정은 기본 시간 (현재 시간)에서 사용 하도록 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a736-112">This schedule is enabled from the default time, which is the current time.</span></span>

## <span data-ttu-id="0a736-113">변수</span><span class="sxs-lookup"><span data-stu-id="0a736-113">PARAMETERS</span></span>

### <span data-ttu-id="0a736-114">-BackupType</span><span class="sxs-lookup"><span data-stu-id="0a736-114">-BackupType</span></span>
<span data-ttu-id="0a736-115">백업 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a736-115">Specifies the backup type.</span></span>
<span data-ttu-id="0a736-116">유효한 값은 LocalSnapshot 및 CloudSnapshot입니다.</span><span class="sxs-lookup"><span data-stu-id="0a736-116">Valid values are: LocalSnapshot and CloudSnapshot.</span></span>

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

### <span data-ttu-id="0a736-117">-사용</span><span class="sxs-lookup"><span data-stu-id="0a736-117">-Enabled</span></span>
<span data-ttu-id="0a736-118">백업 일정을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0a736-118">Indicates whether to enable the backup schedule.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a736-119">-프로필</span><span class="sxs-lookup"><span data-stu-id="0a736-119">-Profile</span></span>
<span data-ttu-id="0a736-120">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a736-120">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="0a736-121">-RecurrenceType</span><span class="sxs-lookup"><span data-stu-id="0a736-121">-RecurrenceType</span></span>
<span data-ttu-id="0a736-122">이 백업 일정의 되풀이 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a736-122">Specifies the type of recurrence for this backup schedule.</span></span>
<span data-ttu-id="0a736-123">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0a736-123">Valid values are:</span></span> 

- <span data-ttu-id="0a736-124">걸릴</span><span class="sxs-lookup"><span data-stu-id="0a736-124">Minutes</span></span>
- <span data-ttu-id="0a736-125">마다</span><span class="sxs-lookup"><span data-stu-id="0a736-125">Hourly</span></span>
- <span data-ttu-id="0a736-126">Daily</span><span class="sxs-lookup"><span data-stu-id="0a736-126">Daily</span></span>
- <span data-ttu-id="0a736-127">매주</span><span class="sxs-lookup"><span data-stu-id="0a736-127">Weekly</span></span>

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

### <span data-ttu-id="0a736-128">-RecurrenceValue</span><span class="sxs-lookup"><span data-stu-id="0a736-128">-RecurrenceValue</span></span>
<span data-ttu-id="0a736-129">백업을 만들 빈도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a736-129">Specifies how often to make a backup.</span></span>
<span data-ttu-id="0a736-130">이 매개 변수는 *RecurrenceType* 매개 변수로 지정 된 단위를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a736-130">This parameter uses the unit specified by the *RecurrenceType* parameter.</span></span>

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

### <span data-ttu-id="0a736-131">-보존 횟수</span><span class="sxs-lookup"><span data-stu-id="0a736-131">-RetentionCount</span></span>
<span data-ttu-id="0a736-132">백업을 유지할 일 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a736-132">Specifies the number of days to keep a backup.</span></span>

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

### <span data-ttu-id="0a736-133">-StartFromDateTime</span><span class="sxs-lookup"><span data-stu-id="0a736-133">-StartFromDateTime</span></span>
<span data-ttu-id="0a736-134">백업 하기 시작 하는 날짜를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a736-134">Specifies the date from which to start making backups.</span></span>
<span data-ttu-id="0a736-135">기본값은 현재 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="0a736-135">The default value is the current time.</span></span>

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

### <span data-ttu-id="0a736-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a736-136">CommonParameters</span></span>
<span data-ttu-id="0a736-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a736-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a736-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a736-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a736-139">입력</span><span class="sxs-lookup"><span data-stu-id="0a736-139">INPUTS</span></span>

### <span data-ttu-id="0a736-140">않아야</span><span class="sxs-lookup"><span data-stu-id="0a736-140">None</span></span>

## <span data-ttu-id="0a736-141">출력</span><span class="sxs-lookup"><span data-stu-id="0a736-141">OUTPUTS</span></span>

### <span data-ttu-id="0a736-142">BackupScheduleBase</span><span class="sxs-lookup"><span data-stu-id="0a736-142">BackupScheduleBase</span></span>
<span data-ttu-id="0a736-143">이 cmdlet은 **BackupScheduleBase** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a736-143">This cmdlet returns a **BackupScheduleBase** object.</span></span>
<span data-ttu-id="0a736-144">**BackupScheduleBase** 를 사용 하 여 새 백업 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0a736-144">Use a **BackupScheduleBase** to construct new backup policy.</span></span>

## <span data-ttu-id="0a736-145">상속자</span><span class="sxs-lookup"><span data-stu-id="0a736-145">NOTES</span></span>

## <span data-ttu-id="0a736-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0a736-146">RELATED LINKS</span></span>

[<span data-ttu-id="0a736-147">새로운 AzureStorSimpleDeviceBackupScheduleUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="0a736-147">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleUpdateConfig.md)

[<span data-ttu-id="0a736-148">새로운 AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="0a736-148">New-AzureStorSimpleDeviceBackupPolicy</span></span>](./New-AzureStorSimpleDeviceBackupPolicy.md)


