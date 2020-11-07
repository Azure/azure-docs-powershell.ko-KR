---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 6813bf30da73f09f285151d6d309eb89b32acbb3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700412"
---
# <span data-ttu-id="8d2bb-101">New-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="8d2bb-101">New-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="8d2bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d2bb-102">SYNOPSIS</span></span>
<span data-ttu-id="8d2bb-103">응용 프로그램 게이트웨이 방화벽 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-103">Creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="8d2bb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8d2bb-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d2bb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8d2bb-105">DESCRIPTION</span></span>
<span data-ttu-id="8d2bb-106">**새 AzApplicationGatewayFirewallPolicy** cmdlet은 응용 프로그램 게이트웨이 방화벽 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-106">The **New-AzApplicationGatewayFirewallPolicy** cmdlet creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="8d2bb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8d2bb-107">EXAMPLES</span></span>

### <span data-ttu-id="8d2bb-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8d2bb-108">Example 1</span></span>
```powershell
PS C:\> $firewallPolicy = New-AzureRmApplicationGatewayFirewallPolicy -Name wafResource1 -ResourceGroupName "rg1"  -Location  "westus" -CustomRules $customRule
```

<span data-ttu-id="8d2bb-109">이 명령은 $customRule 변수에 정의 된 사용자 지정 규칙이 있는 "westus" 리소스 그룹 "rg1"에 "wafResource1" 이라는 새 Azure application gateway 방화벽 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-109">This command creates a new Azure application gateway firewall policy named "wafResource1" in resource group "rg1" in location "westus" with custom rules defined in the $customRule variable</span></span>

## <span data-ttu-id="8d2bb-110">변수</span><span class="sxs-lookup"><span data-stu-id="8d2bb-110">PARAMETERS</span></span>

### <span data-ttu-id="8d2bb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d2bb-111">-AsJob</span></span>
<span data-ttu-id="8d2bb-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="8d2bb-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8d2bb-113">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="8d2bb-113">-CustomRule</span></span>
<span data-ttu-id="8d2bb-114">CustomRules 목록</span><span class="sxs-lookup"><span data-stu-id="8d2bb-114">The list of CustomRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d2bb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d2bb-115">-DefaultProfile</span></span>
<span data-ttu-id="8d2bb-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d2bb-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8d2bb-117">-Force</span></span>
<span data-ttu-id="8d2bb-118">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="8d2bb-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="8d2bb-119">-위치</span><span class="sxs-lookup"><span data-stu-id="8d2bb-119">-Location</span></span>
<span data-ttu-id="8d2bb-120">location.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-120">location.</span></span>

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

### <span data-ttu-id="8d2bb-121">-이름</span><span class="sxs-lookup"><span data-stu-id="8d2bb-121">-Name</span></span>
<span data-ttu-id="8d2bb-122">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-122">The resource name.</span></span>

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

### <span data-ttu-id="8d2bb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d2bb-123">-ResourceGroupName</span></span>
<span data-ttu-id="8d2bb-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-124">The resource group name.</span></span>

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

### <span data-ttu-id="8d2bb-125">태그</span><span class="sxs-lookup"><span data-stu-id="8d2bb-125">-Tag</span></span>
<span data-ttu-id="8d2bb-126">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="8d2bb-127">-확인</span><span class="sxs-lookup"><span data-stu-id="8d2bb-127">-Confirm</span></span>
<span data-ttu-id="8d2bb-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2bb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d2bb-129">-WhatIf</span></span>
<span data-ttu-id="8d2bb-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d2bb-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2bb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d2bb-132">CommonParameters</span></span>
<span data-ttu-id="8d2bb-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d2bb-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d2bb-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d2bb-135">입력</span><span class="sxs-lookup"><span data-stu-id="8d2bb-135">INPUTS</span></span>

### <span data-ttu-id="8d2bb-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8d2bb-136">System.String</span></span>

### <span data-ttu-id="8d2bb-137">PSApplicationGatewayFirewallCustomRule [] (으)로</span><span class="sxs-lookup"><span data-stu-id="8d2bb-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span></span>

### <span data-ttu-id="8d2bb-138">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="8d2bb-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8d2bb-139">출력</span><span class="sxs-lookup"><span data-stu-id="8d2bb-139">OUTPUTS</span></span>

### <span data-ttu-id="8d2bb-140">PSApplicationGatewayWebApplicationFirewallPolicy에 대 한.</span><span class="sxs-lookup"><span data-stu-id="8d2bb-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="8d2bb-141">상속자</span><span class="sxs-lookup"><span data-stu-id="8d2bb-141">NOTES</span></span>

## <span data-ttu-id="8d2bb-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8d2bb-142">RELATED LINKS</span></span>
