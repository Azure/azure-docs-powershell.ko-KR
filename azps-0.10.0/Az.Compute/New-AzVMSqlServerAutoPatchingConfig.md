---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 0ce851373ac31aaef4c5664db7085f345e9b947d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876990"
---
# <span data-ttu-id="893a0-101">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="893a0-101">New-AzVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="893a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="893a0-102">SYNOPSIS</span></span>
<span data-ttu-id="893a0-103">가상 컴퓨터에 자동으로 패치할 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="893a0-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="893a0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="893a0-104">SYNTAX</span></span>

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>]
 [-MaintenanceWindowStartingHour <Int32>] [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="893a0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="893a0-105">DESCRIPTION</span></span>
<span data-ttu-id="893a0-106">**AzVMSqlServerAutoPatchingConfig** cmdlet은 가상 컴퓨터에 자동으로 패치를 적용 하기 위한 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="893a0-106">The **New-AzVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="893a0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="893a0-107">EXAMPLES</span></span>

### <span data-ttu-id="893a0-108">예제 1: 자동 패치를 구성 하는 구성 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="893a0-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="893a0-109">이 명령은 패칭에 대 한 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="893a0-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="893a0-110">이 명령은 요일을 지정 하 고 유지 관리 기간을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="893a0-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="893a0-111">이 구성은 이러한 값을 사용 하는 패치를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="893a0-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="893a0-112">명령이 $AutoBackupConfig 변수에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="893a0-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="893a0-113">Set-AzVMSqlServerExtension cmdlet 등의 다른 cmdlet에 대해이 구성 항목을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="893a0-113">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="893a0-114">변수</span><span class="sxs-lookup"><span data-stu-id="893a0-114">PARAMETERS</span></span>

### <span data-ttu-id="893a0-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="893a0-115">-DayOfWeek</span></span>
<span data-ttu-id="893a0-116">업데이트를 설치 해야 하는 요일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="893a0-116">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="893a0-117">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="893a0-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="893a0-118">나타내고</span><span class="sxs-lookup"><span data-stu-id="893a0-118">Sunday</span></span>
- <span data-ttu-id="893a0-119">월요일</span><span class="sxs-lookup"><span data-stu-id="893a0-119">Monday</span></span>
- <span data-ttu-id="893a0-120">시간은</span><span class="sxs-lookup"><span data-stu-id="893a0-120">Tuesday</span></span>
- <span data-ttu-id="893a0-121">일</span><span class="sxs-lookup"><span data-stu-id="893a0-121">Wednesday</span></span>
- <span data-ttu-id="893a0-122">목요일</span><span class="sxs-lookup"><span data-stu-id="893a0-122">Thursday</span></span>
- <span data-ttu-id="893a0-123">금요일</span><span class="sxs-lookup"><span data-stu-id="893a0-123">Friday</span></span>
- <span data-ttu-id="893a0-124">토요일</span><span class="sxs-lookup"><span data-stu-id="893a0-124">Saturday</span></span>
- <span data-ttu-id="893a0-125">매일</span><span class="sxs-lookup"><span data-stu-id="893a0-125">Everyday</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Everyday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="893a0-126">-사용</span><span class="sxs-lookup"><span data-stu-id="893a0-126">-Enable</span></span>
<span data-ttu-id="893a0-127">가상 컴퓨터에 대 한 자동 패치가 활성화 되어 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="893a0-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="893a0-128">자동 패치를 사용 하도록 설정 하면 cmdlet이 Windows Update를 대화형 모드로 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="893a0-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="893a0-129">자동 패치를 사용 하지 않도록 설정 하는 경우 Windows 업데이트 설정이 변경 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="893a0-129">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="893a0-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="893a0-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="893a0-131">유지 관리 기간의 기간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="893a0-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="893a0-132">자동화 된 패치는 해당 창 외부의 가상 컴퓨터 가용성에 영향을 줄 수 있는 작업을 수행 하지 않도록 방지 합니다.</span><span class="sxs-lookup"><span data-stu-id="893a0-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="893a0-133">30 분의 배수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="893a0-133">Specify a multiple of 30 minutes.</span></span>

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

### <span data-ttu-id="893a0-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="893a0-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="893a0-135">유지 관리 기간이 시작 되는 시간 (일)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="893a0-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="893a0-136">이 시간은 업데이트가 설치 되기 시작 하는 시기를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="893a0-136">This time defines when updates start to install.</span></span>

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

### <span data-ttu-id="893a0-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="893a0-137">-PatchCategory</span></span>
<span data-ttu-id="893a0-138">중요 업데이트를 포함 해야 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="893a0-138">Specifies whether important updates should be included.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Important

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="893a0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="893a0-139">CommonParameters</span></span>
<span data-ttu-id="893a0-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="893a0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="893a0-141">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="893a0-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="893a0-142">입력</span><span class="sxs-lookup"><span data-stu-id="893a0-142">INPUTS</span></span>

### <span data-ttu-id="893a0-143">않아야</span><span class="sxs-lookup"><span data-stu-id="893a0-143">None</span></span>
<span data-ttu-id="893a0-144">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="893a0-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="893a0-145">출력</span><span class="sxs-lookup"><span data-stu-id="893a0-145">OUTPUTS</span></span>

### <span data-ttu-id="893a0-146">AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="893a0-146">AutoPatchingSettings</span></span>
<span data-ttu-id="893a0-147">이 cmdlet은 자동 패칭에 대 한 설정을 포함 하는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="893a0-147">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="893a0-148">상속자</span><span class="sxs-lookup"><span data-stu-id="893a0-148">NOTES</span></span>

## <span data-ttu-id="893a0-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="893a0-149">RELATED LINKS</span></span>

[<span data-ttu-id="893a0-150">새로운 AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="893a0-150">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzureVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="893a0-151">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="893a0-151">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


