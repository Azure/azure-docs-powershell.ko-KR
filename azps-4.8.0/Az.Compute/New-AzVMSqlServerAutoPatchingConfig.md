---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 6fe89822af5be532674e22dd3e1c1edd583fced4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048411"
---
# <span data-ttu-id="475eb-101">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="475eb-101">New-AzVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="475eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="475eb-102">SYNOPSIS</span></span>
<span data-ttu-id="475eb-103">가상 컴퓨터에 자동으로 패치할 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="475eb-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="475eb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="475eb-104">SYNTAX</span></span>

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [<CommonParameters>]
```

## <span data-ttu-id="475eb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="475eb-105">DESCRIPTION</span></span>
<span data-ttu-id="475eb-106">**AzVMSqlServerAutoPatchingConfig** cmdlet은 가상 컴퓨터에 자동으로 패치를 적용 하기 위한 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="475eb-106">The **New-AzVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="475eb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="475eb-107">EXAMPLES</span></span>

### <span data-ttu-id="475eb-108">예제 1: 자동 패치를 구성 하는 구성 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="475eb-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="475eb-109">이 명령은 패칭에 대 한 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="475eb-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="475eb-110">이 명령은 요일을 지정 하 고 유지 관리 기간을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="475eb-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="475eb-111">이 구성은 이러한 값을 사용 하는 패치를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="475eb-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="475eb-112">명령이 $AutoBackupConfig 변수에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="475eb-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="475eb-113">Set-AzVMSqlServerExtension cmdlet 등의 다른 cmdlet에 대해이 구성 항목을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="475eb-113">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="475eb-114">변수</span><span class="sxs-lookup"><span data-stu-id="475eb-114">PARAMETERS</span></span>

### <span data-ttu-id="475eb-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="475eb-115">-DayOfWeek</span></span>
<span data-ttu-id="475eb-116">업데이트를 설치 해야 하는 요일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="475eb-116">Specifies the day of the week when updates should be installed.</span></span>
<span data-ttu-id="475eb-117">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="475eb-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="475eb-118">나타내고</span><span class="sxs-lookup"><span data-stu-id="475eb-118">Sunday</span></span>
- <span data-ttu-id="475eb-119">월요일</span><span class="sxs-lookup"><span data-stu-id="475eb-119">Monday</span></span>
- <span data-ttu-id="475eb-120">시간은</span><span class="sxs-lookup"><span data-stu-id="475eb-120">Tuesday</span></span>
- <span data-ttu-id="475eb-121">일</span><span class="sxs-lookup"><span data-stu-id="475eb-121">Wednesday</span></span>
- <span data-ttu-id="475eb-122">목요일</span><span class="sxs-lookup"><span data-stu-id="475eb-122">Thursday</span></span>
- <span data-ttu-id="475eb-123">금요일</span><span class="sxs-lookup"><span data-stu-id="475eb-123">Friday</span></span>
- <span data-ttu-id="475eb-124">토요일</span><span class="sxs-lookup"><span data-stu-id="475eb-124">Saturday</span></span>
- <span data-ttu-id="475eb-125">매일</span><span class="sxs-lookup"><span data-stu-id="475eb-125">Everyday</span></span>

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

### <span data-ttu-id="475eb-126">-사용</span><span class="sxs-lookup"><span data-stu-id="475eb-126">-Enable</span></span>
<span data-ttu-id="475eb-127">가상 컴퓨터에 대 한 자동 패치가 활성화 되어 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="475eb-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="475eb-128">자동 패치를 사용 하도록 설정 하면 cmdlet이 Windows Update를 대화형 모드로 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="475eb-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="475eb-129">자동 패치를 사용 하지 않도록 설정 하는 경우 Windows 업데이트 설정이 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="475eb-129">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="475eb-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="475eb-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="475eb-131">유지 관리 기간의 기간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="475eb-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="475eb-132">자동화 된 패치는 해당 창 외부의 가상 컴퓨터 가용성에 영향을 줄 수 있는 작업을 수행 하지 않도록 방지 합니다.</span><span class="sxs-lookup"><span data-stu-id="475eb-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="475eb-133">30 분의 배수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="475eb-133">Specify a multiple of 30 minutes.</span></span>

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

### <span data-ttu-id="475eb-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="475eb-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="475eb-135">유지 관리 기간이 시작 되는 시간 (일)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="475eb-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="475eb-136">이 시간은 업데이트가 설치 되기 시작 하는 시기를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="475eb-136">This time defines when updates start to install.</span></span>

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

### <span data-ttu-id="475eb-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="475eb-137">-PatchCategory</span></span>
<span data-ttu-id="475eb-138">중요 업데이트를 포함 해야 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="475eb-138">Specifies whether important updates should be included.</span></span>

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

### <span data-ttu-id="475eb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="475eb-139">CommonParameters</span></span>
<span data-ttu-id="475eb-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="475eb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="475eb-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="475eb-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="475eb-142">입력</span><span class="sxs-lookup"><span data-stu-id="475eb-142">INPUTS</span></span>

### <span data-ttu-id="475eb-143">않아야</span><span class="sxs-lookup"><span data-stu-id="475eb-143">None</span></span>

## <span data-ttu-id="475eb-144">출력</span><span class="sxs-lookup"><span data-stu-id="475eb-144">OUTPUTS</span></span>

### <span data-ttu-id="475eb-145">AutoPatchingSettings를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="475eb-145">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

## <span data-ttu-id="475eb-146">상속자</span><span class="sxs-lookup"><span data-stu-id="475eb-146">NOTES</span></span>

## <span data-ttu-id="475eb-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="475eb-147">RELATED LINKS</span></span>

[<span data-ttu-id="475eb-148">새로운 AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="475eb-148">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="475eb-149">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="475eb-149">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


