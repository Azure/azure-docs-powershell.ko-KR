---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/get-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
ms.openlocfilehash: 3d843729a9ab51e5a4e1ecf1952f778537e8bf11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987303"
---
# <span data-ttu-id="c6736-101">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c6736-101">Get-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="c6736-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6736-102">SYNOPSIS</span></span>
<span data-ttu-id="c6736-103">Traffic Manager 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c6736-103">Gets a Traffic Manager profile.</span></span>

## <span data-ttu-id="c6736-104">구문</span><span class="sxs-lookup"><span data-stu-id="c6736-104">SYNTAX</span></span>

### <span data-ttu-id="c6736-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6736-105">ResourceGroupParameterSet</span></span>
```
Get-AzTrafficManagerProfile [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c6736-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6736-106">AccountNameParameterSet</span></span>
```
Get-AzTrafficManagerProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6736-107">설명</span><span class="sxs-lookup"><span data-stu-id="c6736-107">DESCRIPTION</span></span>
<span data-ttu-id="c6736-108">**Get-AzTrafficManagerProfile** cmdlet은 Azure Traffic Manager 프로필을 얻게 하여 해당 프로필을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c6736-108">The **Get-AzTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="c6736-109">이름 및 리소스 그룹 이름으로 프로필을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c6736-109">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="c6736-110">이 개체를 로컬로 수정한 다음, cmdlet을 사용하여 프로필에 Set-AzTrafficManagerProfile 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6736-110">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="c6736-111">예제</span><span class="sxs-lookup"><span data-stu-id="c6736-111">EXAMPLES</span></span>

### <span data-ttu-id="c6736-112">예제 1: 프로필을 하세요.</span><span class="sxs-lookup"><span data-stu-id="c6736-112">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="c6736-113">이 명령은 ResourceGroup11에서 ContosoProfile이라는 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c6736-113">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="c6736-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c6736-114">PARAMETERS</span></span>

### <span data-ttu-id="c6736-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6736-115">-DefaultProfile</span></span>
<span data-ttu-id="c6736-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c6736-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6736-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c6736-117">-Name</span></span>
<span data-ttu-id="c6736-118">이 cmdlet이 얻을 Traffic Manager 프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c6736-118">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6736-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6736-119">-ResourceGroupName</span></span>
<span data-ttu-id="c6736-120">이 cmdlet에서 얻을 Traffic Manager 프로필을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c6736-120">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6736-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6736-121">CommonParameters</span></span>
<span data-ttu-id="c6736-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c6736-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6736-123">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c6736-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6736-124">입력</span><span class="sxs-lookup"><span data-stu-id="c6736-124">INPUTS</span></span>

### <span data-ttu-id="c6736-125">System.String</span><span class="sxs-lookup"><span data-stu-id="c6736-125">System.String</span></span>

## <span data-ttu-id="c6736-126">출력</span><span class="sxs-lookup"><span data-stu-id="c6736-126">OUTPUTS</span></span>

### <span data-ttu-id="c6736-127">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c6736-127">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="c6736-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c6736-128">NOTES</span></span>

## <span data-ttu-id="c6736-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c6736-129">RELATED LINKS</span></span>

[<span data-ttu-id="c6736-130">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c6736-130">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="c6736-131">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c6736-131">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="c6736-132">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c6736-132">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="c6736-133">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c6736-133">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="c6736-134">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c6736-134">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


