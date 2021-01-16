---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
ms.openlocfilehash: 32d7767ac5bd43be8fb9a3129966a0a88d761953
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491059"
---
# <span data-ttu-id="a3b66-101">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a3b66-101">New-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="a3b66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3b66-102">SYNOPSIS</span></span>
<span data-ttu-id="a3b66-103">애플리케이션 보안 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a3b66-103">Creates an application security group.</span></span>

## <span data-ttu-id="a3b66-104">구문</span><span class="sxs-lookup"><span data-stu-id="a3b66-104">SYNTAX</span></span>

```
New-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3b66-105">설명</span><span class="sxs-lookup"><span data-stu-id="a3b66-105">DESCRIPTION</span></span>
<span data-ttu-id="a3b66-106">**New-AzApplicationSecurityGroup** cmdlet은 애플리케이션 보안 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a3b66-106">The **New-AzApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="a3b66-107">예제</span><span class="sxs-lookup"><span data-stu-id="a3b66-107">EXAMPLES</span></span>

### <span data-ttu-id="a3b66-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a3b66-108">Example 1</span></span>
```
PS C:\> New-AzApplicationSecurityGroup -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="a3b66-109">이 예제에서는 연결 없는 애플리케이션 보안 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a3b66-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="a3b66-110">생성되면 네트워크 인터페이스의 IP 구성을 그룹에 포함될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3b66-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="a3b66-111">보안 규칙은 그룹을 해당 원본 또는 대상으로 참조할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3b66-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="a3b66-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3b66-112">PARAMETERS</span></span>

### <span data-ttu-id="a3b66-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3b66-113">-AsJob</span></span>
<span data-ttu-id="a3b66-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a3b66-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3b66-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3b66-115">-DefaultProfile</span></span>
<span data-ttu-id="a3b66-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a3b66-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3b66-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a3b66-117">-Force</span></span>
<span data-ttu-id="a3b66-118">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a3b66-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="a3b66-119">-Location</span><span class="sxs-lookup"><span data-stu-id="a3b66-119">-Location</span></span>
<span data-ttu-id="a3b66-120">위치입니다.</span><span class="sxs-lookup"><span data-stu-id="a3b66-120">The location.</span></span>

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

### <span data-ttu-id="a3b66-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a3b66-121">-Name</span></span>
<span data-ttu-id="a3b66-122">애플리케이션 보안 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a3b66-122">The name of the application security group.</span></span>

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

### <span data-ttu-id="a3b66-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3b66-123">-ResourceGroupName</span></span>
<span data-ttu-id="a3b66-124">애플리케이션 보안 그룹의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a3b66-124">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="a3b66-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="a3b66-125">-Tag</span></span>
<span data-ttu-id="a3b66-126">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="a3b66-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="a3b66-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3b66-127">-Confirm</span></span>
<span data-ttu-id="a3b66-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3b66-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3b66-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3b66-129">-WhatIf</span></span>
<span data-ttu-id="a3b66-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a3b66-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3b66-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a3b66-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3b66-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3b66-132">CommonParameters</span></span>
<span data-ttu-id="a3b66-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a3b66-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3b66-134">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a3b66-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3b66-135">입력</span><span class="sxs-lookup"><span data-stu-id="a3b66-135">INPUTS</span></span>

### <span data-ttu-id="a3b66-136">System.String</span><span class="sxs-lookup"><span data-stu-id="a3b66-136">System.String</span></span>

### <span data-ttu-id="a3b66-137">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a3b66-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a3b66-138">출력</span><span class="sxs-lookup"><span data-stu-id="a3b66-138">OUTPUTS</span></span>

### <span data-ttu-id="a3b66-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a3b66-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="a3b66-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a3b66-140">NOTES</span></span>

## <span data-ttu-id="a3b66-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a3b66-141">RELATED LINKS</span></span>

[<span data-ttu-id="a3b66-142">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a3b66-142">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)

[<span data-ttu-id="a3b66-143">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a3b66-143">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="a3b66-144">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a3b66-144">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="a3b66-145">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a3b66-145">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="a3b66-146">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a3b66-146">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="a3b66-147">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a3b66-147">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="a3b66-148">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a3b66-148">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="a3b66-149">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a3b66-149">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
