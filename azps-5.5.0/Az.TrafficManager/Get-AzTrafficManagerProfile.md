---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/get-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
ms.openlocfilehash: c79eb6b5a8883f6b3a9ede2316f47c98fd9b389c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198249"
---
# <span data-ttu-id="591aa-101">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="591aa-101">Get-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="591aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="591aa-102">SYNOPSIS</span></span>
<span data-ttu-id="591aa-103">Traffic Manager 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="591aa-103">Gets a Traffic Manager profile.</span></span>

## <span data-ttu-id="591aa-104">구문</span><span class="sxs-lookup"><span data-stu-id="591aa-104">SYNTAX</span></span>

### <span data-ttu-id="591aa-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="591aa-105">ResourceGroupParameterSet</span></span>
```
Get-AzTrafficManagerProfile [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="591aa-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="591aa-106">AccountNameParameterSet</span></span>
```
Get-AzTrafficManagerProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="591aa-107">설명</span><span class="sxs-lookup"><span data-stu-id="591aa-107">DESCRIPTION</span></span>
<span data-ttu-id="591aa-108">**Get-AzTrafficManagerProfile** cmdlet은 Azure Traffic Manager 프로필을 얻게 하여 해당 프로필을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="591aa-108">The **Get-AzTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="591aa-109">이름 및 리소스 그룹 이름으로 프로필을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="591aa-109">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="591aa-110">이 개체를 로컬로 수정한 다음, Set-AzTrafficManagerProfile cmdlet을 사용하여 프로필에 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="591aa-110">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="591aa-111">예제</span><span class="sxs-lookup"><span data-stu-id="591aa-111">EXAMPLES</span></span>

### <span data-ttu-id="591aa-112">예제 1: 프로필을 하세요.</span><span class="sxs-lookup"><span data-stu-id="591aa-112">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="591aa-113">이 명령은 ResourceGroup11에서 ContosoProfile이라는 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="591aa-113">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="591aa-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="591aa-114">PARAMETERS</span></span>

### <span data-ttu-id="591aa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="591aa-115">-DefaultProfile</span></span>
<span data-ttu-id="591aa-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="591aa-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="591aa-117">-Name</span><span class="sxs-lookup"><span data-stu-id="591aa-117">-Name</span></span>
<span data-ttu-id="591aa-118">이 cmdlet이 얻을 Traffic Manager 프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="591aa-118">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="591aa-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="591aa-119">-ResourceGroupName</span></span>
<span data-ttu-id="591aa-120">이 cmdlet에서 얻을 Traffic Manager 프로필을 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="591aa-120">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="591aa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="591aa-121">CommonParameters</span></span>
<span data-ttu-id="591aa-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="591aa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="591aa-123">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="591aa-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="591aa-124">입력</span><span class="sxs-lookup"><span data-stu-id="591aa-124">INPUTS</span></span>

### <span data-ttu-id="591aa-125">System.String</span><span class="sxs-lookup"><span data-stu-id="591aa-125">System.String</span></span>

## <span data-ttu-id="591aa-126">출력</span><span class="sxs-lookup"><span data-stu-id="591aa-126">OUTPUTS</span></span>

### <span data-ttu-id="591aa-127">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="591aa-127">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="591aa-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="591aa-128">NOTES</span></span>

## <span data-ttu-id="591aa-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="591aa-129">RELATED LINKS</span></span>

[<span data-ttu-id="591aa-130">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="591aa-130">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="591aa-131">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="591aa-131">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="591aa-132">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="591aa-132">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="591aa-133">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="591aa-133">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="591aa-134">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="591aa-134">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


