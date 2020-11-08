---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 4556C345-55D0-431C-B980-219D5ED14E5F
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/get-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 3a24063e7b3d74704aa8d409b5bec6d87e35d095
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041639"
---
# <span data-ttu-id="d92c5-101">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d92c5-101">Get-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="d92c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d92c5-102">SYNOPSIS</span></span>
<span data-ttu-id="d92c5-103">Traffic Manager 프로필에 대 한 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d92c5-103">Gets an endpoint for a Traffic Manager profile.</span></span>

## <span data-ttu-id="d92c5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d92c5-104">SYNTAX</span></span>

### <span data-ttu-id="d92c5-105">필드인</span><span class="sxs-lookup"><span data-stu-id="d92c5-105">Fields</span></span>
```
Get-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d92c5-106">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="d92c5-106">Object</span></span>
```
Get-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d92c5-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d92c5-107">DESCRIPTION</span></span>
<span data-ttu-id="d92c5-108">**AzTrafficManagerEndpoint** Cmdlet은 Azure Traffic Manager 프로필에 대 한 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d92c5-108">The **Get-AzTrafficManagerEndpoint** cmdlet gets an endpoint for an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="d92c5-109">이 개체를 로컬로 수정한 다음 Set-AzTrafficManagerEndpoint cmdlet을 사용 하 여 프로필에 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d92c5-109">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="d92c5-110">*Name* 및 *Type* 매개 변수를 사용 하 여 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d92c5-110">Specify the endpoint by using the *Name* and *Type* parameters.</span></span>
<span data-ttu-id="d92c5-111">*/Profile* 및 *ResourceGroupName* 매개 변수를 사용 하거나 **TrafficManagerProfile** 개체를 지정 하 여 Traffic Manager 프로필을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d92c5-111">You can specify the Traffic Manager profile either by using the *ProfileName* and *ResourceGroupName* parameter, or by specifying a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="d92c5-112">또는 파이프라인을 사용 하 여 해당 값을 전달할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d92c5-112">Alternatively, you can pass that value by using the pipeline.</span></span>

## <span data-ttu-id="d92c5-113">예제의</span><span class="sxs-lookup"><span data-stu-id="d92c5-113">EXAMPLES</span></span>

### <span data-ttu-id="d92c5-114">예제 1: 끝점 가져오기</span><span class="sxs-lookup"><span data-stu-id="d92c5-114">Example 1: Get an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="d92c5-115">이 명령은 ResourceGroup11 이라는 리소스 그룹에 있는 ContosoProfile 이라는 프로필에서 contoso 라는 Azure 끝점을 가져온 다음 해당 개체를 $TrafficManagerEndpoint 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d92c5-115">This command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>

## <span data-ttu-id="d92c5-116">변수</span><span class="sxs-lookup"><span data-stu-id="d92c5-116">PARAMETERS</span></span>

### <span data-ttu-id="d92c5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d92c5-117">-DefaultProfile</span></span>
<span data-ttu-id="d92c5-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d92c5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d92c5-119">-이름</span><span class="sxs-lookup"><span data-stu-id="d92c5-119">-Name</span></span>
<span data-ttu-id="d92c5-120">이 cmdlet이 가져오는 Traffic Manager 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d92c5-120">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d92c5-121">-/Profile</span><span class="sxs-lookup"><span data-stu-id="d92c5-121">-ProfileName</span></span>
<span data-ttu-id="d92c5-122">이 cmdlet이 가져오는 Traffic Manager 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d92c5-122">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d92c5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d92c5-123">-ResourceGroupName</span></span>
<span data-ttu-id="d92c5-124">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d92c5-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="d92c5-125">이 cmdlet은이 매개 변수에서 지정 하는 그룹의 Traffic Manager 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d92c5-125">This cmdlet gets a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d92c5-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d92c5-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="d92c5-127">이 cmdlet이 가져오는 트래픽 관리자 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d92c5-127">Specifies the Traffic Manager endpoint that this cmdlet gets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d92c5-128">-Type</span><span class="sxs-lookup"><span data-stu-id="d92c5-128">-Type</span></span>
<span data-ttu-id="d92c5-129">이 cmdlet이 Traffic Manager 프로필에 추가 하는 끝점 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d92c5-129">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="d92c5-130">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d92c5-130">Valid values are:</span></span> 

- <span data-ttu-id="d92c5-131">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="d92c5-131">AzureEndpoints</span></span>
- <span data-ttu-id="d92c5-132">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="d92c5-132">ExternalEndpoints</span></span>
- <span data-ttu-id="d92c5-133">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="d92c5-133">NestedEndpoints</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d92c5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d92c5-134">CommonParameters</span></span>
<span data-ttu-id="d92c5-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d92c5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d92c5-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d92c5-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d92c5-137">입력</span><span class="sxs-lookup"><span data-stu-id="d92c5-137">INPUTS</span></span>

### <span data-ttu-id="d92c5-138">TrafficManager. TrafficManagerEndpoint/.</span><span class="sxs-lookup"><span data-stu-id="d92c5-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="d92c5-139">출력</span><span class="sxs-lookup"><span data-stu-id="d92c5-139">OUTPUTS</span></span>

### <span data-ttu-id="d92c5-140">TrafficManager. TrafficManagerEndpoint/.</span><span class="sxs-lookup"><span data-stu-id="d92c5-140">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="d92c5-141">상속자</span><span class="sxs-lookup"><span data-stu-id="d92c5-141">NOTES</span></span>

## <span data-ttu-id="d92c5-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d92c5-142">RELATED LINKS</span></span>

[<span data-ttu-id="d92c5-143">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d92c5-143">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="d92c5-144">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d92c5-144">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="d92c5-145">새로운 AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d92c5-145">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="d92c5-146">제거-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d92c5-146">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="d92c5-147">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d92c5-147">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)


