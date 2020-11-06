---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A420B3E7-2FE9-4D0B-803E-AC28E5F23C59
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: 1ffcad92a50cc332fdcab71337112b8d0c436388
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531390"
---
# <span data-ttu-id="04ec3-101">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="04ec3-101">New-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="04ec3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04ec3-102">SYNOPSIS</span></span>
<span data-ttu-id="04ec3-103">네트워크 보안 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="04ec3-103">Creates a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04ec3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="04ec3-104">SYNTAX</span></span>

```
New-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -Location <String>
 [-SecurityRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSSecurityRule]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="04ec3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="04ec3-105">DESCRIPTION</span></span>
<span data-ttu-id="04ec3-106">**새 AzureRmNetworkSecurityGroup** Cmdlet은 Azure 네트워크 보안 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="04ec3-106">The **New-AzureRmNetworkSecurityGroup** cmdlet creates an Azure network security group.</span></span>

## <span data-ttu-id="04ec3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="04ec3-107">EXAMPLES</span></span>

### <span data-ttu-id="04ec3-108">1: 새 네트워크 보안 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="04ec3-108">1: Create a new network security group</span></span>
```
New-AzureRmNetworkSecurityGroup -Name "nsg1" -ResourceGroupName "rg1"  -Location  "westus"
```

<span data-ttu-id="04ec3-109">이 명령은 "westus" 위치의 "rg1" 리소스 그룹에 "nsg1" 이라는 새 Azure 네트워크 보안 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="04ec3-109">This command creates a new Azure network security group named "nsg1" in resource group "rg1" in location "westus".</span></span>

### <span data-ttu-id="04ec3-110">2: 상세 네트워크 보안 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="04ec3-110">2: Create a detailed network security group</span></span>
```
$rule1 = New-AzureRmNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP"
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389

$rule2 = New-AzureRmNetworkSecurityRuleConfig -Name web-rule -Description "Allow HTTP"
    -Access Allow -Protocol Tcp -Direction Inbound -Priority 101 -SourceAddressPrefix
    Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 80

$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName TestRG -Location westus -Name
    "NSG-FrontEnd" -SecurityRules $rule1,$rule2
```

<span data-ttu-id="04ec3-111">단계: 1 인터넷에서 포트 3389으로의 액세스를 허용 하는 보안 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="04ec3-111">Step:1 Create a security rule allowing access from the Internet to port 3389.</span></span>
<span data-ttu-id="04ec3-112">단계: 2 인터넷에서 포트 80으로의 액세스를 허용 하는 보안 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="04ec3-112">Step:2 Create a security rule allowing access from the Internet to port 80.</span></span>
<span data-ttu-id="04ec3-113">단계: 3 위에서 만든 규칙을 NSG-프런트 엔드 라는 새 NSG에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="04ec3-113">Step:3 Add the rules created above to a new NSG named NSG-FrontEnd.</span></span>

## <span data-ttu-id="04ec3-114">변수</span><span class="sxs-lookup"><span data-stu-id="04ec3-114">PARAMETERS</span></span>

### <span data-ttu-id="04ec3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04ec3-115">-AsJob</span></span>
<span data-ttu-id="04ec3-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="04ec3-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04ec3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04ec3-117">-DefaultProfile</span></span>
<span data-ttu-id="04ec3-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="04ec3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04ec3-119">-Force</span><span class="sxs-lookup"><span data-stu-id="04ec3-119">-Force</span></span>
<span data-ttu-id="04ec3-120">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="04ec3-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04ec3-121">-위치</span><span class="sxs-lookup"><span data-stu-id="04ec3-121">-Location</span></span>
<span data-ttu-id="04ec3-122">네트워크 보안 그룹을 만들 지역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04ec3-122">Specifies the region for which to create a network security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04ec3-123">-이름</span><span class="sxs-lookup"><span data-stu-id="04ec3-123">-Name</span></span>
<span data-ttu-id="04ec3-124">만들려는 네트워크 보안 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04ec3-124">Specifies the name of the network security group to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04ec3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04ec3-125">-ResourceGroupName</span></span>
<span data-ttu-id="04ec3-126">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04ec3-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="04ec3-127">이 cmdlet은이 매개 변수에서 지정 하는 네트워크 보안 그룹을 리소스 그룹에 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="04ec3-127">This cmdlet creates a network security group in the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04ec3-128">-SecurityRules</span><span class="sxs-lookup"><span data-stu-id="04ec3-128">-SecurityRules</span></span>
<span data-ttu-id="04ec3-129">네트워크 보안 그룹에서 만들 네트워크 보안 규칙 개체의 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04ec3-129">Specifies a list of network security rule objects to create in a network security group.</span></span>

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

### <span data-ttu-id="04ec3-130">태그</span><span class="sxs-lookup"><span data-stu-id="04ec3-130">-Tag</span></span>
<span data-ttu-id="04ec3-131">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="04ec3-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="04ec3-132">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="04ec3-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04ec3-133">-확인</span><span class="sxs-lookup"><span data-stu-id="04ec3-133">-Confirm</span></span>
<span data-ttu-id="04ec3-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="04ec3-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04ec3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04ec3-135">-WhatIf</span></span>
<span data-ttu-id="04ec3-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="04ec3-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04ec3-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04ec3-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04ec3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04ec3-138">CommonParameters</span></span>
<span data-ttu-id="04ec3-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="04ec3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04ec3-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04ec3-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04ec3-141">입력</span><span class="sxs-lookup"><span data-stu-id="04ec3-141">INPUTS</span></span>

### <span data-ttu-id="04ec3-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="04ec3-142">System.String</span></span>

### <span data-ttu-id="04ec3-143">System.webserver. List ' 1 [[Microsoft Azure.]. e-모델의 PSSecurityRule, Microsoft Azure. Network, Version = 6.4.1.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="04ec3-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSSecurityRule, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="04ec3-144">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="04ec3-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="04ec3-145">출력</span><span class="sxs-lookup"><span data-stu-id="04ec3-145">OUTPUTS</span></span>

### <span data-ttu-id="04ec3-146">Microsoft. 네트워크 모델. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="04ec3-146">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="04ec3-147">상속자</span><span class="sxs-lookup"><span data-stu-id="04ec3-147">NOTES</span></span>

## <span data-ttu-id="04ec3-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="04ec3-148">RELATED LINKS</span></span>

[<span data-ttu-id="04ec3-149">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="04ec3-149">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="04ec3-150">제거-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="04ec3-150">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="04ec3-151">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="04ec3-151">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)
