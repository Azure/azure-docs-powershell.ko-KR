---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D344
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/remove-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: 8e79fe1a0d0cc1c681c88cb3d5dfdd8d48dfd26b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987261"
---
# <span data-ttu-id="09546-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="09546-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="09546-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09546-102">SYNOPSIS</span></span>
<span data-ttu-id="09546-103">로컬 Traffic Manager 프로필 개체에서 예상 상태 코드 범위를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="09546-103">Removes an expected status code range from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="09546-104">구문</span><span class="sxs-lookup"><span data-stu-id="09546-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09546-105">설명</span><span class="sxs-lookup"><span data-stu-id="09546-105">DESCRIPTION</span></span>
<span data-ttu-id="09546-106">**Remove-AzTrafficManagerExpectedStatusCodeRange** cmdlet은 로컬 Azure Traffic Manager 프로필 개체에서 예상되는 상태 코드 범위를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="09546-106">The **Remove-AzTrafficManagerExpectedStatusCodeRange** cmdlet removes a range of expected status codes from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="09546-107">New-AzTrafficManagerProfile cmdlet을 사용하여 New-AzTrafficManagerProfile Get-AzTrafficManagerProfile 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="09546-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="09546-108">이 cmdlet은 로컬 프로필 개체에서 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="09546-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="09546-109">Set-AzTrafficManagerProfile cmdlet을 사용하여 Traffic Manager 프로필에 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="09546-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="09546-110">예제</span><span class="sxs-lookup"><span data-stu-id="09546-110">EXAMPLES</span></span>

### <span data-ttu-id="09546-111">예제 1: 프로필에서 예상 상태 코드 범위 제거</span><span class="sxs-lookup"><span data-stu-id="09546-111">Example 1: Remove an expected status code range from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="09546-112">첫 번째 명령은 **Get-AzTrafficManagerProfile** cmdlet을 사용하여 Azure Traffic Manager 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="09546-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="09546-113">두 번째 명령은 에 저장된 프로필에서 예상 상태 코드 범위를 $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="09546-113">The second command removes an expected status code range from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="09546-114">마지막 명령은 Traffic Manager의 프로필을 업데이트하여 로컬 값과 $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="09546-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="09546-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="09546-115">PARAMETERS</span></span>

### <span data-ttu-id="09546-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09546-116">-DefaultProfile</span></span>
<span data-ttu-id="09546-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="09546-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09546-118">-Min</span><span class="sxs-lookup"><span data-stu-id="09546-118">-Min</span></span>
<span data-ttu-id="09546-119">제거할 상태 코드 범위에서 가장 낮은 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="09546-119">Specifies the lowest value in the status code range to be removed.</span></span>

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

### <span data-ttu-id="09546-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="09546-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="09546-121">로컬 **TrafficManagerProfile** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="09546-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="09546-122">이 cmdlet은 이 로컬 개체를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="09546-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="09546-123">**TrafficManagerProfile** 개체를 얻은 경우 Get-AzTrafficManagerProfile cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="09546-123">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="09546-124">-확인</span><span class="sxs-lookup"><span data-stu-id="09546-124">-Confirm</span></span>
<span data-ttu-id="09546-125">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="09546-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09546-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09546-126">-WhatIf</span></span>
<span data-ttu-id="09546-127">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="09546-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="09546-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="09546-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09546-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09546-129">CommonParameters</span></span>
<span data-ttu-id="09546-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="09546-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09546-131">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="09546-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09546-132">입력</span><span class="sxs-lookup"><span data-stu-id="09546-132">INPUTS</span></span>

### <span data-ttu-id="09546-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="09546-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="09546-134">출력</span><span class="sxs-lookup"><span data-stu-id="09546-134">OUTPUTS</span></span>

### <span data-ttu-id="09546-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="09546-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="09546-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="09546-136">NOTES</span></span>

## <span data-ttu-id="09546-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="09546-137">RELATED LINKS</span></span>

[<span data-ttu-id="09546-138">Add-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="09546-138">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Add-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="09546-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="09546-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="09546-140">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="09546-140">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
