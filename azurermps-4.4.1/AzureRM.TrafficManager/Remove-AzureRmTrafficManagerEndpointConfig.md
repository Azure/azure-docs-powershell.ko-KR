---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpointConfig.md
ms.openlocfilehash: 4f936569b5a3c7b3ba63a471aedd6828ef6f36d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702050"
---
# <span data-ttu-id="0cf0e-101">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="0cf0e-101">Remove-AzureRmTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="0cf0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0cf0e-102">SYNOPSIS</span></span>
<span data-ttu-id="0cf0e-103">로컬 트래픽 관리자 프로필 개체에서 끝점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-103">Removes an endpoint from a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0cf0e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0cf0e-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerEndpointConfig -EndpointName <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cf0e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0cf0e-105">DESCRIPTION</span></span>
<span data-ttu-id="0cf0e-106">**AzureRmTrafficManagerEndpointConfig** cmdlet은 로컬 Azure Traffic Manager 프로필 개체에서 끝점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-106">The **Remove-AzureRmTrafficManagerEndpointConfig** cmdlet removes an endpoint from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="0cf0e-107">Get-AzureRmTrafficManagerProfile cmdlet을 사용 하 여 프로필을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-107">You can get a profile by using the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

<span data-ttu-id="0cf0e-108">이 cmdlet은 로컬 프로필 개체에서 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="0cf0e-109">Set-AzureRmTrafficManagerProfile cmdlet을 사용 하 여 트래픽 관리자의 프로필에 대 한 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="0cf0e-110">한 번의 작업으로 끝점을 제거 하 고 변경 내용을 커밋하려면 Remove-AzureRmTrafficManagerEndpoint cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-110">To remove an endpoint and commit changes in a single operation, use the Remove-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="0cf0e-111">예제의</span><span class="sxs-lookup"><span data-stu-id="0cf0e-111">EXAMPLES</span></span>

### <span data-ttu-id="0cf0e-112">예제 1: 끝점 제거</span><span class="sxs-lookup"><span data-stu-id="0cf0e-112">Example 1: Remove an endpoint</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzureRmTrafficManagerEndpointConfig -EndpointName "contoso" -Type AzureEndpoints -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="0cf0e-113">첫 번째 명령은 **AzureRmTrafficManagerProfile** cmdlet을 사용 하 여 Azure Traffic Manager 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="0cf0e-114">명령은 로컬 프로필을 $TrafficManagerProfile 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="0cf0e-115">두 번째 명령은 $TrafficManagerProfile에 저장 된 프로필에서 contoso 라는 Azure 끝점을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-115">The second command removes an Azure endpoint named contoso from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="0cf0e-116">이 명령은 로컬 개체만 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-116">This command changes only the local object.</span></span>

<span data-ttu-id="0cf0e-117">마지막 명령은 $TrafficManagerProfile의 로컬 값과 일치 하도록 ContosoProfile 이라는 Traffic Manager 프로필을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-117">The final command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="0cf0e-118">변수</span><span class="sxs-lookup"><span data-stu-id="0cf0e-118">PARAMETERS</span></span>

### <span data-ttu-id="0cf0e-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="0cf0e-119">-EndpointName</span></span>
<span data-ttu-id="0cf0e-120">이 cmdlet이 제거 하는 Traffic Manager 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-120">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0cf0e-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0cf0e-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="0cf0e-122">로컬 **TrafficManagerProfile** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="0cf0e-123">이 cmdlet은이 로컬 개체를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="0cf0e-124">**TrafficManagerProfile** 개체를 가져오려면 Get-AzureRmTrafficManagerProfile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-124">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="0cf0e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cf0e-125">-DefaultProfile</span></span>
<span data-ttu-id="0cf0e-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0cf0e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cf0e-127">CommonParameters</span></span>
<span data-ttu-id="0cf0e-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cf0e-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cf0e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cf0e-130">입력</span><span class="sxs-lookup"><span data-stu-id="0cf0e-130">INPUTS</span></span>

### <span data-ttu-id="0cf0e-131">TrafficManagerProfile (Network.)</span><span class="sxs-lookup"><span data-stu-id="0cf0e-131">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="0cf0e-132">이 cmdlet은이 cmdlet에 대 한 **TrafficManagerProfile** 개체를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-132">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="0cf0e-133">출력</span><span class="sxs-lookup"><span data-stu-id="0cf0e-133">OUTPUTS</span></span>

### <span data-ttu-id="0cf0e-134">TrafficManagerProfile (Network.)</span><span class="sxs-lookup"><span data-stu-id="0cf0e-134">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="0cf0e-135">이 cmdlet은 수정 된 TrafficManagerProfile 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cf0e-135">This cmdlet returns a modified TrafficManagerProfile object.</span></span>

## <span data-ttu-id="0cf0e-136">상속자</span><span class="sxs-lookup"><span data-stu-id="0cf0e-136">NOTES</span></span>

## <span data-ttu-id="0cf0e-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0cf0e-137">RELATED LINKS</span></span>

[<span data-ttu-id="0cf0e-138">추가-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="0cf0e-138">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="0cf0e-139">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0cf0e-139">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="0cf0e-140">제거-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0cf0e-140">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="0cf0e-141">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0cf0e-141">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


