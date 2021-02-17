---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D344
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: fdada94847fdf2f83141f7cca63da61ead6fcd2c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190524"
---
# <span data-ttu-id="66b99-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="66b99-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="66b99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66b99-102">SYNOPSIS</span></span>
<span data-ttu-id="66b99-103">로컬 Traffic Manager 프로필 개체에서 예상되는 상태 코드 범위를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="66b99-103">Removes an expected status code range from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="66b99-104">구문</span><span class="sxs-lookup"><span data-stu-id="66b99-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66b99-105">설명</span><span class="sxs-lookup"><span data-stu-id="66b99-105">DESCRIPTION</span></span>
<span data-ttu-id="66b99-106">**Remove-AzTrafficManagerExpectedStatusCodeRange** cmdlet은 로컬 Azure Traffic Manager 프로필 개체에서 예상되는 상태 코드 범위를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="66b99-106">The **Remove-AzTrafficManagerExpectedStatusCodeRange** cmdlet removes a range of expected status codes from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="66b99-107">New-AzTrafficManagerProfile cmdlet을 사용하여 프로필을 Get-AzTrafficManagerProfile 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66b99-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="66b99-108">이 cmdlet은 로컬 프로필 개체에서 작동됩니다.</span><span class="sxs-lookup"><span data-stu-id="66b99-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="66b99-109">Set-AzTrafficManagerProfile cmdlet을 사용하여 Traffic Manager에 대한 프로필에 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="66b99-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="66b99-110">예제</span><span class="sxs-lookup"><span data-stu-id="66b99-110">EXAMPLES</span></span>

### <span data-ttu-id="66b99-111">예제 1: 프로필에서 예상되는 상태 코드 범위 제거</span><span class="sxs-lookup"><span data-stu-id="66b99-111">Example 1: Remove an expected status code range from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="66b99-112">첫 번째 명령은 **Get-AzTrafficManagerProfile** cmdlet을 사용하여 Azure Traffic Manager 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="66b99-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="66b99-113">두 번째 명령은 예상되는 상태 코드 범위를 이 명령에 저장된 프로필에서 $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="66b99-113">The second command removes an expected status code range from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="66b99-114">마지막 명령은 Traffic Manager의 프로필을 업데이트하여 트래픽 관리자의 로컬 값과 $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="66b99-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="66b99-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66b99-115">PARAMETERS</span></span>

### <span data-ttu-id="66b99-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66b99-116">-DefaultProfile</span></span>
<span data-ttu-id="66b99-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="66b99-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66b99-118">-Min</span><span class="sxs-lookup"><span data-stu-id="66b99-118">-Min</span></span>
<span data-ttu-id="66b99-119">제거할 상태 코드 범위에서 가장 낮은 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="66b99-119">Specifies the lowest value in the status code range to be removed.</span></span>

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

### <span data-ttu-id="66b99-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="66b99-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="66b99-121">로컬 **TrafficManagerProfile** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="66b99-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="66b99-122">이 cmdlet은 이 로컬 개체를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="66b99-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="66b99-123">**TrafficManagerProfile** 개체를 얻습니다. Get-AzTrafficManagerProfile cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="66b99-123">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="66b99-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="66b99-124">-Confirm</span></span>
<span data-ttu-id="66b99-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="66b99-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66b99-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66b99-126">-WhatIf</span></span>
<span data-ttu-id="66b99-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="66b99-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="66b99-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="66b99-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66b99-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66b99-129">CommonParameters</span></span>
<span data-ttu-id="66b99-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="66b99-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66b99-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="66b99-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66b99-132">입력</span><span class="sxs-lookup"><span data-stu-id="66b99-132">INPUTS</span></span>

### <span data-ttu-id="66b99-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="66b99-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="66b99-134">출력</span><span class="sxs-lookup"><span data-stu-id="66b99-134">OUTPUTS</span></span>

### <span data-ttu-id="66b99-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="66b99-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="66b99-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="66b99-136">NOTES</span></span>

## <span data-ttu-id="66b99-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="66b99-137">RELATED LINKS</span></span>

[<span data-ttu-id="66b99-138">Add-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="66b99-138">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Add-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="66b99-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="66b99-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="66b99-140">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="66b99-140">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
