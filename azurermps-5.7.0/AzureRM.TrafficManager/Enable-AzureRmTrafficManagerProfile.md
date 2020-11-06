---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/enable-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 252a633112c28b1dc1e62a6004e3f67e2b6a343a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532572"
---
# <span data-ttu-id="1d7d4-101">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1d7d4-101">Enable-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="1d7d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d7d4-102">SYNOPSIS</span></span>
<span data-ttu-id="1d7d4-103">Traffic Manager 프로필을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d7d4-103">Enables a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d7d4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1d7d4-104">SYNTAX</span></span>

### <span data-ttu-id="1d7d4-105">필드인</span><span class="sxs-lookup"><span data-stu-id="1d7d4-105">Fields</span></span>
```
Enable-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d7d4-106">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="1d7d4-106">Object</span></span>
```
Enable-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d7d4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1d7d4-107">DESCRIPTION</span></span>
<span data-ttu-id="1d7d4-108">AzureRmTrafficManagerProfile cmdlet을 **사용** 하면 Azure Traffic Manager 프로필을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d7d4-108">The **Enable-AzureRmTrafficManagerProfile** cmdlet enables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="1d7d4-109">파이프라인 또는 매개 변수 값을 사용 하 여 프로필 개체를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d7d4-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="1d7d4-110">또는 *Name* 및 *ResourceGroupName* 매개 변수를 사용 하 여 프로필을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d7d4-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="1d7d4-111">예제의</span><span class="sxs-lookup"><span data-stu-id="1d7d4-111">EXAMPLES</span></span>

### <span data-ttu-id="1d7d4-112">예제 1: 이름으로 지정 된 프로필 사용</span><span class="sxs-lookup"><span data-stu-id="1d7d4-112">Example 1: Enable a profile specified by name</span></span>
```
PS C:\>Enable-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="1d7d4-113">이 명령은 ResourceGroup11에서 ContosoProfile 이라는 프로필을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d7d4-113">This command enables the profile named ContosoProfile in ResourceGroup11.</span></span>

### <span data-ttu-id="1d7d4-114">예제 2: 파이프라인을 사용 하 여 프로필 설정</span><span class="sxs-lookup"><span data-stu-id="1d7d4-114">Example 2: Enable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzureRmTrafficManagerProfile
```

<span data-ttu-id="1d7d4-115">이 명령은 ResourceGroup11에서 ContosoProfile 이라는 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1d7d4-115">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="1d7d4-116">그런 다음이 명령은 파이프라인 연산자를 사용 하 여 해당 프로필을 **AzureRmTrafficManagerProfile** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d7d4-116">The command then passes that profile to the **Enable-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1d7d4-117">해당 cmdlet은 해당 프로필을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d7d4-117">That cmdlet enables that profile.</span></span>

## <span data-ttu-id="1d7d4-118">변수</span><span class="sxs-lookup"><span data-stu-id="1d7d4-118">PARAMETERS</span></span>

### <span data-ttu-id="1d7d4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d7d4-119">-DefaultProfile</span></span>
<span data-ttu-id="1d7d4-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1d7d4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d7d4-121">-이름</span><span class="sxs-lookup"><span data-stu-id="1d7d4-121">-Name</span></span>
<span data-ttu-id="1d7d4-122">이 cmdlet이 사용할 수 있는 Traffic Manager 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d7d4-122">Specifies the name of the Traffic Manager profile that this cmdlet enables.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d7d4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d7d4-123">-ResourceGroupName</span></span>
<span data-ttu-id="1d7d4-124">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d7d4-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="1d7d4-125">이 cmdlet은이 매개 변수에서 지정 하는 그룹에서 Traffic Manager 프로필을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d7d4-125">This cmdlet enables a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d7d4-126">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1d7d4-126">-TrafficManagerProfile</span></span>
<span data-ttu-id="1d7d4-127">사용할 **TrafficManagerProfile** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d7d4-127">Specifies a **TrafficManagerProfile** object to enable.</span></span>
<span data-ttu-id="1d7d4-128">**TrafficManagerProfile** 개체를 가져오려면 Get-AzureRmTrafficManagerProfile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d7d4-128">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: TrafficManagerProfile
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d7d4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d7d4-129">CommonParameters</span></span>
<span data-ttu-id="1d7d4-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d7d4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d7d4-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d7d4-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d7d4-132">입력</span><span class="sxs-lookup"><span data-stu-id="1d7d4-132">INPUTS</span></span>

### <span data-ttu-id="1d7d4-133">TrafficManagerProfile (Network.)</span><span class="sxs-lookup"><span data-stu-id="1d7d4-133">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="1d7d4-134">이 cmdlet은 **TrafficManagerProfile** 개체를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d7d4-134">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="1d7d4-135">출력</span><span class="sxs-lookup"><span data-stu-id="1d7d4-135">OUTPUTS</span></span>

### <span data-ttu-id="1d7d4-136">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="1d7d4-136">System.Boolean</span></span>

## <span data-ttu-id="1d7d4-137">상속자</span><span class="sxs-lookup"><span data-stu-id="1d7d4-137">NOTES</span></span>

## <span data-ttu-id="1d7d4-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1d7d4-138">RELATED LINKS</span></span>

[<span data-ttu-id="1d7d4-139">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1d7d4-139">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="1d7d4-140">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1d7d4-140">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="1d7d4-141">새로운 AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1d7d4-141">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="1d7d4-142">제거-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1d7d4-142">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="1d7d4-143">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1d7d4-143">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


