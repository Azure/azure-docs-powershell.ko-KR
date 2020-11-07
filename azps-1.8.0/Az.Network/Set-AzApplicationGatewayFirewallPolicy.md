---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 3442c5a16493d42dbbfd6460f398b37bb92d6d72
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700060"
---
# <span data-ttu-id="4f863-101">Set-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="4f863-101">Set-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="4f863-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f863-102">SYNOPSIS</span></span>
<span data-ttu-id="4f863-103">응용 프로그램 게이트웨이 방화벽 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f863-103">Updates an application gateway firewall policy.</span></span>

## <span data-ttu-id="4f863-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4f863-104">SYNTAX</span></span>

### <span data-ttu-id="4f863-105">ByFactoryObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="4f863-105">ByFactoryObject (Default)</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4f863-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="4f863-106">ByFactoryName</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4f863-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4f863-107">ByResourceId</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -ResourceId <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4f863-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4f863-108">DESCRIPTION</span></span>
<span data-ttu-id="4f863-109">**AzApplicationGatewayFirewallPolicy** Cmdlet은 Azure application gateway 방화벽 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f863-109">The **Set-AzApplicationGatewayFirewallPolicy** cmdlet updates an Azure application gateway firewall policy.</span></span>

## <span data-ttu-id="4f863-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4f863-110">EXAMPLES</span></span>

### <span data-ttu-id="4f863-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4f863-111">Example 1</span></span>
```powershell
PS C:\> $UpdatedAppGwFirewallPolicy = Set-AzApplicationGatewayFirewallPolicy -ApplicationGateway $AppGwFirewallPolicy
```

<span data-ttu-id="4f863-112">이 명령은 $AppGwFirewallPolicy 변수의 설정을 사용 하 여 응용 프로그램 게이트웨이 방화벽 정책을 업데이트 하 고 업데이트 된 게이트웨이를 $UpdatedAppGwFirewallPolicy 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f863-112">This command updates the application gateway firewall policy with settings in the $AppGwFirewallPolicy variable and stores the updated gateway in the $UpdatedAppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="4f863-113">변수</span><span class="sxs-lookup"><span data-stu-id="4f863-113">PARAMETERS</span></span>

### <span data-ttu-id="4f863-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4f863-114">-AsJob</span></span>
<span data-ttu-id="4f863-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4f863-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4f863-116">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="4f863-116">-CustomRule</span></span>
<span data-ttu-id="4f863-117">CustomRules 목록</span><span class="sxs-lookup"><span data-stu-id="4f863-117">The list of CustomRules</span></span>

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

### <span data-ttu-id="4f863-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f863-118">-DefaultProfile</span></span>
<span data-ttu-id="4f863-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4f863-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f863-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f863-120">-InputObject</span></span>
<span data-ttu-id="4f863-121">ApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="4f863-121">The applicationGatewayFirewallPolicy</span></span>

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

### <span data-ttu-id="4f863-122">-이름</span><span class="sxs-lookup"><span data-stu-id="4f863-122">-Name</span></span>
<span data-ttu-id="4f863-123">방화벽 정책 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f863-123">The Firewall Policy Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f863-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f863-124">-ResourceGroupName</span></span>
<span data-ttu-id="4f863-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f863-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f863-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f863-126">-ResourceId</span></span>
<span data-ttu-id="4f863-127">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4f863-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="4f863-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f863-128">CommonParameters</span></span>
<span data-ttu-id="4f863-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f863-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f863-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f863-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f863-131">입력</span><span class="sxs-lookup"><span data-stu-id="4f863-131">INPUTS</span></span>

### <span data-ttu-id="4f863-132">PSApplicationGatewayWebApplicationFirewallPolicy에 대 한.</span><span class="sxs-lookup"><span data-stu-id="4f863-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="4f863-133">출력</span><span class="sxs-lookup"><span data-stu-id="4f863-133">OUTPUTS</span></span>

### <span data-ttu-id="4f863-134">PSApplicationGatewayWebApplicationFirewallPolicy에 대 한.</span><span class="sxs-lookup"><span data-stu-id="4f863-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="4f863-135">상속자</span><span class="sxs-lookup"><span data-stu-id="4f863-135">NOTES</span></span>

## <span data-ttu-id="4f863-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4f863-136">RELATED LINKS</span></span>
