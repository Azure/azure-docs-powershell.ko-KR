---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallexclusionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallExclusionConfig.md
ms.openlocfilehash: 370965325a265ef4c2b7fa5e0070ae705099e2c8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215979"
---
# <span data-ttu-id="11057-101">New-AzApplicationGatewayFirewallExclusionConfig</span><span class="sxs-lookup"><span data-stu-id="11057-101">New-AzApplicationGatewayFirewallExclusionConfig</span></span>

## <span data-ttu-id="11057-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11057-102">SYNOPSIS</span></span>
<span data-ttu-id="11057-103">Application gateway waf에 대 한 새 제외 규칙 목록 만들기</span><span class="sxs-lookup"><span data-stu-id="11057-103">Creates a new exclusion rule list for application gateway waf</span></span>

## <span data-ttu-id="11057-104">구문과</span><span class="sxs-lookup"><span data-stu-id="11057-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallExclusionConfig -Variable <String> -Operator <String> -Selector <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11057-105">설명은</span><span class="sxs-lookup"><span data-stu-id="11057-105">DESCRIPTION</span></span>
<span data-ttu-id="11057-106">**AzApplicationGatewayFirewallExclusionConfig** cmdlet은 application gateway waf에 대 한 새 제외 규칙 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="11057-106">The **New-AzApplicationGatewayFirewallExclusionConfig** cmdlet a new exclusion rule list for application gateway waf.</span></span>

## <span data-ttu-id="11057-107">예제의</span><span class="sxs-lookup"><span data-stu-id="11057-107">EXAMPLES</span></span>

### <span data-ttu-id="11057-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="11057-108">Example 1</span></span>
```powershell
PS C:\> $exclusion1 = New-AzApplicationGatewayFirewallExclusionConfig -Variable "RequestHeaderNames" -Operator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="11057-109">이 명령은 새 제외 규칙을 만들고 xyz 라는 RequestHeaderNames 및 StartsWith 이라는 변수에 대 한 구성을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="11057-109">This command creates a new exclusion rule lists configuration for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="11057-110">제외 목록 구성은 $exclusion 1에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11057-110">The exclusion list configuration is saved in $exclusion1.</span></span>

## <span data-ttu-id="11057-111">변수</span><span class="sxs-lookup"><span data-stu-id="11057-111">PARAMETERS</span></span>

### <span data-ttu-id="11057-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11057-112">-DefaultProfile</span></span>
<span data-ttu-id="11057-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="11057-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11057-114">-연산자</span><span class="sxs-lookup"><span data-stu-id="11057-114">-Operator</span></span>
<span data-ttu-id="11057-115">변수가 컬렉션인 경우 선택기에 대해 작업을 수행 하 여이 제외를 적용할 컬렉션의 요소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11057-115">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11057-116">-선택기</span><span class="sxs-lookup"><span data-stu-id="11057-116">-Selector</span></span>
<span data-ttu-id="11057-117">Variable 변수는 collection이 고이 제외를 적용할 컬렉션의 요소를 지정 하는 데 사용 되는 연산자입니다.</span><span class="sxs-lookup"><span data-stu-id="11057-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11057-118">-변수</span><span class="sxs-lookup"><span data-stu-id="11057-118">-Variable</span></span>
<span data-ttu-id="11057-119">제외할 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="11057-119">The variable to be excluded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11057-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11057-120">CommonParameters</span></span>
<span data-ttu-id="11057-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="11057-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11057-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11057-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11057-123">입력</span><span class="sxs-lookup"><span data-stu-id="11057-123">INPUTS</span></span>

### <span data-ttu-id="11057-124">않아야</span><span class="sxs-lookup"><span data-stu-id="11057-124">None</span></span>

## <span data-ttu-id="11057-125">출력</span><span class="sxs-lookup"><span data-stu-id="11057-125">OUTPUTS</span></span>

### <span data-ttu-id="11057-126">PSApplicationGatewayFirewallExclusion에 대 한.</span><span class="sxs-lookup"><span data-stu-id="11057-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span></span>

## <span data-ttu-id="11057-127">상속자</span><span class="sxs-lookup"><span data-stu-id="11057-127">NOTES</span></span>

## <span data-ttu-id="11057-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11057-128">RELATED LINKS</span></span>
