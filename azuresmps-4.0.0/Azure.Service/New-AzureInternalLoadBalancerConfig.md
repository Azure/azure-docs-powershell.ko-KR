---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8C01AFE1-65E7-4C5F-B3ED-8FCD9C4D20FC
online version: ''
schema: 2.0.0
ms.openlocfilehash: a42ffe7ded2eb47638dd961ae79b10dd21cf08ad
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045914"
---
# <span data-ttu-id="80544-101">New-AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="80544-101">New-AzureInternalLoadBalancerConfig</span></span>

## <span data-ttu-id="80544-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80544-102">SYNOPSIS</span></span>
<span data-ttu-id="80544-103">내부 부하 분산 장치 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="80544-103">Creates an internal load balancer configuration.</span></span>

## <span data-ttu-id="80544-104">구문과</span><span class="sxs-lookup"><span data-stu-id="80544-104">SYNTAX</span></span>

### <span data-ttu-id="80544-105">ServiceAndSlot (기본값)</span><span class="sxs-lookup"><span data-stu-id="80544-105">ServiceAndSlot (Default)</span></span>
```
New-AzureInternalLoadBalancerConfig [-InternalLoadBalancerName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="80544-106">SubnetNameOnly</span><span class="sxs-lookup"><span data-stu-id="80544-106">SubnetNameOnly</span></span>
```
New-AzureInternalLoadBalancerConfig [-InternalLoadBalancerName] <String> [-SubnetName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="80544-107">SubnetNameAndIP</span><span class="sxs-lookup"><span data-stu-id="80544-107">SubnetNameAndIP</span></span>
```
New-AzureInternalLoadBalancerConfig [-InternalLoadBalancerName] <String> [-SubnetName] <String>
 [-StaticVNetIPAddress] <IPAddress> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="80544-108">설명은</span><span class="sxs-lookup"><span data-stu-id="80544-108">DESCRIPTION</span></span>
<span data-ttu-id="80544-109">**AzureInternalLoadBalancerConfig** Cmdlet은 **InternalLoadBalancerConfig** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="80544-109">The **New-AzureInternalLoadBalancerConfig** cmdlet creates an **InternalLoadBalancerConfig** object.</span></span>
<span data-ttu-id="80544-110">Azure 가상 컴퓨터 배포를 만들 때 내부 부하 분산 장치 구성을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="80544-110">You can use an internal load balancer configuration when you create an Azure virtual machine deployment.</span></span>

## <span data-ttu-id="80544-111">예제의</span><span class="sxs-lookup"><span data-stu-id="80544-111">EXAMPLES</span></span>

### <span data-ttu-id="80544-112">예제 1: 내부 부하 분산 장치 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="80544-112">Example 1: Create an internal load balancer configuration</span></span>
```
PS C:\> $IlbConfig = New-AzureInternalLoadBalancerConfig -InternalLoadBalancerName "Contoso" -SubnetName "FrontEndSubnet"
```

<span data-ttu-id="80544-113">이 명령은 FrontEndSubnet 이라는 서브넷에 대 한 내부 부하 분산 장치 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="80544-113">This command creates an internal load balancer configuration for the subnet named FrontEndSubnet.</span></span>
<span data-ttu-id="80544-114">명령은 가상 컴퓨터 배포에 사용할 수 있도록 $IlbConfig 변수에 구성을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="80544-114">The command stores the configuration in the $IlbConfig variable for you to use for a virtual machine deployment.</span></span>

## <span data-ttu-id="80544-115">변수</span><span class="sxs-lookup"><span data-stu-id="80544-115">PARAMETERS</span></span>

### <span data-ttu-id="80544-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="80544-116">-InformationAction</span></span>
<span data-ttu-id="80544-117">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80544-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="80544-118">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="80544-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="80544-119">하기로</span><span class="sxs-lookup"><span data-stu-id="80544-119">Continue</span></span>
- <span data-ttu-id="80544-120">숨기기</span><span class="sxs-lookup"><span data-stu-id="80544-120">Ignore</span></span>
- <span data-ttu-id="80544-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="80544-121">Inquire</span></span>
- <span data-ttu-id="80544-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="80544-122">SilentlyContinue</span></span>
- <span data-ttu-id="80544-123">중지가</span><span class="sxs-lookup"><span data-stu-id="80544-123">Stop</span></span>
- <span data-ttu-id="80544-124">대기</span><span class="sxs-lookup"><span data-stu-id="80544-124">Suspend</span></span>

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

### <span data-ttu-id="80544-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="80544-125">-InformationVariable</span></span>
<span data-ttu-id="80544-126">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80544-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="80544-127">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="80544-127">-InternalLoadBalancerName</span></span>
<span data-ttu-id="80544-128">이 cmdlet가 구성에 포함 하는 내부 부하 분산의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80544-128">Specifies the name of the internal load balancer that this cmdlet includes in the configuration.</span></span>

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

### <span data-ttu-id="80544-129">-프로필</span><span class="sxs-lookup"><span data-stu-id="80544-129">-Profile</span></span>
<span data-ttu-id="80544-130">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80544-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="80544-131">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="80544-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="80544-132">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="80544-132">-StaticVNetIPAddress</span></span>
<span data-ttu-id="80544-133">이 cmdlet가 구성에 포함 하는 내부 부하 분산 장치에 대 한 가상 네트워크 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80544-133">Specifies the virtual network IP address for an internal load balancer that this cmdlet includes in the configuration.</span></span>

```yaml
Type: IPAddress
Parameter Sets: SubnetNameAndIP
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80544-134">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="80544-134">-SubnetName</span></span>
<span data-ttu-id="80544-135">내부 부하 분산 장치에 대 한 서브넷의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="80544-135">Specifies the name of the subnet for an internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SubnetNameOnly, SubnetNameAndIP
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80544-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80544-136">CommonParameters</span></span>
<span data-ttu-id="80544-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="80544-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80544-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80544-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80544-139">입력</span><span class="sxs-lookup"><span data-stu-id="80544-139">INPUTS</span></span>

## <span data-ttu-id="80544-140">출력</span><span class="sxs-lookup"><span data-stu-id="80544-140">OUTPUTS</span></span>

### <span data-ttu-id="80544-141">WindowsAzure. ServiceManagement. InternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="80544-141">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.InternalLoadBalancerConfig</span></span>

## <span data-ttu-id="80544-142">상속자</span><span class="sxs-lookup"><span data-stu-id="80544-142">NOTES</span></span>

## <span data-ttu-id="80544-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="80544-143">RELATED LINKS</span></span>

[<span data-ttu-id="80544-144">추가-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="80544-144">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="80544-145">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="80544-145">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="80544-146">제거-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="80544-146">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)

[<span data-ttu-id="80544-147">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="80544-147">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


