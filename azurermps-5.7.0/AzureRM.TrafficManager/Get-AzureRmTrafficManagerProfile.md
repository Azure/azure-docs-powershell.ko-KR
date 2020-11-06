---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/get-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: bdfe37622db49c554f128714ab2af65a11fbfce7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532575"
---
# <span data-ttu-id="3f999-101">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3f999-101">Get-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="3f999-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f999-102">SYNOPSIS</span></span>
<span data-ttu-id="3f999-103">Traffic Manager 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3f999-103">Gets a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f999-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3f999-104">SYNTAX</span></span>

```
Get-AzureRmTrafficManagerProfile [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f999-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3f999-105">DESCRIPTION</span></span>
<span data-ttu-id="3f999-106">**AzureRmTrafficManagerProfile** Cmdlet은 Azure Traffic Manager 프로필을 가져오고 해당 프로필을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f999-106">The **Get-AzureRmTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="3f999-107">프로필 이름 및 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f999-107">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="3f999-108">이 개체를 로컬로 수정한 다음 Set-AzureRmTrafficManagerProfile cmdlet을 사용 하 여 프로필에 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3f999-108">You can modify this object locally, and then apply changes to the profile by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="3f999-109">예제의</span><span class="sxs-lookup"><span data-stu-id="3f999-109">EXAMPLES</span></span>

### <span data-ttu-id="3f999-110">예제 1: 프로필 가져오기</span><span class="sxs-lookup"><span data-stu-id="3f999-110">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="3f999-111">이 명령은 ResourceGroup11에서 ContosoProfile 이라는 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3f999-111">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="3f999-112">변수</span><span class="sxs-lookup"><span data-stu-id="3f999-112">PARAMETERS</span></span>

### <span data-ttu-id="3f999-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f999-113">-DefaultProfile</span></span>
<span data-ttu-id="3f999-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3f999-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f999-115">-이름</span><span class="sxs-lookup"><span data-stu-id="3f999-115">-Name</span></span>
<span data-ttu-id="3f999-116">이 cmdlet이 가져오는 Traffic Manager 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f999-116">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f999-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f999-117">-ResourceGroupName</span></span>
<span data-ttu-id="3f999-118">이 cmdlet이 가져오는 Traffic Manager 프로필을 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f999-118">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f999-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f999-119">CommonParameters</span></span>
<span data-ttu-id="3f999-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f999-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f999-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f999-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f999-122">입력</span><span class="sxs-lookup"><span data-stu-id="3f999-122">INPUTS</span></span>

### <span data-ttu-id="3f999-123">않아야</span><span class="sxs-lookup"><span data-stu-id="3f999-123">None</span></span>
<span data-ttu-id="3f999-124">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3f999-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3f999-125">출력</span><span class="sxs-lookup"><span data-stu-id="3f999-125">OUTPUTS</span></span>

### <span data-ttu-id="3f999-126">TrafficManagerProfile (Network.)</span><span class="sxs-lookup"><span data-stu-id="3f999-126">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="3f999-127">이 cmdlet은 **TrafficManagerProfile** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f999-127">This cmdlet returns a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="3f999-128">이 개체를 수정한 다음 **Set-AzureRmTrafficManagerProfile** 를 사용 하 여 트래픽 관리자에 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3f999-128">You can modify this object, and then apply changes to Traffic Manager by using **Set-AzureRmTrafficManagerProfile**.</span></span>

## <span data-ttu-id="3f999-129">상속자</span><span class="sxs-lookup"><span data-stu-id="3f999-129">NOTES</span></span>

## <span data-ttu-id="3f999-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3f999-130">RELATED LINKS</span></span>

[<span data-ttu-id="3f999-131">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3f999-131">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="3f999-132">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3f999-132">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="3f999-133">새로운 AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3f999-133">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="3f999-134">제거-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3f999-134">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="3f999-135">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3f999-135">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


