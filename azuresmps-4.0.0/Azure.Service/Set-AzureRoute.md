---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A7DFF559-188D-4CF9-9315-CA327E0C5C0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: d502ba2961e5238426228e4ac58a29b922be81f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045823"
---
# <span data-ttu-id="26808-101">Set-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="26808-101">Set-AzureRoute</span></span>

## <span data-ttu-id="26808-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26808-102">SYNOPSIS</span></span>
<span data-ttu-id="26808-103">경로 테이블에 경로를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26808-103">Creates a route in a route table.</span></span>

## <span data-ttu-id="26808-104">구문과</span><span class="sxs-lookup"><span data-stu-id="26808-104">SYNTAX</span></span>

```
Set-AzureRoute -RouteName <String> -AddressPrefix <String> -NextHopType <String> [-NextHopIpAddress <String>]
 -RouteTable <IRouteTable> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="26808-105">설명은</span><span class="sxs-lookup"><span data-stu-id="26808-105">DESCRIPTION</span></span>
<span data-ttu-id="26808-106">**Set-AzureRoute** cmdlet은 경로 테이블에 경로를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26808-106">The **Set-AzureRoute** cmdlet creates a route in a route table.</span></span>
<span data-ttu-id="26808-107">새 경로는 경로 테이블과 연결 된 가상 컴퓨터 바로 다음에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="26808-107">The new route takes effect almost immediately on the virtual machines that are associated with the route table.</span></span>

## <span data-ttu-id="26808-108">예제의</span><span class="sxs-lookup"><span data-stu-id="26808-108">EXAMPLES</span></span>

### <span data-ttu-id="26808-109">예제 1: 가상 기기 다음 홉 경로 추가</span><span class="sxs-lookup"><span data-stu-id="26808-109">Example 1: Add a virtual appliance next hop route</span></span>
```
PS C:\> New-AzureRouteTable -Name "ApplianceRouteTable" -Location "Central US" -Label "Appliance Route Table" | Set-AzureRoute -RouteName "ApplianceRoute03" -AddressPrefix "10.0.0.0/24" -NextHopType VirtualAppliance -NextHopIpAddress "10.0.1.5"

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    AppRT                         Central US                    Appliance Route Table
```

<span data-ttu-id="26808-110">이 명령은 지정 된 위치에 ApplianceRouteTable 이라는 경로 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26808-110">This command creates a route table named ApplianceRouteTable in the specified location.</span></span>
<span data-ttu-id="26808-111">명령이 현재 cmdlet에 경로 테이블을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="26808-111">The command passes that route table to the current cmdlet.</span></span>
<span data-ttu-id="26808-112">현재 cmdlet은 VirtualAppliance 다음 홉 유형인 ApplianceRoute03 이라는 경로를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="26808-112">The current cmdlet adds a route named ApplianceRoute03, which is a VirtualAppliance next hop type.</span></span>
<span data-ttu-id="26808-113">이 명령은 경로의 다음 홉 IP 주소와 주소 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26808-113">The command specifies the next hop IP address and the address prefix for the route.</span></span>

### <span data-ttu-id="26808-114">예제 2: 인터넷 다음 홉 경로 추가</span><span class="sxs-lookup"><span data-stu-id="26808-114">Example 2: Add an Internet next hop route</span></span>
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" | Set-AzureRoute -RouteName "InternetRoute" -AddressPrefix "0.0.0.0/0" -NextHopType Internet

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute, internetroute}     AppRT                         Central US                    Appliance Route Table
```

<span data-ttu-id="26808-115">이 명령은 ApplianceRouteTable 이라는 경로 테이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="26808-115">This command gets a route table named ApplianceRouteTable.</span></span>
<span data-ttu-id="26808-116">명령이 현재 cmdlet에 경로 테이블을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="26808-116">The command passes that route table to the current cmdlet.</span></span>
<span data-ttu-id="26808-117">현재 cmdlet은 인터넷 다음 홉 유형인 InternetRoute 라는 경로를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="26808-117">The current cmdlet adds a route named InternetRoute, which is an Internet next hop type.</span></span>
<span data-ttu-id="26808-118">명령은 경로에 대 한 주소 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26808-118">The command specifies the address prefix for the route.</span></span>

## <span data-ttu-id="26808-119">변수</span><span class="sxs-lookup"><span data-stu-id="26808-119">PARAMETERS</span></span>

### <span data-ttu-id="26808-120">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="26808-120">-AddressPrefix</span></span>
<span data-ttu-id="26808-121">새 경로의 주소 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26808-121">Specifies an address prefix for the new route.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26808-122">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="26808-122">-NextHopIpAddress</span></span>
<span data-ttu-id="26808-123">이 경로를 사용 하는 트래픽에 대 한 다음 홉 인 기기의 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26808-123">Specifies the IP address of the appliance that is the next hop for traffic that uses this route.</span></span>
<span data-ttu-id="26808-124">*NextHopType* 매개 변수에 virtualappliance 값을 지정 하는 경우에만이 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26808-124">Specify this value only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="26808-125">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="26808-125">-NextHopType</span></span>
<span data-ttu-id="26808-126">이 경로를 사용 하는 트래픽에 대 한 다음 홉 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26808-126">Specifies the next hop type for traffic that uses this route.</span></span>
<span data-ttu-id="26808-127">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="26808-127">Valid values are:</span></span> 

- <span data-ttu-id="26808-128">VPNGateway</span><span class="sxs-lookup"><span data-stu-id="26808-128">VPNGateway</span></span>
- <span data-ttu-id="26808-129">VNETLocal</span><span class="sxs-lookup"><span data-stu-id="26808-129">VNETLocal</span></span>
- <span data-ttu-id="26808-130">인터넷</span><span class="sxs-lookup"><span data-stu-id="26808-130">Internet</span></span>
- <span data-ttu-id="26808-131">VirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="26808-131">VirtualAppliance</span></span>
- <span data-ttu-id="26808-132">L</span><span class="sxs-lookup"><span data-stu-id="26808-132">Null</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26808-133">-프로필</span><span class="sxs-lookup"><span data-stu-id="26808-133">-Profile</span></span>
<span data-ttu-id="26808-134">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26808-134">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="26808-135">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="26808-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26808-136">-RouteName</span><span class="sxs-lookup"><span data-stu-id="26808-136">-RouteName</span></span>
<span data-ttu-id="26808-137">이 cmdlet에 추가 되는 새 경로의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26808-137">Specifies a name for the new route that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26808-138">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="26808-138">-RouteTable</span></span>
<span data-ttu-id="26808-139">이 cmdlet이 새 경로를 추가 하는 경로 테이블을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26808-139">Specifies the route table to which this cmdlet adds the new route.</span></span>

```yaml
Type: IRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26808-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26808-140">CommonParameters</span></span>
<span data-ttu-id="26808-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="26808-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26808-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26808-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26808-143">입력</span><span class="sxs-lookup"><span data-stu-id="26808-143">INPUTS</span></span>

## <span data-ttu-id="26808-144">출력</span><span class="sxs-lookup"><span data-stu-id="26808-144">OUTPUTS</span></span>

## <span data-ttu-id="26808-145">상속자</span><span class="sxs-lookup"><span data-stu-id="26808-145">NOTES</span></span>

## <span data-ttu-id="26808-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26808-146">RELATED LINKS</span></span>

[<span data-ttu-id="26808-147">제거-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="26808-147">Remove-AzureRoute</span></span>](./Remove-AzureRoute.md)


