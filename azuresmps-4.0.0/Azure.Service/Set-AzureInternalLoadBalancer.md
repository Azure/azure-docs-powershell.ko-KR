---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C6D23ECB-C06E-4EB7-8096-33787E39694D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66f6bac80b219a2b3629b399bb568140a5cef217
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045954"
---
# <span data-ttu-id="a22cd-101">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a22cd-101">Set-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="a22cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a22cd-102">SYNOPSIS</span></span>
<span data-ttu-id="a22cd-103">Azure 서비스의 내부 부하 분산 장치 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a22cd-103">Modifies an internal load balancer configuration in an Azure service.</span></span>

## <span data-ttu-id="a22cd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a22cd-104">SYNTAX</span></span>

### <span data-ttu-id="a22cd-105">ServiceAndSlot (기본값)</span><span class="sxs-lookup"><span data-stu-id="a22cd-105">ServiceAndSlot (Default)</span></span>
```
Set-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="a22cd-106">SubnetNameOnly</span><span class="sxs-lookup"><span data-stu-id="a22cd-106">SubnetNameOnly</span></span>
```
Set-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a22cd-107">SubnetNameAndIP</span><span class="sxs-lookup"><span data-stu-id="a22cd-107">SubnetNameAndIP</span></span>
```
Set-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-StaticVNetIPAddress] <IPAddress> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a22cd-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a22cd-108">DESCRIPTION</span></span>
<span data-ttu-id="a22cd-109">**Set-AzureInternalLoadBalancer** Cmdlet은 Azure 서비스의 내부 부하 분산 장치 구성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a22cd-109">The **Set-AzureInternalLoadBalancer** cmdlet modifies an internal load balancer configuration in an Azure service.</span></span>
<span data-ttu-id="a22cd-110">가상 네트워크의 경우 내부 부하 분산 장치의 서브넷 또는 IP 주소를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a22cd-110">For a virtual network, you can specify a subnet or the IP address of the internal load balancer.</span></span>

## <span data-ttu-id="a22cd-111">예제의</span><span class="sxs-lookup"><span data-stu-id="a22cd-111">EXAMPLES</span></span>

### <span data-ttu-id="a22cd-112">raid-1</span><span class="sxs-lookup"><span data-stu-id="a22cd-112">1:</span></span>
```

```

## <span data-ttu-id="a22cd-113">변수</span><span class="sxs-lookup"><span data-stu-id="a22cd-113">PARAMETERS</span></span>

### <span data-ttu-id="a22cd-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a22cd-114">-InformationAction</span></span>
<span data-ttu-id="a22cd-115">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a22cd-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a22cd-116">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a22cd-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a22cd-117">하기로</span><span class="sxs-lookup"><span data-stu-id="a22cd-117">Continue</span></span>
- <span data-ttu-id="a22cd-118">숨기기</span><span class="sxs-lookup"><span data-stu-id="a22cd-118">Ignore</span></span>
- <span data-ttu-id="a22cd-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="a22cd-119">Inquire</span></span>
- <span data-ttu-id="a22cd-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a22cd-120">SilentlyContinue</span></span>
- <span data-ttu-id="a22cd-121">중지가</span><span class="sxs-lookup"><span data-stu-id="a22cd-121">Stop</span></span>
- <span data-ttu-id="a22cd-122">대기</span><span class="sxs-lookup"><span data-stu-id="a22cd-122">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a22cd-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a22cd-123">-InformationVariable</span></span>
<span data-ttu-id="a22cd-124">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a22cd-124">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a22cd-125">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="a22cd-125">-InternalLoadBalancerName</span></span>
<span data-ttu-id="a22cd-126">이 cmdlet이 수정 하는 내부 부하 분산의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a22cd-126">Specifies the name of the internal load balancer that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a22cd-127">-프로필</span><span class="sxs-lookup"><span data-stu-id="a22cd-127">-Profile</span></span>
<span data-ttu-id="a22cd-128">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a22cd-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a22cd-129">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="a22cd-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a22cd-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a22cd-130">-ServiceName</span></span>
<span data-ttu-id="a22cd-131">이 cmdlet이 내부 부하 분산을 수정 하는 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a22cd-131">Specifies the name of the service in which this cmdlet modifies an internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a22cd-132">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="a22cd-132">-StaticVNetIPAddress</span></span>
<span data-ttu-id="a22cd-133">내부 부하 분산 장치에 대 한 가상 네트워크 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a22cd-133">Specifies the virtual network IP address for an internal load balancer.</span></span>

```yaml
Type: IPAddress
Parameter Sets: SubnetNameAndIP
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a22cd-134">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="a22cd-134">-SubnetName</span></span>
<span data-ttu-id="a22cd-135">내부 부하 분산 장치에 대 한 서브넷의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a22cd-135">Specifies the name of the subnet for an internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SubnetNameOnly, SubnetNameAndIP
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a22cd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a22cd-136">CommonParameters</span></span>
<span data-ttu-id="a22cd-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a22cd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a22cd-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a22cd-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a22cd-139">입력</span><span class="sxs-lookup"><span data-stu-id="a22cd-139">INPUTS</span></span>

## <span data-ttu-id="a22cd-140">출력</span><span class="sxs-lookup"><span data-stu-id="a22cd-140">OUTPUTS</span></span>

## <span data-ttu-id="a22cd-141">상속자</span><span class="sxs-lookup"><span data-stu-id="a22cd-141">NOTES</span></span>

## <span data-ttu-id="a22cd-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a22cd-142">RELATED LINKS</span></span>

[<span data-ttu-id="a22cd-143">추가-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a22cd-143">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="a22cd-144">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a22cd-144">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="a22cd-145">새로운 AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="a22cd-145">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="a22cd-146">제거-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a22cd-146">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)


