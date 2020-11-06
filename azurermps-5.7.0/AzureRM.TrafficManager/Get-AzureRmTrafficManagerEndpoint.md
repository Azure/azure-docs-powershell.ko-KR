---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4556C345-55D0-431C-B980-219D5ED14E5F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/get-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 488643c8f977fb59af0f5b73c9388e65b3425c1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532571"
---
# <span data-ttu-id="28f25-101">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="28f25-101">Get-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="28f25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28f25-102">SYNOPSIS</span></span>
<span data-ttu-id="28f25-103">Traffic Manager 프로필에 대 한 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28f25-103">Gets an endpoint for a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28f25-104">구문과</span><span class="sxs-lookup"><span data-stu-id="28f25-104">SYNTAX</span></span>

### <span data-ttu-id="28f25-105">필드인</span><span class="sxs-lookup"><span data-stu-id="28f25-105">Fields</span></span>
```
Get-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28f25-106">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="28f25-106">Object</span></span>
```
Get-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28f25-107">설명은</span><span class="sxs-lookup"><span data-stu-id="28f25-107">DESCRIPTION</span></span>
<span data-ttu-id="28f25-108">**AzureRmTrafficManagerEndpoint** Cmdlet은 Azure Traffic Manager 프로필에 대 한 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28f25-108">The **Get-AzureRmTrafficManagerEndpoint** cmdlet gets an endpoint for an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="28f25-109">이 개체를 로컬로 수정한 다음 Set-AzureRmTrafficManagerEndpoint cmdlet을 사용 하 여 프로필에 변경 내용을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28f25-109">You can modify this object locally, and then apply changes to the profile by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="28f25-110">*Name* 및 *Type* 매개 변수를 사용 하 여 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28f25-110">Specify the endpoint by using the *Name* and *Type* parameters.</span></span>
<span data-ttu-id="28f25-111">*/Profile* 및 *ResourceGroupName* 매개 변수를 사용 하거나 **TrafficManagerProfile** 개체를 지정 하 여 Traffic Manager 프로필을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28f25-111">You can specify the Traffic Manager profile either by using the *ProfileName* and *ResourceGroupName* parameter, or by specifying a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="28f25-112">또는 파이프라인을 사용 하 여 해당 값을 전달할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28f25-112">Alternatively, you can pass that value by using the pipeline.</span></span>

## <span data-ttu-id="28f25-113">예제의</span><span class="sxs-lookup"><span data-stu-id="28f25-113">EXAMPLES</span></span>

### <span data-ttu-id="28f25-114">예제 1: 끝점 가져오기</span><span class="sxs-lookup"><span data-stu-id="28f25-114">Example 1: Get an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="28f25-115">이 명령은 ResourceGroup11 이라는 리소스 그룹에 있는 ContosoProfile 이라는 프로필에서 contoso 라는 Azure 끝점을 가져온 다음 해당 개체를 $TrafficManagerEndpoint 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="28f25-115">This command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>

## <span data-ttu-id="28f25-116">변수</span><span class="sxs-lookup"><span data-stu-id="28f25-116">PARAMETERS</span></span>

### <span data-ttu-id="28f25-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28f25-117">-DefaultProfile</span></span>
<span data-ttu-id="28f25-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="28f25-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28f25-119">-이름</span><span class="sxs-lookup"><span data-stu-id="28f25-119">-Name</span></span>
<span data-ttu-id="28f25-120">이 cmdlet이 가져오는 Traffic Manager 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28f25-120">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="28f25-121">-/Profile</span><span class="sxs-lookup"><span data-stu-id="28f25-121">-ProfileName</span></span>
<span data-ttu-id="28f25-122">이 cmdlet이 가져오는 Traffic Manager 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28f25-122">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="28f25-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28f25-123">-ResourceGroupName</span></span>
<span data-ttu-id="28f25-124">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28f25-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="28f25-125">이 cmdlet은이 매개 변수에서 지정 하는 그룹의 Traffic Manager 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="28f25-125">This cmdlet gets a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="28f25-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="28f25-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="28f25-127">이 cmdlet이 가져오는 트래픽 관리자 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28f25-127">Specifies the Traffic Manager endpoint that this cmdlet gets.</span></span>

```yaml
Type: TrafficManagerEndpoint
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28f25-128">-Type</span><span class="sxs-lookup"><span data-stu-id="28f25-128">-Type</span></span>
<span data-ttu-id="28f25-129">이 cmdlet이 Traffic Manager 프로필에 추가 하는 끝점 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28f25-129">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="28f25-130">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="28f25-130">Valid values are:</span></span> 

- <span data-ttu-id="28f25-131">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="28f25-131">AzureEndpoints</span></span>
- <span data-ttu-id="28f25-132">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="28f25-132">ExternalEndpoints</span></span>
- <span data-ttu-id="28f25-133">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="28f25-133">NestedEndpoints</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f25-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28f25-134">CommonParameters</span></span>
<span data-ttu-id="28f25-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="28f25-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28f25-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28f25-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28f25-137">입력</span><span class="sxs-lookup"><span data-stu-id="28f25-137">INPUTS</span></span>

### <span data-ttu-id="28f25-138">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="28f25-138">TrafficManagerEndpoint</span></span>
<span data-ttu-id="28f25-139">' TrafficManagerEndpoint ' 매개 변수는 파이프라인에서 ' TrafficManagerEndpoint ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="28f25-139">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="28f25-140">출력</span><span class="sxs-lookup"><span data-stu-id="28f25-140">OUTPUTS</span></span>

### <span data-ttu-id="28f25-141">TrafficManager. TrafficManagerEndpoint/.</span><span class="sxs-lookup"><span data-stu-id="28f25-141">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="28f25-142">상속자</span><span class="sxs-lookup"><span data-stu-id="28f25-142">NOTES</span></span>

## <span data-ttu-id="28f25-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="28f25-143">RELATED LINKS</span></span>

[<span data-ttu-id="28f25-144">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="28f25-144">Disable-AzureRmTrafficManagerEndpoint</span></span>](./Disable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="28f25-145">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="28f25-145">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="28f25-146">새로운 AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="28f25-146">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="28f25-147">제거-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="28f25-147">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="28f25-148">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="28f25-148">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)


