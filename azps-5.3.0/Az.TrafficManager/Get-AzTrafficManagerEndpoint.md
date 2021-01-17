---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 4556C345-55D0-431C-B980-219D5ED14E5F
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/get-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 3a24063e7b3d74704aa8d409b5bec6d87e35d095
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382873"
---
# <span data-ttu-id="29da3-101">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="29da3-101">Get-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="29da3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29da3-102">SYNOPSIS</span></span>
<span data-ttu-id="29da3-103">Traffic Manager 프로필에 대한 엔드포인트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="29da3-103">Gets an endpoint for a Traffic Manager profile.</span></span>

## <span data-ttu-id="29da3-104">구문</span><span class="sxs-lookup"><span data-stu-id="29da3-104">SYNTAX</span></span>

### <span data-ttu-id="29da3-105">필드</span><span class="sxs-lookup"><span data-stu-id="29da3-105">Fields</span></span>
```
Get-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29da3-106">개체</span><span class="sxs-lookup"><span data-stu-id="29da3-106">Object</span></span>
```
Get-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29da3-107">설명</span><span class="sxs-lookup"><span data-stu-id="29da3-107">DESCRIPTION</span></span>
<span data-ttu-id="29da3-108">**Get-AzTrafficManagerEndpoint** cmdlet은 Azure Traffic Manager 프로필에 대한 엔드포인트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="29da3-108">The **Get-AzTrafficManagerEndpoint** cmdlet gets an endpoint for an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="29da3-109">이 개체를 로컬로 수정한 다음, Set-AzTrafficManagerEndpoint cmdlet을 사용하여 프로필에 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="29da3-109">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="29da3-110">이름 및 형식 매개 변수를 사용하여 *엔드포인트를* *지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="29da3-110">Specify the endpoint by using the *Name* and *Type* parameters.</span></span>
<span data-ttu-id="29da3-111">*ProfileName* 및 *ResourceGroupName* 매개 변수를 사용하거나 **TrafficManagerProfile** 개체를 지정하여 Traffic Manager 프로필을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="29da3-111">You can specify the Traffic Manager profile either by using the *ProfileName* and *ResourceGroupName* parameter, or by specifying a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="29da3-112">또는 파이프라인을 사용하여 해당 값을 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="29da3-112">Alternatively, you can pass that value by using the pipeline.</span></span>

## <span data-ttu-id="29da3-113">예제</span><span class="sxs-lookup"><span data-stu-id="29da3-113">EXAMPLES</span></span>

### <span data-ttu-id="29da3-114">예제 1: 엔드포인트를 얻게</span><span class="sxs-lookup"><span data-stu-id="29da3-114">Example 1: Get an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="29da3-115">이 명령은 ResourceGroup11이라는 리소스 그룹의 ContosoProfile 프로필에서 contoso라는 Azure 엔드포인트를 구한 다음 해당 개체를 $TrafficManagerEndpoint 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="29da3-115">This command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>

## <span data-ttu-id="29da3-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29da3-116">PARAMETERS</span></span>

### <span data-ttu-id="29da3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29da3-117">-DefaultProfile</span></span>
<span data-ttu-id="29da3-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="29da3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29da3-119">-Name</span><span class="sxs-lookup"><span data-stu-id="29da3-119">-Name</span></span>
<span data-ttu-id="29da3-120">이 cmdlet에서 얻을 Traffic Manager 엔드포인트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="29da3-120">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="29da3-121">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="29da3-121">-ProfileName</span></span>
<span data-ttu-id="29da3-122">이 cmdlet에서 얻을 Traffic Manager 엔드포인트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="29da3-122">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="29da3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29da3-123">-ResourceGroupName</span></span>
<span data-ttu-id="29da3-124">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="29da3-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="29da3-125">이 cmdlet은 이 매개 변수가 지정하는 그룹의 Traffic Manager 엔드포인트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="29da3-125">This cmdlet gets a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="29da3-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="29da3-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="29da3-127">이 cmdlet이 얻을 Traffic Manager 엔드포인트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="29da3-127">Specifies the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="29da3-128">-Type</span><span class="sxs-lookup"><span data-stu-id="29da3-128">-Type</span></span>
<span data-ttu-id="29da3-129">이 cmdlet이 Traffic Manager 프로필에 추가하는 엔드포인트의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="29da3-129">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="29da3-130">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="29da3-130">Valid values are:</span></span> 

- <span data-ttu-id="29da3-131">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="29da3-131">AzureEndpoints</span></span>
- <span data-ttu-id="29da3-132">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="29da3-132">ExternalEndpoints</span></span>
- <span data-ttu-id="29da3-133">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="29da3-133">NestedEndpoints</span></span>

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

### <span data-ttu-id="29da3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29da3-134">CommonParameters</span></span>
<span data-ttu-id="29da3-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="29da3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29da3-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="29da3-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29da3-137">입력</span><span class="sxs-lookup"><span data-stu-id="29da3-137">INPUTS</span></span>

### <span data-ttu-id="29da3-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="29da3-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="29da3-139">출력</span><span class="sxs-lookup"><span data-stu-id="29da3-139">OUTPUTS</span></span>

### <span data-ttu-id="29da3-140">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="29da3-140">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="29da3-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="29da3-141">NOTES</span></span>

## <span data-ttu-id="29da3-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="29da3-142">RELATED LINKS</span></span>

[<span data-ttu-id="29da3-143">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="29da3-143">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="29da3-144">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="29da3-144">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="29da3-145">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="29da3-145">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="29da3-146">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="29da3-146">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="29da3-147">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="29da3-147">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)


