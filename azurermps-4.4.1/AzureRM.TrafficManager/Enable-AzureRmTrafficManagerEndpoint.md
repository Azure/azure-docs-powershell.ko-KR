---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 32263236-C207-4FE0-AB8A-018118FC7729
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 64fdd0cb3c2fa31396d9e917dcd7c2e26730c755
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525472"
---
# <span data-ttu-id="fcbb3-101">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fcbb3-101">Enable-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="fcbb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcbb3-102">SYNOPSIS</span></span>
<span data-ttu-id="fcbb3-103">Traffic Manager 프로필에서 끝점을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcbb3-103">Enables an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcbb3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fcbb3-104">SYNTAX</span></span>

### <span data-ttu-id="fcbb3-105">필드인</span><span class="sxs-lookup"><span data-stu-id="fcbb3-105">Fields</span></span>
```
Enable-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fcbb3-106">오브젝트가</span><span class="sxs-lookup"><span data-stu-id="fcbb3-106">Object</span></span>
```
Enable-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fcbb3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fcbb3-107">DESCRIPTION</span></span>
<span data-ttu-id="fcbb3-108">AzureRmTrafficManagerEndpoint cmdlet을 **사용** 하면 Azure Traffic Manager 프로필에서 끝점을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fcbb3-108">The **Enable-AzureRmTrafficManagerEndpoint** cmdlet enables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="fcbb3-109">파이프라인 연산자를 사용 하 여이 cmdlet에 **TrafficManagerEndpoint** 개체를 전달 하거나 *TrafficManagerEndpoint* 매개 변수를 사용 하 여 **TrafficManagerEndpoint** 개체를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fcbb3-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="fcbb3-110">또는 *name* 및 *type* 매개 변수를 사용 하 여 */profile* 및 *ResourceGroupName* 매개 변수와 함께 끝점 이름과 형식을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fcbb3-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="fcbb3-111">예제의</span><span class="sxs-lookup"><span data-stu-id="fcbb3-111">EXAMPLES</span></span>

### <span data-ttu-id="fcbb3-112">예제 1: 프로필에서 끝점 사용</span><span class="sxs-lookup"><span data-stu-id="fcbb3-112">Example 1: Enable an endpoint from a profile</span></span>
```
PS C:\>Enable-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="fcbb3-113">이 명령을 사용 하 여 리소스 그룹 ResouceGroup11의 ContosoProfile 이라는 프로필에 contoso 라는 외부 끝점을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcbb3-113">This command enables the external endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>

### <span data-ttu-id="fcbb3-114">예제 2: 파이프라인을 사용 하 여 끝점 활성화</span><span class="sxs-lookup"><span data-stu-id="fcbb3-114">Example 2: Enable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzureRmTrafficManagerEndpoint
```

<span data-ttu-id="fcbb3-115">이 명령은 ResourceGroup11의 ContosoProfile 이라는 프로필에서 Contoso 라는 외부 끝점을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fcbb3-115">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="fcbb3-116">그런 다음 파이프라인 연산자를 사용 하 여 해당 끝점을 **Enable-AzureRmTrafficManagerEndpoint** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcbb3-116">The command then passes that endpoint to the **Enable-AzureRmTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fcbb3-117">해당 cmdlet은 해당 끝점을 사용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcbb3-117">That cmdlet enables that endpoint.</span></span>

## <span data-ttu-id="fcbb3-118">변수</span><span class="sxs-lookup"><span data-stu-id="fcbb3-118">PARAMETERS</span></span>

### <span data-ttu-id="fcbb3-119">-이름</span><span class="sxs-lookup"><span data-stu-id="fcbb3-119">-Name</span></span>
<span data-ttu-id="fcbb3-120">이 cmdlet이 사용할 수 있는 Traffic Manager 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcbb3-120">Specifies the name of the Traffic Manager endpoint that this cmdlet enables.</span></span>

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

### <span data-ttu-id="fcbb3-121">-/Profile</span><span class="sxs-lookup"><span data-stu-id="fcbb3-121">-ProfileName</span></span>
<span data-ttu-id="fcbb3-122">이 cmdlet이 끝점을 사용할 수 있도록 하는 Traffic Manager 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcbb3-122">Specifies the name of a Traffic Manager profile in which this cmdlet enables an endpoint.</span></span>
<span data-ttu-id="fcbb3-123">프로필을 얻으려면 Get-AzureRmTrafficManagerProfile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcbb3-123">To obtain a profile, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="fcbb3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcbb3-124">-ResourceGroupName</span></span>
<span data-ttu-id="fcbb3-125">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcbb3-125">Specifies the name of a resource group.</span></span>
<span data-ttu-id="fcbb3-126">이 cmdlet은이 매개 변수에서 지정 하는 그룹에서 Traffic Manager 끝점을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcbb3-126">This cmdlet enables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="fcbb3-127">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fcbb3-127">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="fcbb3-128">이 cmdlet이 사용할 수 있는 트래픽 관리자 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcbb3-128">Specifies the Traffic Manager endpoint that this cmdlet enables.</span></span>
<span data-ttu-id="fcbb3-129">**TrafficManagerEndpoint** 개체를 가져오려면 Get-AzureRmTrafficManagerEndpoint cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcbb3-129">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="fcbb3-130">-Type</span><span class="sxs-lookup"><span data-stu-id="fcbb3-130">-Type</span></span>
<span data-ttu-id="fcbb3-131">이 cmdlet이 Traffic Manager 프로필에서 사용 하지 않도록 설정 하는 끝점 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcbb3-131">Specifies the type of endpoint that this cmdlet disables in the Traffic Manager profile.</span></span>
<span data-ttu-id="fcbb3-132">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fcbb3-132">Valid values are:</span></span> 

- <span data-ttu-id="fcbb3-133">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="fcbb3-133">AzureEndpoints</span></span>
- <span data-ttu-id="fcbb3-134">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="fcbb3-134">ExternalEndpoints</span></span>
- <span data-ttu-id="fcbb3-135">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="fcbb3-135">NestedEndpoints</span></span>

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

### <span data-ttu-id="fcbb3-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcbb3-136">-DefaultProfile</span></span>
<span data-ttu-id="fcbb3-137">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fcbb3-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcbb3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcbb3-138">CommonParameters</span></span>
<span data-ttu-id="fcbb3-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcbb3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcbb3-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcbb3-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcbb3-141">입력</span><span class="sxs-lookup"><span data-stu-id="fcbb3-141">INPUTS</span></span>

### <span data-ttu-id="fcbb3-142">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fcbb3-142">TrafficManagerEndpoint</span></span>
<span data-ttu-id="fcbb3-143">' TrafficManagerEndpoint ' 매개 변수는 파이프라인에서 ' TrafficManagerEndpoint ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcbb3-143">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="fcbb3-144">출력</span><span class="sxs-lookup"><span data-stu-id="fcbb3-144">OUTPUTS</span></span>

### <span data-ttu-id="fcbb3-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="fcbb3-145">System.Boolean</span></span>

## <span data-ttu-id="fcbb3-146">상속자</span><span class="sxs-lookup"><span data-stu-id="fcbb3-146">NOTES</span></span>

## <span data-ttu-id="fcbb3-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fcbb3-147">RELATED LINKS</span></span>

[<span data-ttu-id="fcbb3-148">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fcbb3-148">Disable-AzureRmTrafficManagerEndpoint</span></span>](./Disable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="fcbb3-149">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fcbb3-149">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="fcbb3-150">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fcbb3-150">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="fcbb3-151">새로운 AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fcbb3-151">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="fcbb3-152">새로운 AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fcbb3-152">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="fcbb3-153">제거-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fcbb3-153">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="fcbb3-154">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fcbb3-154">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


