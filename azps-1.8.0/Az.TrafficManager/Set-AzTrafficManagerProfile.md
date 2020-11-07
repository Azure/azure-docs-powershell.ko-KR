---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
ms.openlocfilehash: d8f4b5e069ef273dedc8e2e5a1f929d1649aefdb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698381"
---
# <span data-ttu-id="73397-101">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="73397-101">Set-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="73397-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73397-102">SYNOPSIS</span></span>
<span data-ttu-id="73397-103">Traffic Manager 프로필을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="73397-103">Updates a Traffic Manager profile.</span></span>

## <span data-ttu-id="73397-104">구문과</span><span class="sxs-lookup"><span data-stu-id="73397-104">SYNTAX</span></span>

```
Set-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73397-105">설명은</span><span class="sxs-lookup"><span data-stu-id="73397-105">DESCRIPTION</span></span>
<span data-ttu-id="73397-106">**AzTrafficManagerProfile** Cmdlet은 Azure Traffic Manager 프로필을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="73397-106">The **Set-AzTrafficManagerProfile** cmdlet updates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="73397-107">이 cmdlet은 로컬 프로필 개체의 프로필 설정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="73397-107">This cmdlet updates the settings of the profile from a local profile object.</span></span>
<span data-ttu-id="73397-108">*TrafficManagerProfile* 매개 변수를 사용 하거나 파이프라인을 사용 하 여 프로필 개체를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73397-108">You can specify the profile object either by using the *TrafficManagerProfile* parameter or by using the pipeline.</span></span>

<span data-ttu-id="73397-109">Get-AzTrafficManagerProfile cmdlet을 사용 하 여 프로필을 나타내는 로컬 개체를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73397-109">You can obtain a local object that represents a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="73397-110">개체를 로컬로 수정한 다음 **Set-AzTrafficManagerProfile** 를 사용 하 여 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="73397-110">Modify the object locally and then use **Set-AzTrafficManagerProfile** to commit your changes.</span></span>

## <span data-ttu-id="73397-111">예제의</span><span class="sxs-lookup"><span data-stu-id="73397-111">EXAMPLES</span></span>

### <span data-ttu-id="73397-112">예제 1: 프로필 업데이트</span><span class="sxs-lookup"><span data-stu-id="73397-112">Example 1: Update a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="73397-113">첫 번째 명령은 Get-AzTrafficManagerProfile cmdlet을 사용 하 여 Azure Traffic Manager 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="73397-113">The first command gets an Azure Traffic Manager profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="73397-114">명령이 $TrafficManagerProfile 변수에 로컬로 프로필을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="73397-114">The command stores the profile locally in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="73397-115">두 번째 명령은 해당 프로필을 로컬로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="73397-115">The second command changes that profile locally.</span></span>
<span data-ttu-id="73397-116">이 명령은 프로필을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73397-116">This command disables the profile.</span></span>

<span data-ttu-id="73397-117">세 번째 명령은 $TrafficManagerProfile의 로컬 값과 일치 하도록 ContosoProfile 이라는 Traffic Manager 프로필을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="73397-117">The third command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="73397-118">변수</span><span class="sxs-lookup"><span data-stu-id="73397-118">PARAMETERS</span></span>

### <span data-ttu-id="73397-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73397-119">-DefaultProfile</span></span>
<span data-ttu-id="73397-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="73397-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73397-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="73397-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="73397-122">로컬 **TrafficManagerProfile** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73397-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="73397-123">이 cmdlet은이 로컬 개체와 일치 하도록 Traffic Manager를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="73397-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="73397-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73397-124">CommonParameters</span></span>
<span data-ttu-id="73397-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="73397-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73397-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73397-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73397-127">입력</span><span class="sxs-lookup"><span data-stu-id="73397-127">INPUTS</span></span>

### <span data-ttu-id="73397-128">TrafficManager. TrafficManagerProfile/.</span><span class="sxs-lookup"><span data-stu-id="73397-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="73397-129">출력</span><span class="sxs-lookup"><span data-stu-id="73397-129">OUTPUTS</span></span>

### <span data-ttu-id="73397-130">TrafficManager. TrafficManagerProfile/.</span><span class="sxs-lookup"><span data-stu-id="73397-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="73397-131">상속자</span><span class="sxs-lookup"><span data-stu-id="73397-131">NOTES</span></span>

## <span data-ttu-id="73397-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="73397-132">RELATED LINKS</span></span>

[<span data-ttu-id="73397-133">추가-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="73397-133">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="73397-134">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="73397-134">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="73397-135">새로운 AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="73397-135">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="73397-136">제거-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="73397-136">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="73397-137">제거-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="73397-137">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)


