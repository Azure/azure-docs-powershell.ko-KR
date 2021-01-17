---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
ms.openlocfilehash: 8f774ab221160a94ee4e8b5f13780b7e3131f252
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330374"
---
# <span data-ttu-id="0a082-101">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0a082-101">Set-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="0a082-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a082-102">SYNOPSIS</span></span>
<span data-ttu-id="0a082-103">Traffic Manager 프로필을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0a082-103">Updates a Traffic Manager profile.</span></span>

## <span data-ttu-id="0a082-104">구문</span><span class="sxs-lookup"><span data-stu-id="0a082-104">SYNTAX</span></span>

```
Set-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a082-105">설명</span><span class="sxs-lookup"><span data-stu-id="0a082-105">DESCRIPTION</span></span>
<span data-ttu-id="0a082-106">**Set-AzTrafficManagerProfile** cmdlet은 Azure Traffic Manager 프로필을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0a082-106">The **Set-AzTrafficManagerProfile** cmdlet updates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="0a082-107">이 cmdlet은 로컬 프로필 개체에서 프로필 설정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0a082-107">This cmdlet updates the settings of the profile from a local profile object.</span></span>
<span data-ttu-id="0a082-108">*TrafficManagerProfile* 매개 변수를 사용하거나 파이프라인을 사용하여 프로필 개체를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0a082-108">You can specify the profile object either by using the *TrafficManagerProfile* parameter or by using the pipeline.</span></span>

<span data-ttu-id="0a082-109">Get-AzTrafficManagerProfile cmdlet을 사용하여 프로필을 나타내는 로컬 개체를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0a082-109">You can obtain a local object that represents a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="0a082-110">개체를 로컬로 수정한 다음 **Set-AzTrafficManagerProfile을** 사용하여 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="0a082-110">Modify the object locally and then use **Set-AzTrafficManagerProfile** to commit your changes.</span></span>

## <span data-ttu-id="0a082-111">예제</span><span class="sxs-lookup"><span data-stu-id="0a082-111">EXAMPLES</span></span>

### <span data-ttu-id="0a082-112">예제 1: 프로필 업데이트</span><span class="sxs-lookup"><span data-stu-id="0a082-112">Example 1: Update a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="0a082-113">첫 번째 명령은 Get-AzTrafficManagerProfile cmdlet을 사용하여 Azure Traffic Manager 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0a082-113">The first command gets an Azure Traffic Manager profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="0a082-114">이 명령은 프로필을 로컬로 $TrafficManagerProfile 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="0a082-114">The command stores the profile locally in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="0a082-115">두 번째 명령은 로컬로 프로파일을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="0a082-115">The second command changes that profile locally.</span></span>
<span data-ttu-id="0a082-116">이 명령은 프로필을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="0a082-116">This command disables the profile.</span></span>

<span data-ttu-id="0a082-117">세 번째 명령은 ContosoProfile이라는 Traffic Manager 프로필을 업데이트하여 $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="0a082-117">The third command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="0a082-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a082-118">PARAMETERS</span></span>

### <span data-ttu-id="0a082-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a082-119">-DefaultProfile</span></span>
<span data-ttu-id="0a082-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0a082-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a082-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0a082-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="0a082-122">로컬 **TrafficManagerProfile** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0a082-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="0a082-123">이 cmdlet은 Traffic Manager를 이 로컬 개체와 일치하게 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0a082-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="0a082-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a082-124">CommonParameters</span></span>
<span data-ttu-id="0a082-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0a082-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a082-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0a082-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a082-127">입력</span><span class="sxs-lookup"><span data-stu-id="0a082-127">INPUTS</span></span>

### <span data-ttu-id="0a082-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0a082-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="0a082-129">출력</span><span class="sxs-lookup"><span data-stu-id="0a082-129">OUTPUTS</span></span>

### <span data-ttu-id="0a082-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0a082-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="0a082-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0a082-131">NOTES</span></span>

## <span data-ttu-id="0a082-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0a082-132">RELATED LINKS</span></span>

[<span data-ttu-id="0a082-133">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="0a082-133">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="0a082-134">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0a082-134">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="0a082-135">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0a082-135">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="0a082-136">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="0a082-136">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="0a082-137">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0a082-137">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)


