---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
ms.openlocfilehash: f53733976d946b61fc143e0a2b2e9be71017b7f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310865"
---
# <span data-ttu-id="473de-101">Get-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="473de-101">Get-AzFirewallPolicy</span></span>

## <span data-ttu-id="473de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="473de-102">SYNOPSIS</span></span>
<span data-ttu-id="473de-103">Azure 방화벽 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="473de-103">Gets a Azure Firewall Policy</span></span>

## <span data-ttu-id="473de-104">구문과</span><span class="sxs-lookup"><span data-stu-id="473de-104">SYNTAX</span></span>

### <span data-ttu-id="473de-105">GetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="473de-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="473de-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="473de-106">GetByResourceIdParameterSet</span></span>
```
Get-AzFirewallPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="473de-107">설명은</span><span class="sxs-lookup"><span data-stu-id="473de-107">DESCRIPTION</span></span>
<span data-ttu-id="473de-108">**AzFirewallPolicy** cmdlet은 리소스 그룹에서 하나 이상의 방화벽을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="473de-108">The **Get-AzFirewallPolicy** cmdlet gets one or more Firewalls in a resource group</span></span>

## <span data-ttu-id="473de-109">예제의</span><span class="sxs-lookup"><span data-stu-id="473de-109">EXAMPLES</span></span>

### <span data-ttu-id="473de-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="473de-110">Example 1</span></span>
```powershell
PS C:\> Get-AzFirewallPolicy -Name firwallPolicy -ResourceGroupName TestRg
```

<span data-ttu-id="473de-111">이 예제에서는 리소스 그룹 "TestRg"에 "firewallPolicy" 이라는 방화벽 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="473de-111">This example get a firewall policy named "firewallPolicy" in the resource group "TestRg"</span></span>

## <span data-ttu-id="473de-112">변수</span><span class="sxs-lookup"><span data-stu-id="473de-112">PARAMETERS</span></span>

### <span data-ttu-id="473de-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="473de-113">-DefaultProfile</span></span>
<span data-ttu-id="473de-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="473de-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="473de-115">-이름</span><span class="sxs-lookup"><span data-stu-id="473de-115">-Name</span></span>
<span data-ttu-id="473de-116">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="473de-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="473de-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="473de-117">-ResourceGroupName</span></span>
<span data-ttu-id="473de-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="473de-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="473de-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="473de-119">-ResourceId</span></span>
<span data-ttu-id="473de-120">리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="473de-120">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="473de-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="473de-121">CommonParameters</span></span>
<span data-ttu-id="473de-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="473de-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="473de-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="473de-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="473de-124">입력</span><span class="sxs-lookup"><span data-stu-id="473de-124">INPUTS</span></span>

### <span data-ttu-id="473de-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="473de-125">System.String</span></span>

## <span data-ttu-id="473de-126">출력</span><span class="sxs-lookup"><span data-stu-id="473de-126">OUTPUTS</span></span>

### <span data-ttu-id="473de-127">Microsoft. \* PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="473de-127">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="473de-128">1.12.0.0 ' 1 [[Microsoft Azure.]. 모델에 대 한 PSAzureFirewall, Microsoft Azure. PowerShell. t e t-네트워크, 버전 =, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="473de-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="473de-129">상속자</span><span class="sxs-lookup"><span data-stu-id="473de-129">NOTES</span></span>

## <span data-ttu-id="473de-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="473de-130">RELATED LINKS</span></span>
