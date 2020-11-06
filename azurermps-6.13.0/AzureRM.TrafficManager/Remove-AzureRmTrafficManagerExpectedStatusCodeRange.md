---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D344
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: 0971a4b8d485c1590794de6f1b6c2d4d9d21da4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525920"
---
# <span data-ttu-id="0123b-101">Remove-AzureRmTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="0123b-101">Remove-AzureRmTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="0123b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0123b-102">SYNOPSIS</span></span>
<span data-ttu-id="0123b-103">로컬 트래픽 관리자 프로필 개체에서 예상 되는 상태 코드 범위를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0123b-103">Removes an expected status code range from a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0123b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0123b-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerExpectedStatusCodeRange -Min <Int32> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0123b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0123b-105">DESCRIPTION</span></span>
<span data-ttu-id="0123b-106">**AzureRmTrafficManagerExpectedStatusCodeRange** cmdlet은 로컬 Azure Traffic Manager 프로필 개체에서 예상 되는 상태 코드의 범위를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0123b-106">The **Remove-AzureRmTrafficManagerExpectedStatusCodeRange** cmdlet removes a range of expected status codes from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="0123b-107">New-AzureRmTrafficManagerProfile 또는 Get-AzureRmTrafficManagerProfile cmdlet을 사용 하 여 프로필을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0123b-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="0123b-108">이 cmdlet은 로컬 프로필 개체에서 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="0123b-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="0123b-109">Set-AzureRmTrafficManagerProfile cmdlet을 사용 하 여 트래픽 관리자의 프로필에 대 한 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="0123b-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="0123b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="0123b-110">EXAMPLES</span></span>

### <span data-ttu-id="0123b-111">예제 1: 프로필에서 예상 되는 상태 코드 범위 제거</span><span class="sxs-lookup"><span data-stu-id="0123b-111">Example 1: Remove an expected status code range from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzureRmTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="0123b-112">첫 번째 명령은 **AzureRmTrafficManagerProfile** cmdlet을 사용 하 여 Azure Traffic Manager 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0123b-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="0123b-113">두 번째 명령은 $TrafficManagerProfile에 저장 된 프로필에서 예상 되는 상태 코드 범위를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0123b-113">The second command removes an expected status code range from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="0123b-114">마지막 명령은 $TrafficManagerProfile의 로컬 값과 일치 하도록 Traffic Manager에서 프로필을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0123b-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="0123b-115">변수</span><span class="sxs-lookup"><span data-stu-id="0123b-115">PARAMETERS</span></span>

### <span data-ttu-id="0123b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0123b-116">-DefaultProfile</span></span>
<span data-ttu-id="0123b-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0123b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0123b-118">-Min</span><span class="sxs-lookup"><span data-stu-id="0123b-118">-Min</span></span>
<span data-ttu-id="0123b-119">상태 코드 범위에서 제거할 가장 낮은 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0123b-119">Specifies the lowest value in the status code range to be removed.</span></span>

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

### <span data-ttu-id="0123b-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0123b-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="0123b-121">로컬 **TrafficManagerProfile** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0123b-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="0123b-122">이 cmdlet은이 로컬 개체를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0123b-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="0123b-123">**TrafficManagerProfile** 개체를 가져오려면 Get-AzureRmTrafficManagerProfile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0123b-123">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="0123b-124">-확인</span><span class="sxs-lookup"><span data-stu-id="0123b-124">-Confirm</span></span>
<span data-ttu-id="0123b-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0123b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0123b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0123b-126">-WhatIf</span></span>
<span data-ttu-id="0123b-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0123b-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0123b-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0123b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0123b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0123b-129">CommonParameters</span></span>
<span data-ttu-id="0123b-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0123b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0123b-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0123b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0123b-132">입력</span><span class="sxs-lookup"><span data-stu-id="0123b-132">INPUTS</span></span>

### <span data-ttu-id="0123b-133">TrafficManagerProfile (Network.)</span><span class="sxs-lookup"><span data-stu-id="0123b-133">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="0123b-134">이 cmdlet은이 cmdlet에 대 한 **TrafficManagerProfile** 개체를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0123b-134">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="0123b-135">출력</span><span class="sxs-lookup"><span data-stu-id="0123b-135">OUTPUTS</span></span>

### <span data-ttu-id="0123b-136">TrafficManagerProfile (Network.)</span><span class="sxs-lookup"><span data-stu-id="0123b-136">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="0123b-137">이 cmdlet은 수정 된 **TrafficManagerProfile** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0123b-137">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="0123b-138">상속자</span><span class="sxs-lookup"><span data-stu-id="0123b-138">NOTES</span></span>

## <span data-ttu-id="0123b-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0123b-139">RELATED LINKS</span></span>

[<span data-ttu-id="0123b-140">추가-AzureRmTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="0123b-140">Add-AzureRmTrafficManagerExpectedStatusCodeRange</span></span>](./Add-AzureRmTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="0123b-141">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0123b-141">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="0123b-142">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0123b-142">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)
