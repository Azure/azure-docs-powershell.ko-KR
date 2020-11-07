---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
ms.openlocfilehash: 0bccee6b8242e3480ad405837f9c2a661eb97431
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700368"
---
# <span data-ttu-id="88d4b-101">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="88d4b-101">New-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="88d4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88d4b-102">SYNOPSIS</span></span>
<span data-ttu-id="88d4b-103">응용 프로그램 보안 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="88d4b-103">Creates an application security group.</span></span>

## <span data-ttu-id="88d4b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="88d4b-104">SYNTAX</span></span>

```
New-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88d4b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="88d4b-105">DESCRIPTION</span></span>
<span data-ttu-id="88d4b-106">**AzApplicationSecurityGroup** cmdlet은 응용 프로그램 보안 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="88d4b-106">The **New-AzApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="88d4b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="88d4b-107">EXAMPLES</span></span>

### <span data-ttu-id="88d4b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="88d4b-108">Example 1</span></span>
```
PS C:\> New-AzApplicationSecurityGroup -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="88d4b-109">이 예제에서는 연결이 없는 응용 프로그램 보안 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="88d4b-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="88d4b-110">생성 된 네트워크 인터페이스의 IP 구성은 그룹에 포함 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88d4b-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="88d4b-111">또한 보안 규칙은 그룹을 원본 또는 대상으로 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88d4b-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="88d4b-112">변수</span><span class="sxs-lookup"><span data-stu-id="88d4b-112">PARAMETERS</span></span>

### <span data-ttu-id="88d4b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88d4b-113">-AsJob</span></span>
<span data-ttu-id="88d4b-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="88d4b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="88d4b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88d4b-115">-DefaultProfile</span></span>
<span data-ttu-id="88d4b-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="88d4b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88d4b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="88d4b-117">-Force</span></span>
<span data-ttu-id="88d4b-118">리소스를 덮어쓰려고 하는 경우 확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="88d4b-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="88d4b-119">-위치</span><span class="sxs-lookup"><span data-stu-id="88d4b-119">-Location</span></span>
<span data-ttu-id="88d4b-120">위치입니다.</span><span class="sxs-lookup"><span data-stu-id="88d4b-120">The location.</span></span>

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

### <span data-ttu-id="88d4b-121">-이름</span><span class="sxs-lookup"><span data-stu-id="88d4b-121">-Name</span></span>
<span data-ttu-id="88d4b-122">응용 프로그램 보안 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88d4b-122">The name of the application security group.</span></span>

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

### <span data-ttu-id="88d4b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88d4b-123">-ResourceGroupName</span></span>
<span data-ttu-id="88d4b-124">응용 프로그램 보안 그룹의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88d4b-124">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="88d4b-125">태그</span><span class="sxs-lookup"><span data-stu-id="88d4b-125">-Tag</span></span>
<span data-ttu-id="88d4b-126">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="88d4b-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="88d4b-127">-확인</span><span class="sxs-lookup"><span data-stu-id="88d4b-127">-Confirm</span></span>
<span data-ttu-id="88d4b-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="88d4b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88d4b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88d4b-129">-WhatIf</span></span>
<span data-ttu-id="88d4b-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="88d4b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88d4b-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="88d4b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88d4b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88d4b-132">CommonParameters</span></span>
<span data-ttu-id="88d4b-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="88d4b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88d4b-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88d4b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88d4b-135">입력</span><span class="sxs-lookup"><span data-stu-id="88d4b-135">INPUTS</span></span>

### <span data-ttu-id="88d4b-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="88d4b-136">System.String</span></span>

### <span data-ttu-id="88d4b-137">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="88d4b-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="88d4b-138">출력</span><span class="sxs-lookup"><span data-stu-id="88d4b-138">OUTPUTS</span></span>

### <span data-ttu-id="88d4b-139">Microsoft. \* PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="88d4b-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="88d4b-140">상속자</span><span class="sxs-lookup"><span data-stu-id="88d4b-140">NOTES</span></span>

## <span data-ttu-id="88d4b-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88d4b-141">RELATED LINKS</span></span>

[<span data-ttu-id="88d4b-142">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="88d4b-142">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)

[<span data-ttu-id="88d4b-143">제거-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="88d4b-143">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="88d4b-144">새로운 AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="88d4b-144">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="88d4b-145">추가-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="88d4b-145">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="88d4b-146">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="88d4b-146">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="88d4b-147">새로운 AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="88d4b-147">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="88d4b-148">추가-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="88d4b-148">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="88d4b-149">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="88d4b-149">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
