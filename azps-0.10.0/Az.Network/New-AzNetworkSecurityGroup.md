---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkSecurityGroup.md
ms.openlocfilehash: 4606ea7a9e403ad5963aacc9ee85b89068635325
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875421"
---
# <span data-ttu-id="a5d84-101">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a5d84-101">New-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="a5d84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5d84-102">SYNOPSIS</span></span>
<span data-ttu-id="a5d84-103">네트워크 보안 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a5d84-103">Creates a network security group.</span></span>

## <span data-ttu-id="a5d84-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a5d84-104">SYNTAX</span></span>

```
New-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSecurityRule]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5d84-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a5d84-105">DESCRIPTION</span></span>
<span data-ttu-id="a5d84-106">**새 AzNetworkSecurityGroup** Cmdlet은 Azure 네트워크 보안 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a5d84-106">The **New-AzNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="a5d84-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a5d84-107">EXAMPLES</span></span>

### <span data-ttu-id="a5d84-108">1: 새 네트워크 securtiy 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="a5d84-108">1: Create a new network securtiy group</span></span>
```
New-AzNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="a5d84-109">이 명령은 "westus" 위치의 "rg1" 리소스 그룹에 "nsg1" 이라는 새 Azure 네트워크 보안 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a5d84-109">This command ceates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="a5d84-110">2: 상세 네트워크 보안 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="a5d84-110">2: Create a detailed network security group</span></span>
```
$rule1 = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP"
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$rule2 = New-AzNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP"
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80

$nsg = New-AzNetworkSecurityGroup -ResourceGroupName TestRG -Location westus -Name
    "NSG-FrontEnd" -SecurityRules $rule1,$rule2
```

<span data-ttu-id="a5d84-111">단계: 1 인터넷에서 포트 3389으로의 액세스를 허용 하는 보안 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a5d84-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="a5d84-112">단계: 2 인터넷에서 포트 80으로의 액세스를 허용 하는 보안 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a5d84-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="a5d84-113">단계: 3 위에서 만든 규칙을 NSG-프런트 엔드 라는 새 NSG에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d84-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="a5d84-114">변수</span><span class="sxs-lookup"><span data-stu-id="a5d84-114">PARAMETERS</span></span>

### <span data-ttu-id="a5d84-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5d84-115">-AsJob</span></span>
<span data-ttu-id="a5d84-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a5d84-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5d84-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5d84-117">-DefaultProfile</span></span>
<span data-ttu-id="a5d84-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5d84-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5d84-119">-Force</span><span class="sxs-lookup"><span data-stu-id="a5d84-119">-Force</span></span>
<span data-ttu-id="a5d84-120">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d84-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5d84-121">-위치</span><span class="sxs-lookup"><span data-stu-id="a5d84-121">-Location</span></span>
<span data-ttu-id="a5d84-122">네트워크 보안 그룹을 만들 지역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d84-122">Specifies the region for which to create a network security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5d84-123">-이름</span><span class="sxs-lookup"><span data-stu-id="a5d84-123">-Name</span></span>
<span data-ttu-id="a5d84-124">만들려는 네트워크 보안 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d84-124">Specifies the name of the network security group to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5d84-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5d84-125">-ResourceGroupName</span></span>
<span data-ttu-id="a5d84-126">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d84-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="a5d84-127">이 cmdlet은이 매개 변수에서 지정 하는 네트워크 보안 그룹을 리소스 그룹에 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a5d84-127">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5d84-128">-SecurityRules</span><span class="sxs-lookup"><span data-stu-id="a5d84-128">-SecurityRules</span></span>
<span data-ttu-id="a5d84-129">네트워크 보안 그룹에서 만들 네트워크 보안 규칙 개체의 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d84-129">Specifies a list of network security rule objects to create in a network security group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSecurityRule]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5d84-130">태그</span><span class="sxs-lookup"><span data-stu-id="a5d84-130">-Tag</span></span>
<span data-ttu-id="a5d84-131">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="a5d84-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a5d84-132">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="a5d84-132">For example:</span></span>

<span data-ttu-id="a5d84-133">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="a5d84-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5d84-134">-확인</span><span class="sxs-lookup"><span data-stu-id="a5d84-134">-Confirm</span></span>
<span data-ttu-id="a5d84-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d84-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5d84-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5d84-136">-WhatIf</span></span>
<span data-ttu-id="a5d84-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a5d84-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5d84-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5d84-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5d84-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5d84-139">CommonParameters</span></span>
<span data-ttu-id="a5d84-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5d84-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5d84-141">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5d84-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5d84-142">입력</span><span class="sxs-lookup"><span data-stu-id="a5d84-142">INPUTS</span></span>

## <span data-ttu-id="a5d84-143">출력</span><span class="sxs-lookup"><span data-stu-id="a5d84-143">OUTPUTS</span></span>

### <span data-ttu-id="a5d84-144">Microsoft. 네트워크 모델. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a5d84-144">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="a5d84-145">상속자</span><span class="sxs-lookup"><span data-stu-id="a5d84-145">NOTES</span></span>

## <span data-ttu-id="a5d84-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5d84-146">RELATED LINKS</span></span>

[<span data-ttu-id="a5d84-147">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a5d84-147">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="a5d84-148">제거-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a5d84-148">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="a5d84-149">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a5d84-149">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)
