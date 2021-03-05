---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 2d7bdd9a1669859f0bcd650577ed3169a0aeea2e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992553"
---
# <span data-ttu-id="16ebd-101">Remove-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="16ebd-101">Remove-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="16ebd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16ebd-102">SYNOPSIS</span></span>
<span data-ttu-id="16ebd-103">애플리케이션 게이트웨이 방화벽 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="16ebd-103">Removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="16ebd-104">구문</span><span class="sxs-lookup"><span data-stu-id="16ebd-104">SYNTAX</span></span>

### <span data-ttu-id="16ebd-105">ByFactoryName(기본값)</span><span class="sxs-lookup"><span data-stu-id="16ebd-105">ByFactoryName (Default)</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16ebd-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="16ebd-106">ByFactoryObject</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16ebd-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="16ebd-107">ByResourceId</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16ebd-108">설명</span><span class="sxs-lookup"><span data-stu-id="16ebd-108">DESCRIPTION</span></span>
<span data-ttu-id="16ebd-109">**Remove-AzApplicationGatewayFirewallPolicy** cmdlet은 애플리케이션 게이트웨이 방화벽 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="16ebd-109">The **Remove-AzApplicationGatewayFirewallPolicy** cmdlet removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="16ebd-110">예제</span><span class="sxs-lookup"><span data-stu-id="16ebd-110">EXAMPLES</span></span>

### <span data-ttu-id="16ebd-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="16ebd-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzApplicationGatewayFirewallPolicy -Name "ApplicationGatewayFirewallPolicy01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="16ebd-112">이 명령은 ResourceGroup01이라는 리소스 그룹에서 ApplicationGatewayFirewallPolicy01이라는 애플리케이션 게이트웨이 방화벽 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="16ebd-112">This command removes the application gateway firewall policy named ApplicationGatewayFirewallPolicy01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="16ebd-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="16ebd-113">PARAMETERS</span></span>

### <span data-ttu-id="16ebd-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16ebd-114">-AsJob</span></span>
<span data-ttu-id="16ebd-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="16ebd-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="16ebd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16ebd-116">-DefaultProfile</span></span>
<span data-ttu-id="16ebd-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="16ebd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16ebd-118">-Force</span><span class="sxs-lookup"><span data-stu-id="16ebd-118">-Force</span></span>
<span data-ttu-id="16ebd-119">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16ebd-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="16ebd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16ebd-120">-InputObject</span></span>
<span data-ttu-id="16ebd-121">방화벽 정책 개체</span><span class="sxs-lookup"><span data-stu-id="16ebd-121">The firewall policy object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16ebd-122">-Name</span><span class="sxs-lookup"><span data-stu-id="16ebd-122">-Name</span></span>
<span data-ttu-id="16ebd-123">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16ebd-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16ebd-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16ebd-124">-PassThru</span></span>
<span data-ttu-id="16ebd-125">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="16ebd-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="16ebd-126">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16ebd-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="16ebd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16ebd-127">-ResourceGroupName</span></span>
<span data-ttu-id="16ebd-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16ebd-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16ebd-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16ebd-129">-ResourceId</span></span>
<span data-ttu-id="16ebd-130">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="16ebd-130">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16ebd-131">-확인</span><span class="sxs-lookup"><span data-stu-id="16ebd-131">-Confirm</span></span>
<span data-ttu-id="16ebd-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="16ebd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16ebd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16ebd-133">-WhatIf</span></span>
<span data-ttu-id="16ebd-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="16ebd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16ebd-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16ebd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16ebd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16ebd-136">CommonParameters</span></span>
<span data-ttu-id="16ebd-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="16ebd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16ebd-138">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="16ebd-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16ebd-139">입력</span><span class="sxs-lookup"><span data-stu-id="16ebd-139">INPUTS</span></span>

### <span data-ttu-id="16ebd-140">System.String</span><span class="sxs-lookup"><span data-stu-id="16ebd-140">System.String</span></span>

## <span data-ttu-id="16ebd-141">출력</span><span class="sxs-lookup"><span data-stu-id="16ebd-141">OUTPUTS</span></span>

### <span data-ttu-id="16ebd-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="16ebd-142">System.Boolean</span></span>

## <span data-ttu-id="16ebd-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="16ebd-143">NOTES</span></span>

## <span data-ttu-id="16ebd-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16ebd-144">RELATED LINKS</span></span>
