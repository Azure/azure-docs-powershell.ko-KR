---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4A0442F9-F420-4A26-9127-4C875090CC12
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0e2709ce2939cb45200e758563e917675894e443
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045724"
---
# <span data-ttu-id="e374e-101">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e374e-101">Add-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="e374e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e374e-102">SYNOPSIS</span></span>
<span data-ttu-id="e374e-103">Azure 서비스에 내부 부하 분산 장치를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e374e-103">Adds an internal load balancer to an Azure service.</span></span>

## <span data-ttu-id="e374e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e374e-104">SYNTAX</span></span>

### <span data-ttu-id="e374e-105">ServiceAndSlot (기본값)</span><span class="sxs-lookup"><span data-stu-id="e374e-105">ServiceAndSlot (Default)</span></span>
```
Add-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="e374e-106">SubnetNameOnly</span><span class="sxs-lookup"><span data-stu-id="e374e-106">SubnetNameOnly</span></span>
```
Add-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="e374e-107">SubnetNameAndIP</span><span class="sxs-lookup"><span data-stu-id="e374e-107">SubnetNameAndIP</span></span>
```
Add-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-StaticVNetIPAddress] <IPAddress> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e374e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e374e-108">DESCRIPTION</span></span>
<span data-ttu-id="e374e-109">**추가-AzureInternalLoadBalancer** cmdlet은 내부 부하 분산 장치 구성을 Azure 서비스에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e374e-109">The **Add-AzureInternalLoadBalancer** cmdlet adds an internal load balancer configuration to an Azure service.</span></span>
<span data-ttu-id="e374e-110">가상 네트워크의 경우 내부 부하 분산 장치의 서브넷 또는 IP 주소를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e374e-110">For a virtual network, you can specify a subnet or the IP address of the internal load balancer.</span></span>

## <span data-ttu-id="e374e-111">예제의</span><span class="sxs-lookup"><span data-stu-id="e374e-111">EXAMPLES</span></span>

### <span data-ttu-id="e374e-112">예제 1: 내부 부하 분산 장치 추가</span><span class="sxs-lookup"><span data-stu-id="e374e-112">Example 1: Add an internal load balancer</span></span>
```
PS C:\> Add-AzureInternalLoadBalancer -ServiceName "ContosoWebsite01" -InternalLoadBalancerName "ContosoILB"
```

<span data-ttu-id="e374e-113">이 명령은 ContosoILB 이라는 내부 부하 분산 장치를 ContosoWebsite01 라는 서비스에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e374e-113">This command adds an internal load balancer named ContosoILB to the service named ContosoWebsite01.</span></span>

### <span data-ttu-id="e374e-114">예제 2: 지정 된 서브넷에 대 한 내부 부하 분산 장치 추가</span><span class="sxs-lookup"><span data-stu-id="e374e-114">Example 2: Add an internal load balancer for a specified subnet</span></span>
```
PS C:\> Add-AzureInternalLoadBalancer -ServiceName "ContosoWebsite01" -InternalLoadBalancerName "ContosoILB" -SubnetName "FrontEndSubnet"
```

<span data-ttu-id="e374e-115">이 명령은 ContosoILB 이라는 내부 부하 분산 장치를 ContosoWebsite01 라는 서비스에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e374e-115">This command adds an internal load balancer named ContosoILB to the service named ContosoWebsite01.</span></span>
<span data-ttu-id="e374e-116">명령에서 FrontEndSubnet 이라는 서브넷을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e374e-116">The command specifies the subnet named FrontEndSubnet.</span></span>

### <span data-ttu-id="e374e-117">예제 3: 지정 된 서브넷 및 주소에 대 한 내부 부하 분산 장치 추가</span><span class="sxs-lookup"><span data-stu-id="e374e-117">Example 3: Add an internal load balancer for a specified subnet and address</span></span>
```
PS C:\> Add-AzureInternalLoadBalancer -ServiceName "ContosoWebsite01" -InternalLoadBalancerName "ContosoILB" -SubnetName "FrontEndSubnet" -StaticVNetIPAddress 192.168.4.7
```

<span data-ttu-id="e374e-118">이 명령은 ContosoILB 이라는 내부 부하 분산 장치를 ContosoWebsite01 라는 서비스에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e374e-118">This command adds an internal load balancer named ContosoILB to the service named ContosoWebsite01.</span></span>
<span data-ttu-id="e374e-119">명령은 FrontEndSubnet 이라는 서브넷과 가상 네트워크의 고정 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e374e-119">The command specifies the subnet named FrontEndSubnet and the static address of the virtual network.</span></span>

## <span data-ttu-id="e374e-120">변수</span><span class="sxs-lookup"><span data-stu-id="e374e-120">PARAMETERS</span></span>

### <span data-ttu-id="e374e-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e374e-121">-InformationAction</span></span>
<span data-ttu-id="e374e-122">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e374e-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e374e-123">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e374e-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e374e-124">하기로</span><span class="sxs-lookup"><span data-stu-id="e374e-124">Continue</span></span>
- <span data-ttu-id="e374e-125">숨기기</span><span class="sxs-lookup"><span data-stu-id="e374e-125">Ignore</span></span>
- <span data-ttu-id="e374e-126">Inquire</span><span class="sxs-lookup"><span data-stu-id="e374e-126">Inquire</span></span>
- <span data-ttu-id="e374e-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e374e-127">SilentlyContinue</span></span>
- <span data-ttu-id="e374e-128">중지가</span><span class="sxs-lookup"><span data-stu-id="e374e-128">Stop</span></span>
- <span data-ttu-id="e374e-129">대기</span><span class="sxs-lookup"><span data-stu-id="e374e-129">Suspend</span></span>

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

### <span data-ttu-id="e374e-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e374e-130">-InformationVariable</span></span>
<span data-ttu-id="e374e-131">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e374e-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e374e-132">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="e374e-132">-InternalLoadBalancerName</span></span>
<span data-ttu-id="e374e-133">이 cmdlet이 추가 하는 내부 부하 분산의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e374e-133">Specifies the name of the internal load balancer that this cmdlet adds.</span></span>

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

### <span data-ttu-id="e374e-134">-프로필</span><span class="sxs-lookup"><span data-stu-id="e374e-134">-Profile</span></span>
<span data-ttu-id="e374e-135">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e374e-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e374e-136">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="e374e-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e374e-137">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e374e-137">-ServiceName</span></span>
<span data-ttu-id="e374e-138">이 cmdlet이 내부 부하 분산 장치를 추가 하는 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e374e-138">Specifies the name of the service to which this cmdlet adds an internal load balancer.</span></span>

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

### <span data-ttu-id="e374e-139">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="e374e-139">-StaticVNetIPAddress</span></span>
<span data-ttu-id="e374e-140">이 cmdlet이 추가 하는 내부 부하 분산 장치에 대 한 가상 네트워크 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e374e-140">Specifies the virtual network IP address for an internal load balancer that this cmdlet adds.</span></span>

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

### <span data-ttu-id="e374e-141">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="e374e-141">-SubnetName</span></span>
<span data-ttu-id="e374e-142">이 cmdlet이 추가 하는 내부 부하 분산 장치에 대 한 서브넷의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e374e-142">Specifies the name of the subnet for an internal load balancer that this cmdlet adds.</span></span>

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

### <span data-ttu-id="e374e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e374e-143">CommonParameters</span></span>
<span data-ttu-id="e374e-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e374e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e374e-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e374e-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e374e-146">입력</span><span class="sxs-lookup"><span data-stu-id="e374e-146">INPUTS</span></span>

## <span data-ttu-id="e374e-147">출력</span><span class="sxs-lookup"><span data-stu-id="e374e-147">OUTPUTS</span></span>

### <span data-ttu-id="e374e-148">WindowsAzure. 유틸리티. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="e374e-148">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="e374e-149">상속자</span><span class="sxs-lookup"><span data-stu-id="e374e-149">NOTES</span></span>

## <span data-ttu-id="e374e-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e374e-150">RELATED LINKS</span></span>

[<span data-ttu-id="e374e-151">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e374e-151">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="e374e-152">새로운 AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="e374e-152">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="e374e-153">제거-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e374e-153">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)

[<span data-ttu-id="e374e-154">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e374e-154">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


