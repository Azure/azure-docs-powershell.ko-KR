---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D340
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/add-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: 88755e6830342dc7636bdb0b338269c47bc23398
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987378"
---
# <span data-ttu-id="9ca59-101">Add-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="9ca59-101">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="9ca59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ca59-102">SYNOPSIS</span></span>
<span data-ttu-id="9ca59-103">로컬 Traffic Manager 프로필 개체에 예상 상태 코드 범위를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="9ca59-103">Adds an expected status code range to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="9ca59-104">구문</span><span class="sxs-lookup"><span data-stu-id="9ca59-104">SYNTAX</span></span>

```
Add-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -Max <Int32>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9ca59-105">설명</span><span class="sxs-lookup"><span data-stu-id="9ca59-105">DESCRIPTION</span></span>
<span data-ttu-id="9ca59-106">**Add-AzTrafficManagerExpectedStatusCodeRange** cmdlet은 로컬 Azure Traffic Manager 프로필 개체에 예상되는 상태 코드 범위를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="9ca59-106">The **Add-AzTrafficManagerExpectedStatusCodeRange** cmdlet adds a range of expected status codes to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="9ca59-107">New-AzTrafficManagerProfile cmdlet을 사용하여 New-AzTrafficManagerProfile Get-AzTrafficManagerProfile 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9ca59-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="9ca59-108">이 cmdlet은 로컬 프로필 개체에서 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="9ca59-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="9ca59-109">Set-AzTrafficManagerProfile cmdlet을 사용하여 Traffic Manager 프로필에 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="9ca59-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="9ca59-110">예제</span><span class="sxs-lookup"><span data-stu-id="9ca59-110">EXAMPLES</span></span>

### <span data-ttu-id="9ca59-111">예제 1: 프로필에 예상 상태 코드 범위 추가</span><span class="sxs-lookup"><span data-stu-id="9ca59-111">Example 1: Add an expected status code range to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200 -Max 499
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="9ca59-112">첫 번째 명령은 **Get-AzTrafficManagerProfile** cmdlet을 사용하여 Azure Traffic Manager 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9ca59-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="9ca59-113">명령은 로컬 프로필을 $TrafficManagerProfile 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="9ca59-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="9ca59-114">두 번째 명령은 에 저장된 프로필에 예상 상태 코드 범위를 $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="9ca59-114">The second command adds an expected status code range to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="9ca59-115">마지막 명령은 Traffic Manager의 프로필을 업데이트하여 로컬 값과 $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="9ca59-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="9ca59-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9ca59-116">PARAMETERS</span></span>

### <span data-ttu-id="9ca59-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ca59-117">-DefaultProfile</span></span>
<span data-ttu-id="9ca59-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9ca59-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ca59-119">-Max</span><span class="sxs-lookup"><span data-stu-id="9ca59-119">-Max</span></span>
<span data-ttu-id="9ca59-120">추가할 상태 코드 범위에서 가장 높은 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9ca59-120">Specifies the highest value in the status code range to be added.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ca59-121">-Min</span><span class="sxs-lookup"><span data-stu-id="9ca59-121">-Min</span></span>
<span data-ttu-id="9ca59-122">추가할 상태 코드 범위에서 가장 낮은 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9ca59-122">Specifies the lowest value in the status code range to be added.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ca59-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9ca59-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="9ca59-124">로컬 **TrafficManagerProfile** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9ca59-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="9ca59-125">이 cmdlet은 이 로컬 개체를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="9ca59-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="9ca59-126">**TrafficManagerProfile** 개체를 얻은 경우 Get-AzTrafficManagerProfile cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="9ca59-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ca59-127">-확인</span><span class="sxs-lookup"><span data-stu-id="9ca59-127">-Confirm</span></span>
<span data-ttu-id="9ca59-128">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ca59-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ca59-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ca59-129">-WhatIf</span></span>
<span data-ttu-id="9ca59-130">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9ca59-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9ca59-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9ca59-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ca59-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ca59-132">CommonParameters</span></span>
<span data-ttu-id="9ca59-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9ca59-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ca59-134">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9ca59-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ca59-135">입력</span><span class="sxs-lookup"><span data-stu-id="9ca59-135">INPUTS</span></span>

### <span data-ttu-id="9ca59-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9ca59-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="9ca59-137">출력</span><span class="sxs-lookup"><span data-stu-id="9ca59-137">OUTPUTS</span></span>

### <span data-ttu-id="9ca59-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9ca59-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="9ca59-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9ca59-139">NOTES</span></span>

## <span data-ttu-id="9ca59-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ca59-140">RELATED LINKS</span></span>

[<span data-ttu-id="9ca59-141">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="9ca59-141">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Remove-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="9ca59-142">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9ca59-142">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="9ca59-143">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9ca59-143">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
