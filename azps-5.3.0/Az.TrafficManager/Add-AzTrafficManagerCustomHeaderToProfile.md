---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToProfile.md
ms.openlocfilehash: b90e83a403be59f5c454c0c055f0fe4719c3116f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382985"
---
# <span data-ttu-id="6d3ea-101">Add-AzTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="6d3ea-101">Add-AzTrafficManagerCustomHeaderToProfile</span></span>

## <span data-ttu-id="6d3ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d3ea-102">SYNOPSIS</span></span>
<span data-ttu-id="6d3ea-103">로컬 Traffic Manager 프로필 개체에 사용자 지정 헤더 정보를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6d3ea-103">Adds custom header information to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="6d3ea-104">구문</span><span class="sxs-lookup"><span data-stu-id="6d3ea-104">SYNTAX</span></span>

```
Add-AzTrafficManagerCustomHeaderToProfile -Name <String> -Value <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6d3ea-105">설명</span><span class="sxs-lookup"><span data-stu-id="6d3ea-105">DESCRIPTION</span></span>
<span data-ttu-id="6d3ea-106">**Add-AzTrafficManagerCustomHeaderToProfile** cmdlet은 로컬 Azure Traffic Manager 프로필 개체에 사용자 지정 헤더 정보를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="6d3ea-106">The **Add-AzTrafficManagerCustomHeaderToProfile** cmdlet adds custom header information to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="6d3ea-107">New-AzTrafficManagerProfile cmdlet을 사용하여 프로필을 Get-AzTrafficManagerProfile 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6d3ea-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="6d3ea-108">이 cmdlet은 로컬 프로필 개체에서 작동됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d3ea-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="6d3ea-109">Set-AzTrafficManagerProfile cmdlet을 사용하여 Traffic Manager에 대한 프로필에 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="6d3ea-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="6d3ea-110">예제</span><span class="sxs-lookup"><span data-stu-id="6d3ea-110">EXAMPLES</span></span>

### <span data-ttu-id="6d3ea-111">예제 1: 프로필에 사용자 지정 헤더 정보 추가</span><span class="sxs-lookup"><span data-stu-id="6d3ea-111">Example 1: Add custom header information to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerCustomHeaderToProfile -TrafficManagerProfile $TrafficManagerProfile -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="6d3ea-112">첫 번째 명령은 **Get-AzTrafficManagerProfile** cmdlet을 사용하여 Azure Traffic Manager 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6d3ea-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="6d3ea-113">이 명령은 로컬 프로필을 $TrafficManagerProfile 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="6d3ea-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="6d3ea-114">두 번째 명령은 사용자 지정 헤더 정보를 사용자 지정 헤더에 저장된 프로필에 $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="6d3ea-114">The second command adds custom header information to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="6d3ea-115">마지막 명령은 Traffic Manager의 프로필을 업데이트하여 트래픽 관리자의 로컬 값과 $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="6d3ea-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="6d3ea-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d3ea-116">PARAMETERS</span></span>

### <span data-ttu-id="6d3ea-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d3ea-117">-DefaultProfile</span></span>
<span data-ttu-id="6d3ea-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6d3ea-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d3ea-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6d3ea-119">-Name</span></span>
<span data-ttu-id="6d3ea-120">추가할 사용자 지정 헤더 정보의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6d3ea-120">Specifies the name of the custom header information to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d3ea-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6d3ea-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="6d3ea-122">로컬 **TrafficManagerProfile** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6d3ea-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="6d3ea-123">이 cmdlet은 이 로컬 개체를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="6d3ea-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="6d3ea-124">**TrafficManagerProfile** 개체를 얻습니다. Get-AzTrafficManagerProfile cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="6d3ea-124">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="6d3ea-125">-Value</span><span class="sxs-lookup"><span data-stu-id="6d3ea-125">-Value</span></span>
<span data-ttu-id="6d3ea-126">추가할 사용자 지정 헤더 정보의 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6d3ea-126">Specifies the value of the custom header information to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d3ea-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d3ea-127">-Confirm</span></span>
<span data-ttu-id="6d3ea-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d3ea-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d3ea-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d3ea-129">-WhatIf</span></span>
<span data-ttu-id="6d3ea-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6d3ea-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6d3ea-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6d3ea-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d3ea-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d3ea-132">CommonParameters</span></span>
<span data-ttu-id="6d3ea-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6d3ea-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d3ea-134">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6d3ea-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d3ea-135">입력</span><span class="sxs-lookup"><span data-stu-id="6d3ea-135">INPUTS</span></span>

### <span data-ttu-id="6d3ea-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6d3ea-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="6d3ea-137">출력</span><span class="sxs-lookup"><span data-stu-id="6d3ea-137">OUTPUTS</span></span>

### <span data-ttu-id="6d3ea-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6d3ea-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="6d3ea-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6d3ea-139">NOTES</span></span>

## <span data-ttu-id="6d3ea-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6d3ea-140">RELATED LINKS</span></span>

[<span data-ttu-id="6d3ea-141">Remove-AzTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="6d3ea-141">Remove-AzTrafficManagerCustomHeaderFromProfile</span></span>](./Remove-AzTrafficManagerCustomHeaderFromProfile.md)

[<span data-ttu-id="6d3ea-142">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6d3ea-142">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="6d3ea-143">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6d3ea-143">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
