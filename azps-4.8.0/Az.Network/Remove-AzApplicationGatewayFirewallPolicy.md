---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 18795b91b6dfe25b64946587dc9199078c4cd727
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056173"
---
# <span data-ttu-id="01beb-101">Remove-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="01beb-101">Remove-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="01beb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01beb-102">SYNOPSIS</span></span>
<span data-ttu-id="01beb-103">응용 프로그램 게이트웨이 방화벽 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="01beb-103">Removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="01beb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="01beb-104">SYNTAX</span></span>

### <span data-ttu-id="01beb-105">ByFactoryName (기본값)</span><span class="sxs-lookup"><span data-stu-id="01beb-105">ByFactoryName (Default)</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01beb-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="01beb-106">ByFactoryObject</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01beb-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="01beb-107">ByResourceId</span></span>
```
Remove-AzApplicationGatewayFirewallPolicy -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01beb-108">설명은</span><span class="sxs-lookup"><span data-stu-id="01beb-108">DESCRIPTION</span></span>
<span data-ttu-id="01beb-109">**AzApplicationGatewayFirewallPolicy** cmdlet은 응용 프로그램 게이트웨이 방화벽 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="01beb-109">The **Remove-AzApplicationGatewayFirewallPolicy** cmdlet removes an application gateway firewall policy.</span></span>

## <span data-ttu-id="01beb-110">예제의</span><span class="sxs-lookup"><span data-stu-id="01beb-110">EXAMPLES</span></span>

### <span data-ttu-id="01beb-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="01beb-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzApplicationGatewayFirewallPolicy -Name "ApplicationGatewayFirewallPolicy01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="01beb-112">이 명령은 ResourceGroup01 이라는 리소스 그룹에서 ApplicationGatewayFirewallPolicy01 이라는 응용 프로그램 게이트웨이 방화벽 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="01beb-112">This command removes the application gateway firewall policy named ApplicationGatewayFirewallPolicy01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="01beb-113">변수</span><span class="sxs-lookup"><span data-stu-id="01beb-113">PARAMETERS</span></span>

### <span data-ttu-id="01beb-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01beb-114">-AsJob</span></span>
<span data-ttu-id="01beb-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="01beb-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="01beb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01beb-116">-DefaultProfile</span></span>
<span data-ttu-id="01beb-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="01beb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01beb-118">-Force</span><span class="sxs-lookup"><span data-stu-id="01beb-118">-Force</span></span>
<span data-ttu-id="01beb-119">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01beb-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="01beb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01beb-120">-InputObject</span></span>
<span data-ttu-id="01beb-121">방화벽 정책 개체</span><span class="sxs-lookup"><span data-stu-id="01beb-121">The firewall policy object</span></span>

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

### <span data-ttu-id="01beb-122">-이름</span><span class="sxs-lookup"><span data-stu-id="01beb-122">-Name</span></span>
<span data-ttu-id="01beb-123">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="01beb-123">The resource name.</span></span>

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

### <span data-ttu-id="01beb-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01beb-124">-PassThru</span></span>
<span data-ttu-id="01beb-125">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="01beb-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="01beb-126">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01beb-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="01beb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01beb-127">-ResourceGroupName</span></span>
<span data-ttu-id="01beb-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="01beb-128">The resource group name.</span></span>

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

### <span data-ttu-id="01beb-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01beb-129">-ResourceId</span></span>
<span data-ttu-id="01beb-130">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="01beb-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="01beb-131">-확인</span><span class="sxs-lookup"><span data-stu-id="01beb-131">-Confirm</span></span>
<span data-ttu-id="01beb-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="01beb-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01beb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01beb-133">-WhatIf</span></span>
<span data-ttu-id="01beb-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="01beb-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01beb-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01beb-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01beb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01beb-136">CommonParameters</span></span>
<span data-ttu-id="01beb-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="01beb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01beb-138">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01beb-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01beb-139">입력</span><span class="sxs-lookup"><span data-stu-id="01beb-139">INPUTS</span></span>

### <span data-ttu-id="01beb-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="01beb-140">System.String</span></span>

## <span data-ttu-id="01beb-141">출력</span><span class="sxs-lookup"><span data-stu-id="01beb-141">OUTPUTS</span></span>

### <span data-ttu-id="01beb-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="01beb-142">System.Boolean</span></span>

## <span data-ttu-id="01beb-143">상속자</span><span class="sxs-lookup"><span data-stu-id="01beb-143">NOTES</span></span>

## <span data-ttu-id="01beb-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="01beb-144">RELATED LINKS</span></span>
