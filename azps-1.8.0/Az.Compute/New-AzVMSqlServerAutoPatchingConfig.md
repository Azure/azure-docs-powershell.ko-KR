---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 38689e4ca41e4403ba7ef5a6af7d8419a1b54732
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869009"
---
# <span data-ttu-id="b1767-101">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="b1767-101">New-AzVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="b1767-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1767-102">SYNOPSIS</span></span>
<span data-ttu-id="b1767-103">가상 컴퓨터에 자동으로 패치할 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1767-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="b1767-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b1767-104">SYNTAX</span></span>

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [<CommonParameters>]
```

## <span data-ttu-id="b1767-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b1767-105">DESCRIPTION</span></span>
<span data-ttu-id="b1767-106">**AzVMSqlServerAutoPatchingConfig** cmdlet은 가상 컴퓨터에 자동으로 패치를 적용 하기 위한 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1767-106">The **New-AzVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="b1767-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b1767-107">EXAMPLES</span></span>

### <span data-ttu-id="b1767-108">예제 1: 자동 패치를 구성 하는 구성 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="b1767-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="b1767-109">이 명령은 패칭에 대 한 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1767-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="b1767-110">이 명령은 요일을 지정 하 고 유지 관리 기간을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1767-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="b1767-111">이 구성은 이러한 값을 사용 하는 패치를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1767-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="b1767-112">명령이 $AutoBackupConfig 변수에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1767-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="b1767-113">Set-AzVMSqlServerExtension cmdlet 등의 다른 cmdlet에 대해이 구성 항목을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b1767-113">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="b1767-114">변수</span><span class="sxs-lookup"><span data-stu-id="b1767-114">PARAMETERS</span></span>

### <span data-ttu-id="b1767-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="b1767-115">-DayOfWeek</span></span>
<span data-ttu-id="b1767-116">업데이트를 설치 해야 하는 요일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1767-116">Specifies the day of the week when updates should be installed.</span></span>
<span data-ttu-id="b1767-117">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b1767-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b1767-118">나타내고</span><span class="sxs-lookup"><span data-stu-id="b1767-118">Sunday</span></span>
- <span data-ttu-id="b1767-119">월요일</span><span class="sxs-lookup"><span data-stu-id="b1767-119">Monday</span></span>
- <span data-ttu-id="b1767-120">시간은</span><span class="sxs-lookup"><span data-stu-id="b1767-120">Tuesday</span></span>
- <span data-ttu-id="b1767-121">일</span><span class="sxs-lookup"><span data-stu-id="b1767-121">Wednesday</span></span>
- <span data-ttu-id="b1767-122">목요일</span><span class="sxs-lookup"><span data-stu-id="b1767-122">Thursday</span></span>
- <span data-ttu-id="b1767-123">금요일</span><span class="sxs-lookup"><span data-stu-id="b1767-123">Friday</span></span>
- <span data-ttu-id="b1767-124">토요일</span><span class="sxs-lookup"><span data-stu-id="b1767-124">Saturday</span></span>
- <span data-ttu-id="b1767-125">매일</span><span class="sxs-lookup"><span data-stu-id="b1767-125">Everyday</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Everyday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1767-126">-사용</span><span class="sxs-lookup"><span data-stu-id="b1767-126">-Enable</span></span>
<span data-ttu-id="b1767-127">가상 컴퓨터에 대 한 자동 패치가 활성화 되어 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b1767-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="b1767-128">자동 패치를 사용 하도록 설정 하면 cmdlet이 Windows Update를 대화형 모드로 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1767-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="b1767-129">자동 패치를 사용 하지 않도록 설정 하는 경우 Windows 업데이트 설정이 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1767-129">If you disable automated patching, Windows Update settings do not change.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1767-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="b1767-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="b1767-131">유지 관리 기간의 기간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1767-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="b1767-132">자동화 된 패치는 해당 창 외부의 가상 컴퓨터 가용성에 영향을 줄 수 있는 작업을 수행 하지 않도록 방지 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1767-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="b1767-133">30 분의 배수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1767-133">Specify a multiple of 30 minutes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1767-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="b1767-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="b1767-135">유지 관리 기간이 시작 되는 시간 (일)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1767-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="b1767-136">이 시간은 업데이트가 설치 되기 시작 하는 시기를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1767-136">This time defines when updates start to install.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1767-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="b1767-137">-PatchCategory</span></span>
<span data-ttu-id="b1767-138">중요 업데이트를 포함 해야 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1767-138">Specifies whether important updates should be included.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Important

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1767-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1767-139">CommonParameters</span></span>
<span data-ttu-id="b1767-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1767-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1767-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1767-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1767-142">입력</span><span class="sxs-lookup"><span data-stu-id="b1767-142">INPUTS</span></span>

### <span data-ttu-id="b1767-143">않아야</span><span class="sxs-lookup"><span data-stu-id="b1767-143">None</span></span>

## <span data-ttu-id="b1767-144">출력</span><span class="sxs-lookup"><span data-stu-id="b1767-144">OUTPUTS</span></span>

### <span data-ttu-id="b1767-145">AutoPatchingSettings를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1767-145">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

## <span data-ttu-id="b1767-146">상속자</span><span class="sxs-lookup"><span data-stu-id="b1767-146">NOTES</span></span>

## <span data-ttu-id="b1767-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1767-147">RELATED LINKS</span></span>

[<span data-ttu-id="b1767-148">새로운 AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="b1767-148">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="b1767-149">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="b1767-149">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


