---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallhubpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
ms.openlocfilehash: fc60a983e06e632912e43291f7b60980ff34a8cd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214858"
---
# <span data-ttu-id="14670-101">New-AzFirewallHubPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="14670-101">New-AzFirewallHubPublicIpAddress</span></span>

## <span data-ttu-id="14670-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14670-102">SYNOPSIS</span></span>
<span data-ttu-id="14670-103">가상 허브의 방화벽에 대 한 공용 Ip assoicated</span><span class="sxs-lookup"><span data-stu-id="14670-103">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="14670-104">구문과</span><span class="sxs-lookup"><span data-stu-id="14670-104">SYNTAX</span></span>

```
New-AzFirewallHubPublicIpAddress [-Count <Int32>] [-Addresses <PSAzureFirewallPublicIpAddress[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14670-105">설명은</span><span class="sxs-lookup"><span data-stu-id="14670-105">DESCRIPTION</span></span>
<span data-ttu-id="14670-106">가상 허브의 방화벽에 대 한 공용 Ip assoicated</span><span class="sxs-lookup"><span data-stu-id="14670-106">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="14670-107">예제의</span><span class="sxs-lookup"><span data-stu-id="14670-107">EXAMPLES</span></span>

### <span data-ttu-id="14670-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="14670-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallHubPublicIpAddress -Count 2
```

<span data-ttu-id="14670-109">이렇게 하면 가상 허브에 연결 된 방화벽에 2 개의 공용 ip가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="14670-109">This will create 2 public ips on the firewall attached to the virtual hub.</span></span> <span data-ttu-id="14670-110">이렇게 하면 백 엔드에 ip 주소가 만들어집니다. 새 방화벽에 대해 ipaddresses를 명시적으로 제공할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="14670-110">This will create the ip address in the backend.We cannot provide the ipaddresses explicitly for a new firewall.</span></span>

### <span data-ttu-id="14670-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="14670-111">Example 2</span></span>
```powershell
PS C:\> $publicIp1 = New-AzFirewallPublicIpAddress -Address 10.2.3.4
PS C:\> $publicIp2 = New-AzFirewallPublicIpAddress -Address 20.56.37.46
PS C:\> New-AzFirewallHubPublicIpAddress -Count 3 -Addresses $publicIp1, $publicIp2
```

<span data-ttu-id="14670-112">이렇게 하면 방화벽에 이미 존재 하는 $publicIp 1 $publicIp 2)를 유지 하 여 방화벽에 새 공용 ip가 1 개 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="14670-112">This will create 1 new public ip on the firewall by retain $publicIp1, $publicIp2 which are already exist on the firewall.</span></span>

## <span data-ttu-id="14670-113">변수</span><span class="sxs-lookup"><span data-stu-id="14670-113">PARAMETERS</span></span>

### <span data-ttu-id="14670-114">-주소</span><span class="sxs-lookup"><span data-stu-id="14670-114">-Addresses</span></span>
<span data-ttu-id="14670-115">허브에 연결 된 방화벽의 공용 IP 주소</span><span class="sxs-lookup"><span data-stu-id="14670-115">The Public IP Addresses of the Firewall attached to a hub</span></span>

```yaml
Type: PSAzureFirewallPublicIpAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14670-116">-카운트</span><span class="sxs-lookup"><span data-stu-id="14670-116">-Count</span></span>
<span data-ttu-id="14670-117">공용 Ip 주소 수</span><span class="sxs-lookup"><span data-stu-id="14670-117">The count of public Ip addresses</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14670-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14670-118">-DefaultProfile</span></span>
<span data-ttu-id="14670-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="14670-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14670-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14670-120">CommonParameters</span></span>
<span data-ttu-id="14670-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="14670-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14670-122">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="14670-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14670-123">입력</span><span class="sxs-lookup"><span data-stu-id="14670-123">INPUTS</span></span>

### <span data-ttu-id="14670-124">않아야</span><span class="sxs-lookup"><span data-stu-id="14670-124">None</span></span>

## <span data-ttu-id="14670-125">출력</span><span class="sxs-lookup"><span data-stu-id="14670-125">OUTPUTS</span></span>

### <span data-ttu-id="14670-126">PSAzureFirewallHubPublicIpAddresses에 대 한.</span><span class="sxs-lookup"><span data-stu-id="14670-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubPublicIpAddresses</span></span>

## <span data-ttu-id="14670-127">상속자</span><span class="sxs-lookup"><span data-stu-id="14670-127">NOTES</span></span>

## <span data-ttu-id="14670-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14670-128">RELATED LINKS</span></span>
