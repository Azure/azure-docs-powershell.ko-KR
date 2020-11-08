---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
ms.openlocfilehash: c4bc5e9fcc7d0ca405a8031af29d16283f963ad2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211585"
---
# <span data-ttu-id="7d618-101">New-AzFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7d618-101">New-AzFirewallPublicIpAddress</span></span>

## <span data-ttu-id="7d618-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d618-102">SYNOPSIS</span></span>
<span data-ttu-id="7d618-103">Azure 방화벽에서 다중 pip에 사용할 수 있는 Ip 주소의 자리 표시자입니다.</span><span class="sxs-lookup"><span data-stu-id="7d618-103">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="7d618-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7d618-104">SYNTAX</span></span>

```
New-AzFirewallPublicIpAddress [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d618-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7d618-105">DESCRIPTION</span></span>
<span data-ttu-id="7d618-106">Azure 방화벽에서 다중 pip에 사용할 수 있는 Ip 주소의 자리 표시자입니다.</span><span class="sxs-lookup"><span data-stu-id="7d618-106">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="7d618-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7d618-107">EXAMPLES</span></span>

### <span data-ttu-id="7d618-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7d618-108">Example 1</span></span>
```powershell
PS C:\> $publicIp = New-AzFirewallPublicIpAddress -Address 20.2.3.4
```

<span data-ttu-id="7d618-109">$publicIp는 ip 주소 20.2.3.4의 자리 표시자입니다.</span><span class="sxs-lookup"><span data-stu-id="7d618-109">$publicIp will be the placeholder for the ip address 20.2.3.4</span></span>

## <span data-ttu-id="7d618-110">변수</span><span class="sxs-lookup"><span data-stu-id="7d618-110">PARAMETERS</span></span>

### <span data-ttu-id="7d618-111">-주소</span><span class="sxs-lookup"><span data-stu-id="7d618-111">-Address</span></span>
<span data-ttu-id="7d618-112">허브에 연결 된 방화벽의 IP 주소</span><span class="sxs-lookup"><span data-stu-id="7d618-112">The IP Addresses of the Firewall attached to a hub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d618-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d618-113">-DefaultProfile</span></span>
<span data-ttu-id="7d618-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7d618-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d618-115">-확인</span><span class="sxs-lookup"><span data-stu-id="7d618-115">-Confirm</span></span>
<span data-ttu-id="7d618-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d618-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d618-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d618-117">-WhatIf</span></span>
<span data-ttu-id="7d618-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7d618-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7d618-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7d618-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d618-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d618-120">CommonParameters</span></span>
<span data-ttu-id="7d618-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d618-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d618-122">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7d618-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d618-123">입력</span><span class="sxs-lookup"><span data-stu-id="7d618-123">INPUTS</span></span>

### <span data-ttu-id="7d618-124">않아야</span><span class="sxs-lookup"><span data-stu-id="7d618-124">None</span></span>

## <span data-ttu-id="7d618-125">출력</span><span class="sxs-lookup"><span data-stu-id="7d618-125">OUTPUTS</span></span>

### <span data-ttu-id="7d618-126">PSAzureFirewallPublicIpAddress에 대 한.</span><span class="sxs-lookup"><span data-stu-id="7d618-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPublicIpAddress</span></span>

## <span data-ttu-id="7d618-127">상속자</span><span class="sxs-lookup"><span data-stu-id="7d618-127">NOTES</span></span>

## <span data-ttu-id="7d618-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7d618-128">RELATED LINKS</span></span>
