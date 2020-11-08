---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
ms.openlocfilehash: ba578d800631304405ab1e0a4139a11d9f2a26dc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225986"
---
# <span data-ttu-id="2e328-101">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2e328-101">Enable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="2e328-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e328-102">SYNOPSIS</span></span>
<span data-ttu-id="2e328-103">Traffic Manager 프로필을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e328-103">Enables a Traffic Manager profile.</span></span>

## <span data-ttu-id="2e328-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2e328-104">SYNTAX</span></span>

### <span data-ttu-id="2e328-105">필드인</span><span class="sxs-lookup"><span data-stu-id="2e328-105">Fields</span></span>
```
Enable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e328-106">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="2e328-106">Object</span></span>
```
Enable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e328-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2e328-107">DESCRIPTION</span></span>
<span data-ttu-id="2e328-108">AzTrafficManagerProfile cmdlet을 **사용** 하면 Azure Traffic Manager 프로필을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e328-108">The **Enable-AzTrafficManagerProfile** cmdlet enables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="2e328-109">파이프라인 또는 매개 변수 값을 사용 하 여 프로필 개체를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e328-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="2e328-110">또는 *Name* 및 *ResourceGroupName* 매개 변수를 사용 하 여 프로필을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e328-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="2e328-111">예제의</span><span class="sxs-lookup"><span data-stu-id="2e328-111">EXAMPLES</span></span>

### <span data-ttu-id="2e328-112">예제 1: 이름으로 지정 된 프로필 사용</span><span class="sxs-lookup"><span data-stu-id="2e328-112">Example 1: Enable a profile specified by name</span></span>
```
PS C:\>Enable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="2e328-113">이 명령은 ResourceGroup11에서 ContosoProfile 이라는 프로필을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e328-113">This command enables the profile named ContosoProfile in ResourceGroup11.</span></span>

### <span data-ttu-id="2e328-114">예제 2: 파이프라인을 사용 하 여 프로필 설정</span><span class="sxs-lookup"><span data-stu-id="2e328-114">Example 2: Enable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerProfile
```

<span data-ttu-id="2e328-115">이 명령은 ResourceGroup11에서 ContosoProfile 이라는 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2e328-115">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="2e328-116">그런 다음이 명령은 파이프라인 연산자를 사용 하 여 해당 프로필을 **AzTrafficManagerProfile** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e328-116">The command then passes that profile to the **Enable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2e328-117">해당 cmdlet은 해당 프로필을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e328-117">That cmdlet enables that profile.</span></span>

## <span data-ttu-id="2e328-118">변수</span><span class="sxs-lookup"><span data-stu-id="2e328-118">PARAMETERS</span></span>

### <span data-ttu-id="2e328-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e328-119">-DefaultProfile</span></span>
<span data-ttu-id="2e328-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2e328-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e328-121">-이름</span><span class="sxs-lookup"><span data-stu-id="2e328-121">-Name</span></span>
<span data-ttu-id="2e328-122">이 cmdlet이 사용할 수 있는 Traffic Manager 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e328-122">Specifies the name of the Traffic Manager profile that this cmdlet enables.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e328-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e328-123">-ResourceGroupName</span></span>
<span data-ttu-id="2e328-124">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e328-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="2e328-125">이 cmdlet은이 매개 변수에서 지정 하는 그룹에서 Traffic Manager 프로필을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e328-125">This cmdlet enables a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e328-126">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2e328-126">-TrafficManagerProfile</span></span>
<span data-ttu-id="2e328-127">사용할 **TrafficManagerProfile** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e328-127">Specifies a **TrafficManagerProfile** object to enable.</span></span>
<span data-ttu-id="2e328-128">**TrafficManagerProfile** 개체를 가져오려면 Get-AzTrafficManagerProfile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e328-128">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e328-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e328-129">CommonParameters</span></span>
<span data-ttu-id="2e328-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e328-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e328-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e328-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e328-132">입력</span><span class="sxs-lookup"><span data-stu-id="2e328-132">INPUTS</span></span>

### <span data-ttu-id="2e328-133">TrafficManager. TrafficManagerProfile/.</span><span class="sxs-lookup"><span data-stu-id="2e328-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="2e328-134">출력</span><span class="sxs-lookup"><span data-stu-id="2e328-134">OUTPUTS</span></span>

### <span data-ttu-id="2e328-135">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="2e328-135">System.Boolean</span></span>

## <span data-ttu-id="2e328-136">상속자</span><span class="sxs-lookup"><span data-stu-id="2e328-136">NOTES</span></span>

## <span data-ttu-id="2e328-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2e328-137">RELATED LINKS</span></span>

[<span data-ttu-id="2e328-138">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2e328-138">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="2e328-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2e328-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="2e328-140">새로운 AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2e328-140">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="2e328-141">제거-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2e328-141">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="2e328-142">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2e328-142">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


