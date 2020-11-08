---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 125B6865-0022-4F88-BB0F-DDDDB2EDFF00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a1f1d033c3e8bae708310d12a1c4cb2b581bf80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045800"
---
# <span data-ttu-id="c6d1b-101">Set-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="c6d1b-101">Set-AzureNetworkSecurityRule</span></span>

## <span data-ttu-id="c6d1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6d1b-102">SYNOPSIS</span></span>
<span data-ttu-id="c6d1b-103">네트워크 보안 그룹에서 네트워크 보안 규칙을 추가 하거나 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6d1b-103">Adds or modifies a network security rule in a network security group.</span></span>

## <span data-ttu-id="c6d1b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c6d1b-104">SYNTAX</span></span>

```
Set-AzureNetworkSecurityRule -Name <String> -Type <String> -Priority <Int32> -Action <String>
 -SourceAddressPrefix <String> -SourcePortRange <String> -DestinationAddressPrefix <String>
 -DestinationPortRange <String> -Protocol <String> -NetworkSecurityGroup <INetworkSecurityGroup>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c6d1b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c6d1b-105">DESCRIPTION</span></span>
<span data-ttu-id="c6d1b-106">**AzureNetworkSecurityRule** cmdlet은 네트워크 보안 그룹에서 Azure 네트워크 보안 규칙을 추가 하거나 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6d1b-106">The **Set-AzureNetworkSecurityRule** cmdlet adds or modifies an Azure network security rule in a network security group.</span></span>

## <span data-ttu-id="c6d1b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c6d1b-107">EXAMPLES</span></span>

## <span data-ttu-id="c6d1b-108">변수</span><span class="sxs-lookup"><span data-stu-id="c6d1b-108">PARAMETERS</span></span>

### <span data-ttu-id="c6d1b-109">-작업</span><span class="sxs-lookup"><span data-stu-id="c6d1b-109">-Action</span></span>
<span data-ttu-id="c6d1b-110">네트워크 보안 규칙에 대 한 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6d1b-110">Specifies the action for a network security rule.</span></span>
<span data-ttu-id="c6d1b-111">유효한 값은 Allow 및 Deny입니다.</span><span class="sxs-lookup"><span data-stu-id="c6d1b-111">Valid values are: Allow and Deny.</span></span>

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

### <span data-ttu-id="c6d1b-112">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c6d1b-112">-DestinationAddressPrefix</span></span>
<span data-ttu-id="c6d1b-113">네트워크 보안 규칙에 대 한 대상 IP 범위의 CIDR (클래스 간 라우팅) 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6d1b-113">Specifies the Classless Interdomain Routing (CIDR) address of the destination IP range for the network security rule.</span></span>
<span data-ttu-id="c6d1b-114">별표 (\*)는 모든 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6d1b-114">An asterisk (\*) specifies any IP address.</span></span>

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

### <span data-ttu-id="c6d1b-115">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="c6d1b-115">-DestinationPortRange</span></span>
<span data-ttu-id="c6d1b-116">네트워크 보안 규칙에 대 한 대상 포트 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6d1b-116">Specifies a destination port range for the network security rule.</span></span>
<span data-ttu-id="c6d1b-117">유효한 값은 0에서 65535 까지의 정수로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6d1b-117">Valid values consist of integers from 0 to 65535.</span></span>
<span data-ttu-id="c6d1b-118">개별 값을 지정 하거나 LowerNumber-HigherNumber 형식으로 범위를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6d1b-118">You can specify an individual value, or specify a range in the format LowerNumber-HigherNumber.</span></span>
<span data-ttu-id="c6d1b-119">하이픈은 두 값을 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6d1b-119">A hyphen separates the two values.</span></span>

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

### <span data-ttu-id="c6d1b-120">-이름</span><span class="sxs-lookup"><span data-stu-id="c6d1b-120">-Name</span></span>
<span data-ttu-id="c6d1b-121">이 cmdlet이 추가 하거나 수정 하는 네트워크 보안 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6d1b-121">Specifies the name for the network security rule that this cmdlet adds or modifies.</span></span>

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

### <span data-ttu-id="c6d1b-122">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c6d1b-122">-NetworkSecurityGroup</span></span>
<span data-ttu-id="c6d1b-123">이 cmdlet이 수정 하는 네트워크 보안 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6d1b-123">Specifies the network security group that this cmdlet modifies.</span></span>
<span data-ttu-id="c6d1b-124">**INetworkSecurityGroup** 개체를 가져오려면 Get-AzureNetworkSecurityGroup cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6d1b-124">To obtain an **INetworkSecurityGroup** object, use the Get-AzureNetworkSecurityGroup cmdlet.</span></span>

```yaml
Type: INetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6d1b-125">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="c6d1b-125">-Priority</span></span>
<span data-ttu-id="c6d1b-126">네트워크 보안 규칙에 대 한 우선 순위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6d1b-126">Specifies the priority for the network security rule.</span></span>
<span data-ttu-id="c6d1b-127">유효한 값은 100부터 4096 까지의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="c6d1b-127">Valid values are: integers from 100 to 4096.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6d1b-128">-프로필</span><span class="sxs-lookup"><span data-stu-id="c6d1b-128">-Profile</span></span>
<span data-ttu-id="c6d1b-129">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6d1b-129">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="c6d1b-130">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="c6d1b-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c6d1b-131">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="c6d1b-131">-Protocol</span></span>
<span data-ttu-id="c6d1b-132">네트워크 보안 규칙에 대 한 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6d1b-132">Specifies the protocol for the network security rule.</span></span>
<span data-ttu-id="c6d1b-133">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c6d1b-133">Valid values are:</span></span> 

- <span data-ttu-id="c6d1b-134">NET.TCP</span><span class="sxs-lookup"><span data-stu-id="c6d1b-134">TCP</span></span> 
- <span data-ttu-id="c6d1b-135">UDP</span><span class="sxs-lookup"><span data-stu-id="c6d1b-135">UDP</span></span> 
- *

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

### <span data-ttu-id="c6d1b-136">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c6d1b-136">-SourceAddressPrefix</span></span>
<span data-ttu-id="c6d1b-137">네트워크 보안 규칙의 원본 IP 범위에 대 한 CIDR 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6d1b-137">Specifies the CIDR address of the source IP range for the network security rule.</span></span>
<span data-ttu-id="c6d1b-138">별표 (\*)는 모든 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6d1b-138">An asterisk (\*) specifies any IP address.</span></span>

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

### <span data-ttu-id="c6d1b-139">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="c6d1b-139">-SourcePortRange</span></span>
<span data-ttu-id="c6d1b-140">네트워크 보안 규칙의 원본 포트 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6d1b-140">Specifies a source port range for the network security rule.</span></span>
<span data-ttu-id="c6d1b-141">유효한 값은 0에서 65535 까지의 정수로 구성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6d1b-141">Valid values consist of integers from 0 to 65535.</span></span>
<span data-ttu-id="c6d1b-142">개별 값을 지정 하거나 LowerNumber-HigherNumber 형식으로 범위를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6d1b-142">You can specify an individual value, or specify a range in the format LowerNumber-HigherNumber.</span></span>
<span data-ttu-id="c6d1b-143">하이픈은 두 값을 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6d1b-143">A hyphen separates the two values.</span></span>

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

### <span data-ttu-id="c6d1b-144">-Type</span><span class="sxs-lookup"><span data-stu-id="c6d1b-144">-Type</span></span>
<span data-ttu-id="c6d1b-145">네트워크 보안 규칙에 대 한 연결 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6d1b-145">Specifies the type of connection for the network security rule.</span></span>
<span data-ttu-id="c6d1b-146">유효한 값은 인바운드와 아웃 바운드입니다.</span><span class="sxs-lookup"><span data-stu-id="c6d1b-146">Valid values are: Inbound and Outbound.</span></span>

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

### <span data-ttu-id="c6d1b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6d1b-147">CommonParameters</span></span>
<span data-ttu-id="c6d1b-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6d1b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6d1b-149">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6d1b-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6d1b-150">입력</span><span class="sxs-lookup"><span data-stu-id="c6d1b-150">INPUTS</span></span>

## <span data-ttu-id="c6d1b-151">출력</span><span class="sxs-lookup"><span data-stu-id="c6d1b-151">OUTPUTS</span></span>

## <span data-ttu-id="c6d1b-152">상속자</span><span class="sxs-lookup"><span data-stu-id="c6d1b-152">NOTES</span></span>

## <span data-ttu-id="c6d1b-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c6d1b-153">RELATED LINKS</span></span>

[<span data-ttu-id="c6d1b-154">제거-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="c6d1b-154">Remove-AzureNetworkSecurityRule</span></span>](./Remove-AzureNetworkSecurityRule.md)


