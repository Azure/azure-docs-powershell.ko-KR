---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 3ba7ab00076a3a0634a0d4394270fe4a83ec8ede
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398260"
---
# <span data-ttu-id="91ad7-101">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="91ad7-101">New-AzVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="91ad7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91ad7-102">SYNOPSIS</span></span>
<span data-ttu-id="91ad7-103">가상 머신에서 자동 패치를 위한 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91ad7-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="91ad7-104">구문</span><span class="sxs-lookup"><span data-stu-id="91ad7-104">SYNTAX</span></span>

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>]
 [-MaintenanceWindowStartingHour <Int32>] [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="91ad7-105">설명</span><span class="sxs-lookup"><span data-stu-id="91ad7-105">DESCRIPTION</span></span>
<span data-ttu-id="91ad7-106">**New-AzVMSqlServerAutoPatchingConfig** cmdlet은 가상 머신에서 자동 패치를 위한 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91ad7-106">The **New-AzVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="91ad7-107">예제</span><span class="sxs-lookup"><span data-stu-id="91ad7-107">EXAMPLES</span></span>

### <span data-ttu-id="91ad7-108">예제 1: 자동 패치를 구성하는 구성 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="91ad7-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="91ad7-109">이 명령은 패치를 위한 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91ad7-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="91ad7-110">이 명령은 주중 날을 지정하고 유지 관리 기간을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="91ad7-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="91ad7-111">이 구성은 이러한 값을 사용하는 패치를 가능하게 합니다.</span><span class="sxs-lookup"><span data-stu-id="91ad7-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="91ad7-112">이 명령은 결과 값을 $AutoBackupConfig 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="91ad7-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="91ad7-113">이 구성 항목은 cmdlet과 같은 다른 cmdlet에 Set-AzVMSqlServerExtension 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91ad7-113">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="91ad7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91ad7-114">PARAMETERS</span></span>

### <span data-ttu-id="91ad7-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="91ad7-115">-DayOfWeek</span></span>
<span data-ttu-id="91ad7-116">업데이트를 설치해야 하는 주중 날을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91ad7-116">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="91ad7-117">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="91ad7-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="91ad7-118">일요일</span><span class="sxs-lookup"><span data-stu-id="91ad7-118">Sunday</span></span>
- <span data-ttu-id="91ad7-119">월요일</span><span class="sxs-lookup"><span data-stu-id="91ad7-119">Monday</span></span>
- <span data-ttu-id="91ad7-120">화요일</span><span class="sxs-lookup"><span data-stu-id="91ad7-120">Tuesday</span></span>
- <span data-ttu-id="91ad7-121">수요일</span><span class="sxs-lookup"><span data-stu-id="91ad7-121">Wednesday</span></span>
- <span data-ttu-id="91ad7-122">목요일</span><span class="sxs-lookup"><span data-stu-id="91ad7-122">Thursday</span></span>
- <span data-ttu-id="91ad7-123">금요일</span><span class="sxs-lookup"><span data-stu-id="91ad7-123">Friday</span></span>
- <span data-ttu-id="91ad7-124">토요일</span><span class="sxs-lookup"><span data-stu-id="91ad7-124">Saturday</span></span>
- <span data-ttu-id="91ad7-125">매일</span><span class="sxs-lookup"><span data-stu-id="91ad7-125">Everyday</span></span>

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

### <span data-ttu-id="91ad7-126">-Enable</span><span class="sxs-lookup"><span data-stu-id="91ad7-126">-Enable</span></span>
<span data-ttu-id="91ad7-127">가상 머신에 대한 자동화된 패치가 사용하도록 설정되어 있는 경우를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="91ad7-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="91ad7-128">자동화된 패치를 사용하도록 설정하면 cmdlet에서 Windows 업데이트를 대화형 모드로 전환합니다.</span><span class="sxs-lookup"><span data-stu-id="91ad7-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="91ad7-129">자동화된 패치를 사용하지 않도록 설정하면 Windows 업데이트 설정이 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="91ad7-129">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="91ad7-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="91ad7-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="91ad7-131">유지 관리 기간의 기간(분)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91ad7-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="91ad7-132">자동화된 패치는 이 창 외부의 가상 머신 가용성에 영향을 줄 수 있는 작업을 수행하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="91ad7-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="91ad7-133">30분의 배수로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91ad7-133">Specify a multiple of 30 minutes.</span></span>

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

### <span data-ttu-id="91ad7-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="91ad7-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="91ad7-135">유지 관리 기간이 시작되는 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91ad7-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="91ad7-136">이번에는 업데이트 설치가 시작된 시기를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="91ad7-136">This time defines when updates start to install.</span></span>

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

### <span data-ttu-id="91ad7-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="91ad7-137">-PatchCategory</span></span>
<span data-ttu-id="91ad7-138">중요한 업데이트를 포함해야 하는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="91ad7-138">Specifies whether important updates should be included.</span></span>

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

### <span data-ttu-id="91ad7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91ad7-139">CommonParameters</span></span>
<span data-ttu-id="91ad7-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="91ad7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91ad7-141">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="91ad7-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91ad7-142">입력</span><span class="sxs-lookup"><span data-stu-id="91ad7-142">INPUTS</span></span>

### <span data-ttu-id="91ad7-143">없음</span><span class="sxs-lookup"><span data-stu-id="91ad7-143">None</span></span>
<span data-ttu-id="91ad7-144">이 cmdlet은 입력을 허용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="91ad7-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="91ad7-145">출력</span><span class="sxs-lookup"><span data-stu-id="91ad7-145">OUTPUTS</span></span>

### <span data-ttu-id="91ad7-146">AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="91ad7-146">AutoPatchingSettings</span></span>
<span data-ttu-id="91ad7-147">이 cmdlet은 자동화된 패치에 대한 설정을 포함하는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="91ad7-147">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="91ad7-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="91ad7-148">NOTES</span></span>

## <span data-ttu-id="91ad7-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91ad7-149">RELATED LINKS</span></span>

[<span data-ttu-id="91ad7-150">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="91ad7-150">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="91ad7-151">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="91ad7-151">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


