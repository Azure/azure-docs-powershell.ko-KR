---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/set-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 9536e6250f73270c7700a14406cb24b8e8f31189
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525911"
---
# <span data-ttu-id="b65c0-101">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b65c0-101">Set-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="b65c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b65c0-102">SYNOPSIS</span></span>
<span data-ttu-id="b65c0-103">Traffic Manager 프로필을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b65c0-103">Updates a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b65c0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b65c0-104">SYNTAX</span></span>

```
Set-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b65c0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b65c0-105">DESCRIPTION</span></span>
<span data-ttu-id="b65c0-106">**AzureRmTrafficManagerProfile** Cmdlet은 Azure Traffic Manager 프로필을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b65c0-106">The **Set-AzureRmTrafficManagerProfile** cmdlet updates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="b65c0-107">이 cmdlet은 로컬 프로필 개체의 프로필 설정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b65c0-107">This cmdlet updates the settings of the profile from a local profile object.</span></span>
<span data-ttu-id="b65c0-108">*TrafficManagerProfile* 매개 변수를 사용 하거나 파이프라인을 사용 하 여 프로필 개체를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b65c0-108">You can specify the profile object either by using the *TrafficManagerProfile* parameter or by using the pipeline.</span></span>

<span data-ttu-id="b65c0-109">Get-AzureRmTrafficManagerProfile cmdlet을 사용 하 여 프로필을 나타내는 로컬 개체를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b65c0-109">You can obtain a local object that represents a profile by using the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="b65c0-110">개체를 로컬로 수정한 다음 **Set-AzureRmTrafficManagerProfile** 를 사용 하 여 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="b65c0-110">Modify the object locally and then use **Set-AzureRmTrafficManagerProfile** to commit your changes.</span></span>

## <span data-ttu-id="b65c0-111">예제의</span><span class="sxs-lookup"><span data-stu-id="b65c0-111">EXAMPLES</span></span>

### <span data-ttu-id="b65c0-112">예제 1: 프로필 업데이트</span><span class="sxs-lookup"><span data-stu-id="b65c0-112">Example 1: Update a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="b65c0-113">첫 번째 명령은 Get-AzureRmTrafficManagerProfile cmdlet을 사용 하 여 Azure Traffic Manager 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b65c0-113">The first command gets an Azure Traffic Manager profile by using the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="b65c0-114">명령이 $TrafficManagerProfile 변수에 로컬로 프로필을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b65c0-114">The command stores the profile locally in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="b65c0-115">두 번째 명령은 해당 프로필을 로컬로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="b65c0-115">The second command changes that profile locally.</span></span>
<span data-ttu-id="b65c0-116">이 명령은 프로필을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b65c0-116">This command disables the profile.</span></span>

<span data-ttu-id="b65c0-117">세 번째 명령은 $TrafficManagerProfile의 로컬 값과 일치 하도록 ContosoProfile 이라는 Traffic Manager 프로필을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b65c0-117">The third command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="b65c0-118">변수</span><span class="sxs-lookup"><span data-stu-id="b65c0-118">PARAMETERS</span></span>

### <span data-ttu-id="b65c0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b65c0-119">-DefaultProfile</span></span>
<span data-ttu-id="b65c0-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b65c0-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b65c0-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b65c0-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="b65c0-122">로컬 **TrafficManagerProfile** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b65c0-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="b65c0-123">이 cmdlet은이 로컬 개체와 일치 하도록 Traffic Manager를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b65c0-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="b65c0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b65c0-124">CommonParameters</span></span>
<span data-ttu-id="b65c0-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b65c0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b65c0-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b65c0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b65c0-127">입력</span><span class="sxs-lookup"><span data-stu-id="b65c0-127">INPUTS</span></span>

### <span data-ttu-id="b65c0-128">TrafficManagerProfile (Network.)</span><span class="sxs-lookup"><span data-stu-id="b65c0-128">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="b65c0-129">이 cmdlet은 **TrafficManagerProfile** 개체를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b65c0-129">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="b65c0-130">출력</span><span class="sxs-lookup"><span data-stu-id="b65c0-130">OUTPUTS</span></span>

### <span data-ttu-id="b65c0-131">TrafficManagerProfile (Network.)</span><span class="sxs-lookup"><span data-stu-id="b65c0-131">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="b65c0-132">이 cmdlet은 **TrafficManagerProfile** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b65c0-132">This cmdlet returns a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="b65c0-133">상속자</span><span class="sxs-lookup"><span data-stu-id="b65c0-133">NOTES</span></span>

## <span data-ttu-id="b65c0-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b65c0-134">RELATED LINKS</span></span>

[<span data-ttu-id="b65c0-135">추가-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="b65c0-135">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="b65c0-136">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b65c0-136">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="b65c0-137">새로운 AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b65c0-137">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="b65c0-138">제거-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="b65c0-138">Remove-AzureRmTrafficManagerEndpointConfig</span></span>](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="b65c0-139">제거-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b65c0-139">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)


