---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5032D487-3849-4C80-BD14-5B735FC39285
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/get-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerProfile.md
ms.openlocfilehash: c79eb6b5a8883f6b3a9ede2316f47c98fd9b389c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041682"
---
# <span data-ttu-id="08565-101">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="08565-101">Get-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="08565-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08565-102">SYNOPSIS</span></span>
<span data-ttu-id="08565-103">Traffic Manager 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="08565-103">Gets a Traffic Manager profile.</span></span>

## <span data-ttu-id="08565-104">구문과</span><span class="sxs-lookup"><span data-stu-id="08565-104">SYNTAX</span></span>

### <span data-ttu-id="08565-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="08565-105">ResourceGroupParameterSet</span></span>
```
Get-AzTrafficManagerProfile [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="08565-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="08565-106">AccountNameParameterSet</span></span>
```
Get-AzTrafficManagerProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08565-107">설명은</span><span class="sxs-lookup"><span data-stu-id="08565-107">DESCRIPTION</span></span>
<span data-ttu-id="08565-108">**AzTrafficManagerProfile** Cmdlet은 Azure Traffic Manager 프로필을 가져오고 해당 프로필을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="08565-108">The **Get-AzTrafficManagerProfile** cmdlet gets an Azure Traffic Manager profile, and returns an object that represents that profile.</span></span>
<span data-ttu-id="08565-109">프로필 이름 및 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="08565-109">Specify a profile by its name and resource group name.</span></span>

<span data-ttu-id="08565-110">이 개체를 로컬로 수정한 다음 Set-AzTrafficManagerProfile cmdlet을 사용 하 여 프로필에 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="08565-110">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="08565-111">예제의</span><span class="sxs-lookup"><span data-stu-id="08565-111">EXAMPLES</span></span>

### <span data-ttu-id="08565-112">예제 1: 프로필 가져오기</span><span class="sxs-lookup"><span data-stu-id="08565-112">Example 1: Get a profile</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="08565-113">이 명령은 ResourceGroup11에서 ContosoProfile 이라는 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="08565-113">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>

## <span data-ttu-id="08565-114">변수</span><span class="sxs-lookup"><span data-stu-id="08565-114">PARAMETERS</span></span>

### <span data-ttu-id="08565-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08565-115">-DefaultProfile</span></span>
<span data-ttu-id="08565-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="08565-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08565-117">-이름</span><span class="sxs-lookup"><span data-stu-id="08565-117">-Name</span></span>
<span data-ttu-id="08565-118">이 cmdlet이 가져오는 Traffic Manager 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="08565-118">Specifies the name of the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="08565-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08565-119">-ResourceGroupName</span></span>
<span data-ttu-id="08565-120">이 cmdlet이 가져오는 Traffic Manager 프로필을 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="08565-120">Specifies the name of a resource group that contains the Traffic Manager profile that this cmdlet gets.</span></span>

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

### <span data-ttu-id="08565-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08565-121">CommonParameters</span></span>
<span data-ttu-id="08565-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="08565-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08565-123">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08565-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08565-124">입력</span><span class="sxs-lookup"><span data-stu-id="08565-124">INPUTS</span></span>

### <span data-ttu-id="08565-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="08565-125">System.String</span></span>

## <span data-ttu-id="08565-126">출력</span><span class="sxs-lookup"><span data-stu-id="08565-126">OUTPUTS</span></span>

### <span data-ttu-id="08565-127">TrafficManager. TrafficManagerProfile/.</span><span class="sxs-lookup"><span data-stu-id="08565-127">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="08565-128">상속자</span><span class="sxs-lookup"><span data-stu-id="08565-128">NOTES</span></span>

## <span data-ttu-id="08565-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="08565-129">RELATED LINKS</span></span>

[<span data-ttu-id="08565-130">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="08565-130">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="08565-131">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="08565-131">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="08565-132">새로운 AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="08565-132">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="08565-133">제거-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="08565-133">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="08565-134">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="08565-134">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


