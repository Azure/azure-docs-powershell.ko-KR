---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D343
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagercustomheaderfromprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromProfile.md
ms.openlocfilehash: 62dbdfe69feddcbd942a51c05c65e486653a2405
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216378"
---
# <span data-ttu-id="d75af-101">Remove-AzTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="d75af-101">Remove-AzTrafficManagerCustomHeaderFromProfile</span></span>

## <span data-ttu-id="d75af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d75af-102">SYNOPSIS</span></span>
<span data-ttu-id="d75af-103">로컬 트래픽 관리자 프로필 개체에서 사용자 지정 헤더 정보를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d75af-103">Removes custom header information from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="d75af-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d75af-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerCustomHeaderFromProfile -Name <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d75af-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d75af-105">DESCRIPTION</span></span>
<span data-ttu-id="d75af-106">**AzTrafficManagerCustomHeaderFromProfile** cmdlet은 로컬 Azure Traffic Manager 프로필 개체에서 사용자 지정 헤더 정보를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d75af-106">The **Remove-AzTrafficManagerCustomHeaderFromProfile** cmdlet removes custom header information from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="d75af-107">New-AzTrafficManagerProfile 또는 Get-AzTrafficManagerProfile cmdlet을 사용 하 여 프로필을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d75af-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="d75af-108">이 cmdlet은 로컬 프로필 개체에서 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="d75af-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="d75af-109">Set-AzTrafficManagerProfile cmdlet을 사용 하 여 트래픽 관리자의 프로필에 대 한 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="d75af-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="d75af-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d75af-110">EXAMPLES</span></span>

### <span data-ttu-id="d75af-111">예제 1: 프로필에서 사용자 지정 헤더 정보 제거</span><span class="sxs-lookup"><span data-stu-id="d75af-111">Example 1: Remove custom header information from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerCustomHeaderFromEndpoint -TrafficManagerProfile $TrafficManagerProfile -Name "host"
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="d75af-112">첫 번째 명령은 **AzTrafficManagerProfile** cmdlet을 사용 하 여 Azure Traffic Manager 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d75af-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="d75af-113">두 번째 명령은 $TrafficManagerProfile에 저장 된 프로필에서 사용자 지정 헤더 정보를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d75af-113">The second command removes custom header information from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="d75af-114">마지막 명령은 $TrafficManagerProfile의 로컬 값과 일치 하도록 Traffic Manager에서 프로필을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d75af-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="d75af-115">변수</span><span class="sxs-lookup"><span data-stu-id="d75af-115">PARAMETERS</span></span>

### <span data-ttu-id="d75af-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d75af-116">-DefaultProfile</span></span>
<span data-ttu-id="d75af-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d75af-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d75af-118">-이름</span><span class="sxs-lookup"><span data-stu-id="d75af-118">-Name</span></span>
<span data-ttu-id="d75af-119">제거할 사용자 지정 머리글 정보의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d75af-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="d75af-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d75af-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="d75af-121">로컬 **TrafficManagerProfile** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d75af-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="d75af-122">이 cmdlet은이 로컬 개체를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d75af-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="d75af-123">**TrafficManagerProfile** 개체를 가져오려면 Get-AzTrafficManagerProfile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d75af-123">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="d75af-124">-확인</span><span class="sxs-lookup"><span data-stu-id="d75af-124">-Confirm</span></span>
<span data-ttu-id="d75af-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d75af-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d75af-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d75af-126">-WhatIf</span></span>
<span data-ttu-id="d75af-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d75af-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d75af-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d75af-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d75af-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d75af-129">CommonParameters</span></span>
<span data-ttu-id="d75af-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d75af-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d75af-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d75af-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d75af-132">입력</span><span class="sxs-lookup"><span data-stu-id="d75af-132">INPUTS</span></span>

### <span data-ttu-id="d75af-133">TrafficManager. TrafficManagerProfile/.</span><span class="sxs-lookup"><span data-stu-id="d75af-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="d75af-134">출력</span><span class="sxs-lookup"><span data-stu-id="d75af-134">OUTPUTS</span></span>

### <span data-ttu-id="d75af-135">TrafficManager. TrafficManagerProfile/.</span><span class="sxs-lookup"><span data-stu-id="d75af-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="d75af-136">상속자</span><span class="sxs-lookup"><span data-stu-id="d75af-136">NOTES</span></span>

## <span data-ttu-id="d75af-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d75af-137">RELATED LINKS</span></span>

[<span data-ttu-id="d75af-138">추가-AzTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="d75af-138">Add-AzTrafficManagerCustomHeaderToProfile</span></span>](./Add-AzTrafficManagerCustomHeaderToProfile.md)

[<span data-ttu-id="d75af-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d75af-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="d75af-140">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d75af-140">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
