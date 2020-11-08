---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7317DAC1-B535-4650-86BF-73E96F61EECD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23bb8e09fac8ec4fe0e8ff5b3c23ab995f03694c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046191"
---
# <span data-ttu-id="daf2c-101">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="daf2c-101">New-AzureVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="daf2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="daf2c-102">SYNOPSIS</span></span>
<span data-ttu-id="daf2c-103">가상 컴퓨터 자동 패칭에 대 한 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="daf2c-103">Creates a configuration object for virtual machine automatic patching.</span></span>

## <span data-ttu-id="daf2c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="daf2c-104">SYNTAX</span></span>

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="daf2c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="daf2c-105">DESCRIPTION</span></span>
<span data-ttu-id="daf2c-106">**AzureVMSqlServerAutoPatchingConfig** cmdlet은 가상 컴퓨터 자동 패칭에 대 한 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="daf2c-106">The **New-AzureVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for virtual machine automatic patching.</span></span>

## <span data-ttu-id="daf2c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="daf2c-107">EXAMPLES</span></span>

### <span data-ttu-id="daf2c-108">예제 1: 자동 패치를 구성 하는 구성 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="daf2c-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $APS = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
          Enable                        : True
          DayOfWeek                     : Thursday
          MaintenanceWindowStartingHour : 11
          MaintenanceWindowDuration     : 120
          PatchCategory                 : Important
```

<span data-ttu-id="daf2c-109">이 명령은 Set-AzureVMSqlServerExtension를 사용 하 여 자동 패치를 구성 하는 데 사용할 수 있는 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="daf2c-109">This command creates configuration object that can be used to configure automatic patching using Set-AzureVMSqlServerExtension.</span></span>

## <span data-ttu-id="daf2c-110">변수</span><span class="sxs-lookup"><span data-stu-id="daf2c-110">PARAMETERS</span></span>

### <span data-ttu-id="daf2c-111">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="daf2c-111">-DayOfWeek</span></span>
<span data-ttu-id="daf2c-112">업데이트를 설치 해야 하는 요일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="daf2c-112">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="daf2c-113">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="daf2c-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="daf2c-114">나타내고</span><span class="sxs-lookup"><span data-stu-id="daf2c-114">Sunday</span></span>
- <span data-ttu-id="daf2c-115">월요일</span><span class="sxs-lookup"><span data-stu-id="daf2c-115">Monday</span></span>
- <span data-ttu-id="daf2c-116">시간은</span><span class="sxs-lookup"><span data-stu-id="daf2c-116">Tuesday</span></span>
- <span data-ttu-id="daf2c-117">일</span><span class="sxs-lookup"><span data-stu-id="daf2c-117">Wednesday</span></span>
- <span data-ttu-id="daf2c-118">목요일</span><span class="sxs-lookup"><span data-stu-id="daf2c-118">Thursday</span></span>
- <span data-ttu-id="daf2c-119">금요일</span><span class="sxs-lookup"><span data-stu-id="daf2c-119">Friday</span></span>
- <span data-ttu-id="daf2c-120">토요일</span><span class="sxs-lookup"><span data-stu-id="daf2c-120">Saturday</span></span>
- <span data-ttu-id="daf2c-121">매일</span><span class="sxs-lookup"><span data-stu-id="daf2c-121">Everyday</span></span>

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

### <span data-ttu-id="daf2c-122">-사용</span><span class="sxs-lookup"><span data-stu-id="daf2c-122">-Enable</span></span>
<span data-ttu-id="daf2c-123">가상 컴퓨터에 대 한 자동 패치가 활성화 되어 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="daf2c-123">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="daf2c-124">자동 패치 기능을 사용 하도록 설정 하면 cmdlet에서 Windows 업데이트를 대화형 모드로 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="daf2c-124">If you enable automated patching the cmdlet will put Windows Update into interactive mode.</span></span>
<span data-ttu-id="daf2c-125">자동 패치를 사용 하지 않도록 설정 하면 Windows 업데이트 설정이 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="daf2c-125">If you disable automated patching, Windows Update settings will not change.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daf2c-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="daf2c-126">-InformationAction</span></span>
<span data-ttu-id="daf2c-127">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="daf2c-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="daf2c-128">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="daf2c-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="daf2c-129">하기로</span><span class="sxs-lookup"><span data-stu-id="daf2c-129">Continue</span></span>
- <span data-ttu-id="daf2c-130">숨기기</span><span class="sxs-lookup"><span data-stu-id="daf2c-130">Ignore</span></span>
- <span data-ttu-id="daf2c-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="daf2c-131">Inquire</span></span>
- <span data-ttu-id="daf2c-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="daf2c-132">SilentlyContinue</span></span>
- <span data-ttu-id="daf2c-133">중지가</span><span class="sxs-lookup"><span data-stu-id="daf2c-133">Stop</span></span>
- <span data-ttu-id="daf2c-134">대기</span><span class="sxs-lookup"><span data-stu-id="daf2c-134">Suspend</span></span>

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

### <span data-ttu-id="daf2c-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="daf2c-135">-InformationVariable</span></span>
<span data-ttu-id="daf2c-136">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="daf2c-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="daf2c-137">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="daf2c-137">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="daf2c-138">유지 관리 창의 기간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="daf2c-138">Specifies the duration of the maintenance window.</span></span>
<span data-ttu-id="daf2c-139">자동화 된 패치는 해당 창 외부의 가상 컴퓨터 가용성에 영향을 줄 수 있는 작업을 수행 하지 않도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="daf2c-139">Automated patching will avoid performing an action that can impact a virtual machine availability outside of that window.</span></span>
<span data-ttu-id="daf2c-140">30 분 단위로만 증가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="daf2c-140">Only 30 minutes increments are allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daf2c-141">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="daf2c-141">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="daf2c-142">유지 관리 기간이 시작 되는 시간 (일)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="daf2c-142">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="daf2c-143">이번에는 업데이트 설치가 시작 되는 시간과 시간으로 반올림 되는 시간을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="daf2c-143">This time defines when updates start installing and is rounded to the hour.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daf2c-144">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="daf2c-144">-PatchCategory</span></span>
<span data-ttu-id="daf2c-145">중요 업데이트를 포함 해야 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="daf2c-145">Specifies whether important updates should be included.</span></span>

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

### <span data-ttu-id="daf2c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daf2c-146">CommonParameters</span></span>
<span data-ttu-id="daf2c-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="daf2c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daf2c-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="daf2c-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daf2c-149">입력</span><span class="sxs-lookup"><span data-stu-id="daf2c-149">INPUTS</span></span>

## <span data-ttu-id="daf2c-150">출력</span><span class="sxs-lookup"><span data-stu-id="daf2c-150">OUTPUTS</span></span>

### <span data-ttu-id="daf2c-151">AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="daf2c-151">AutoPatchingSettings</span></span>
<span data-ttu-id="daf2c-152">이 cmdlet은 자동 패칭에 대 한 설정을 포함 하는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="daf2c-152">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="daf2c-153">상속자</span><span class="sxs-lookup"><span data-stu-id="daf2c-153">NOTES</span></span>

## <span data-ttu-id="daf2c-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="daf2c-154">RELATED LINKS</span></span>

[<span data-ttu-id="daf2c-155">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="daf2c-155">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)

[<span data-ttu-id="daf2c-156">제거-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="daf2c-156">Remove-AzureVMSqlServerExtension</span></span>](./Remove-AzureVMSqlServerExtension.md)

[<span data-ttu-id="daf2c-157">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="daf2c-157">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)


