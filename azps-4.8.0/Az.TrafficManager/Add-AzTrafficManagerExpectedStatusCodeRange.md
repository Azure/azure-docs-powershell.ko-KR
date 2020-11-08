---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D340
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: ee249b7e3d811a527a9322e09ba65075883e73b6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212024"
---
# <span data-ttu-id="19cc3-101">Add-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="19cc3-101">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="19cc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19cc3-102">SYNOPSIS</span></span>
<span data-ttu-id="19cc3-103">로컬 트래픽 관리자 프로필 개체에 예상 상태 코드 범위를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="19cc3-103">Adds an expected status code range to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="19cc3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="19cc3-104">SYNTAX</span></span>

```
Add-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -Max <Int32>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="19cc3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="19cc3-105">DESCRIPTION</span></span>
<span data-ttu-id="19cc3-106">**AzTrafficManagerExpectedStatusCodeRange** cmdlet은 로컬 Azure Traffic Manager 프로필 개체에 예상 상태 코드의 범위를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="19cc3-106">The **Add-AzTrafficManagerExpectedStatusCodeRange** cmdlet adds a range of expected status codes to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="19cc3-107">New-AzTrafficManagerProfile 또는 Get-AzTrafficManagerProfile cmdlet을 사용 하 여 프로필을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19cc3-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="19cc3-108">이 cmdlet은 로컬 프로필 개체에서 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="19cc3-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="19cc3-109">Set-AzTrafficManagerProfile cmdlet을 사용 하 여 트래픽 관리자의 프로필에 대 한 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="19cc3-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="19cc3-110">예제의</span><span class="sxs-lookup"><span data-stu-id="19cc3-110">EXAMPLES</span></span>

### <span data-ttu-id="19cc3-111">예제 1: 프로필에 예상 상태 코드 범위 추가</span><span class="sxs-lookup"><span data-stu-id="19cc3-111">Example 1: Add an expected status code range to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200 -Max 499
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="19cc3-112">첫 번째 명령은 **AzTrafficManagerProfile** cmdlet을 사용 하 여 Azure Traffic Manager 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="19cc3-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="19cc3-113">명령은 로컬 프로필을 $TrafficManagerProfile 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="19cc3-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="19cc3-114">두 번째 명령은 $TrafficManagerProfile에 저장 된 프로필에 예상 상태 코드 범위를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="19cc3-114">The second command adds an expected status code range to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="19cc3-115">마지막 명령은 $TrafficManagerProfile의 로컬 값과 일치 하도록 Traffic Manager에서 프로필을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="19cc3-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="19cc3-116">변수</span><span class="sxs-lookup"><span data-stu-id="19cc3-116">PARAMETERS</span></span>

### <span data-ttu-id="19cc3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19cc3-117">-DefaultProfile</span></span>
<span data-ttu-id="19cc3-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="19cc3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19cc3-119">-최대</span><span class="sxs-lookup"><span data-stu-id="19cc3-119">-Max</span></span>
<span data-ttu-id="19cc3-120">추가할 상태 코드 범위의 가장 높은 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19cc3-120">Specifies the highest value in the status code range to be added.</span></span>

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

### <span data-ttu-id="19cc3-121">-Min</span><span class="sxs-lookup"><span data-stu-id="19cc3-121">-Min</span></span>
<span data-ttu-id="19cc3-122">상태 코드 범위에서 추가할 가장 낮은 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19cc3-122">Specifies the lowest value in the status code range to be added.</span></span>

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

### <span data-ttu-id="19cc3-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="19cc3-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="19cc3-124">로컬 **TrafficManagerProfile** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19cc3-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="19cc3-125">이 cmdlet은이 로컬 개체를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19cc3-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="19cc3-126">**TrafficManagerProfile** 개체를 가져오려면 Get-AzTrafficManagerProfile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="19cc3-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="19cc3-127">-확인</span><span class="sxs-lookup"><span data-stu-id="19cc3-127">-Confirm</span></span>
<span data-ttu-id="19cc3-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="19cc3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19cc3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19cc3-129">-WhatIf</span></span>
<span data-ttu-id="19cc3-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="19cc3-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="19cc3-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="19cc3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19cc3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19cc3-132">CommonParameters</span></span>
<span data-ttu-id="19cc3-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="19cc3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19cc3-134">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19cc3-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19cc3-135">입력</span><span class="sxs-lookup"><span data-stu-id="19cc3-135">INPUTS</span></span>

### <span data-ttu-id="19cc3-136">TrafficManager. TrafficManagerProfile/.</span><span class="sxs-lookup"><span data-stu-id="19cc3-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="19cc3-137">출력</span><span class="sxs-lookup"><span data-stu-id="19cc3-137">OUTPUTS</span></span>

### <span data-ttu-id="19cc3-138">TrafficManager. TrafficManagerProfile/.</span><span class="sxs-lookup"><span data-stu-id="19cc3-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="19cc3-139">상속자</span><span class="sxs-lookup"><span data-stu-id="19cc3-139">NOTES</span></span>

## <span data-ttu-id="19cc3-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="19cc3-140">RELATED LINKS</span></span>

[<span data-ttu-id="19cc3-141">제거-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="19cc3-141">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Remove-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="19cc3-142">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="19cc3-142">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="19cc3-143">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="19cc3-143">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
