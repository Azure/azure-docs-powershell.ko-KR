---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/set-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
ms.openlocfilehash: 4a4d09fb0e44dcb09781b2155e1bfe2d10a0cc80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987210"
---
# <span data-ttu-id="ce1ae-101">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ce1ae-101">Set-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="ce1ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce1ae-102">SYNOPSIS</span></span>
<span data-ttu-id="ce1ae-103">Traffic Manager 프로필을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1ae-103">Updates a Traffic Manager profile.</span></span>

## <span data-ttu-id="ce1ae-104">구문</span><span class="sxs-lookup"><span data-stu-id="ce1ae-104">SYNTAX</span></span>

```
Set-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce1ae-105">설명</span><span class="sxs-lookup"><span data-stu-id="ce1ae-105">DESCRIPTION</span></span>
<span data-ttu-id="ce1ae-106">**Set-AzTrafficManagerProfile** cmdlet은 Azure Traffic Manager 프로필을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1ae-106">The **Set-AzTrafficManagerProfile** cmdlet updates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="ce1ae-107">이 cmdlet은 로컬 프로필 개체에서 프로필의 설정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1ae-107">This cmdlet updates the settings of the profile from a local profile object.</span></span>
<span data-ttu-id="ce1ae-108">*TrafficManagerProfile* 매개 변수를 사용하거나 파이프라인을 사용하여 프로필 개체를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce1ae-108">You can specify the profile object either by using the *TrafficManagerProfile* parameter or by using the pipeline.</span></span>

<span data-ttu-id="ce1ae-109">cmdlet을 사용하여 프로필을 나타내는 로컬 개체를 Get-AzTrafficManagerProfile 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce1ae-109">You can obtain a local object that represents a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="ce1ae-110">개체를 로컬로 수정한 다음 **Set-AzTrafficManagerProfile을** 사용하여 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1ae-110">Modify the object locally and then use **Set-AzTrafficManagerProfile** to commit your changes.</span></span>

## <span data-ttu-id="ce1ae-111">예제</span><span class="sxs-lookup"><span data-stu-id="ce1ae-111">EXAMPLES</span></span>

### <span data-ttu-id="ce1ae-112">예제 1: 프로필 업데이트</span><span class="sxs-lookup"><span data-stu-id="ce1ae-112">Example 1: Update a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="ce1ae-113">첫 번째 명령은 Get-AzTrafficManagerProfile cmdlet을 사용하여 Azure Traffic Manager 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ce1ae-113">The first command gets an Azure Traffic Manager profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="ce1ae-114">명령은 프로필을 로컬로 $TrafficManagerProfile 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1ae-114">The command stores the profile locally in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="ce1ae-115">두 번째 명령은 로컬로 프로필을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1ae-115">The second command changes that profile locally.</span></span>
<span data-ttu-id="ce1ae-116">이 명령은 프로필을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1ae-116">This command disables the profile.</span></span>

<span data-ttu-id="ce1ae-117">세 번째 명령은 ContosoProfile이라는 Traffic Manager 프로필을 업데이트하여 로컬 값과 $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="ce1ae-117">The third command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="ce1ae-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ce1ae-118">PARAMETERS</span></span>

### <span data-ttu-id="ce1ae-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce1ae-119">-DefaultProfile</span></span>
<span data-ttu-id="ce1ae-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ce1ae-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce1ae-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ce1ae-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="ce1ae-122">로컬 **TrafficManagerProfile** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1ae-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="ce1ae-123">이 cmdlet은 Traffic Manager를 업데이트하여 이 로컬 개체와 일치합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1ae-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="ce1ae-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce1ae-124">CommonParameters</span></span>
<span data-ttu-id="ce1ae-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ce1ae-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce1ae-126">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ce1ae-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce1ae-127">입력</span><span class="sxs-lookup"><span data-stu-id="ce1ae-127">INPUTS</span></span>

### <span data-ttu-id="ce1ae-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ce1ae-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="ce1ae-129">출력</span><span class="sxs-lookup"><span data-stu-id="ce1ae-129">OUTPUTS</span></span>

### <span data-ttu-id="ce1ae-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ce1ae-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="ce1ae-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ce1ae-131">NOTES</span></span>

## <span data-ttu-id="ce1ae-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ce1ae-132">RELATED LINKS</span></span>

[<span data-ttu-id="ce1ae-133">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="ce1ae-133">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="ce1ae-134">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ce1ae-134">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="ce1ae-135">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ce1ae-135">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="ce1ae-136">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="ce1ae-136">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="ce1ae-137">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ce1ae-137">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)


