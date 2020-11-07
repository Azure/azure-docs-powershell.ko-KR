---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D344
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: 8f26030f726d472024dd788abb02e55f8eac4c6e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874410"
---
# <span data-ttu-id="388e7-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="388e7-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="388e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="388e7-102">SYNOPSIS</span></span>
<span data-ttu-id="388e7-103">로컬 트래픽 관리자 프로필 개체에서 예상 되는 상태 코드 범위를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-103">Removes an expected status code range from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="388e7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="388e7-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="388e7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="388e7-105">DESCRIPTION</span></span>
<span data-ttu-id="388e7-106">**AzTrafficManagerExpectedStatusCodeRange** cmdlet은 로컬 Azure Traffic Manager 프로필 개체에서 예상 되는 상태 코드의 범위를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-106">The **Remove-AzTrafficManagerExpectedStatusCodeRange** cmdlet removes a range of expected status codes from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="388e7-107">New-AzTrafficManagerProfile 또는 Get-AzTrafficManagerProfile cmdlet을 사용 하 여 프로필을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="388e7-108">이 cmdlet은 로컬 프로필 개체에서 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="388e7-109">Set-AzTrafficManagerProfile cmdlet을 사용 하 여 트래픽 관리자의 프로필에 대 한 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="388e7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="388e7-110">EXAMPLES</span></span>

### <span data-ttu-id="388e7-111">예제 1: 프로필에서 예상 되는 상태 코드 범위 제거</span><span class="sxs-lookup"><span data-stu-id="388e7-111">Example 1: Remove an expected status code range from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="388e7-112">첫 번째 명령은 **AzTrafficManagerProfile** cmdlet을 사용 하 여 Azure Traffic Manager 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="388e7-113">두 번째 명령은 $TrafficManagerProfile에 저장 된 프로필에서 예상 되는 상태 코드 범위를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-113">The second command removes an expected status code range from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="388e7-114">마지막 명령은 $TrafficManagerProfile의 로컬 값과 일치 하도록 Traffic Manager에서 프로필을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="388e7-115">변수</span><span class="sxs-lookup"><span data-stu-id="388e7-115">PARAMETERS</span></span>

### <span data-ttu-id="388e7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="388e7-116">-DefaultProfile</span></span>
<span data-ttu-id="388e7-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="388e7-118">-Min</span><span class="sxs-lookup"><span data-stu-id="388e7-118">-Min</span></span>
<span data-ttu-id="388e7-119">상태 코드 범위에서 제거할 가장 낮은 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-119">Specifies the lowest value in the status code range to be removed.</span></span>

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

### <span data-ttu-id="388e7-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="388e7-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="388e7-121">로컬 **TrafficManagerProfile** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="388e7-122">이 cmdlet은이 로컬 개체를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="388e7-123">**TrafficManagerProfile** 개체를 가져오려면 Get-AzTrafficManagerProfile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-123">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="388e7-124">-확인</span><span class="sxs-lookup"><span data-stu-id="388e7-124">-Confirm</span></span>
<span data-ttu-id="388e7-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="388e7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="388e7-126">-WhatIf</span></span>
<span data-ttu-id="388e7-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="388e7-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="388e7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="388e7-129">CommonParameters</span></span>
<span data-ttu-id="388e7-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="388e7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="388e7-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="388e7-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="388e7-132">입력</span><span class="sxs-lookup"><span data-stu-id="388e7-132">INPUTS</span></span>

### <span data-ttu-id="388e7-133">TrafficManager. TrafficManagerProfile/.</span><span class="sxs-lookup"><span data-stu-id="388e7-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="388e7-134">출력</span><span class="sxs-lookup"><span data-stu-id="388e7-134">OUTPUTS</span></span>

### <span data-ttu-id="388e7-135">TrafficManager. TrafficManagerProfile/.</span><span class="sxs-lookup"><span data-stu-id="388e7-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="388e7-136">상속자</span><span class="sxs-lookup"><span data-stu-id="388e7-136">NOTES</span></span>

## <span data-ttu-id="388e7-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="388e7-137">RELATED LINKS</span></span>

[<span data-ttu-id="388e7-138">추가-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="388e7-138">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Add-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="388e7-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="388e7-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="388e7-140">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="388e7-140">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
