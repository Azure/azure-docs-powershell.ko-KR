---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
ms.openlocfilehash: c4bc5e9fcc7d0ca405a8031af29d16283f963ad2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202811"
---
# <span data-ttu-id="06044-101">New-AzFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="06044-101">New-AzFirewallPublicIpAddress</span></span>

## <span data-ttu-id="06044-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06044-102">SYNOPSIS</span></span>
<span data-ttu-id="06044-103">Azure 방화벽에서 다중 pip에 사용할 수 있는 IP 주소의 자리 홀더입니다.</span><span class="sxs-lookup"><span data-stu-id="06044-103">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="06044-104">구문</span><span class="sxs-lookup"><span data-stu-id="06044-104">SYNTAX</span></span>

```
New-AzFirewallPublicIpAddress [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06044-105">설명</span><span class="sxs-lookup"><span data-stu-id="06044-105">DESCRIPTION</span></span>
<span data-ttu-id="06044-106">Azure 방화벽에서 다중 pip에 사용할 수 있는 IP 주소의 자리 홀더입니다.</span><span class="sxs-lookup"><span data-stu-id="06044-106">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="06044-107">예제</span><span class="sxs-lookup"><span data-stu-id="06044-107">EXAMPLES</span></span>

### <span data-ttu-id="06044-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="06044-108">Example 1</span></span>
```powershell
PS C:\> $publicIp = New-AzFirewallPublicIpAddress -Address 20.2.3.4
```

<span data-ttu-id="06044-109">$publicIp IP 주소 20.2.3.4의 자리 홀더가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="06044-109">$publicIp will be the placeholder for the ip address 20.2.3.4</span></span>

## <span data-ttu-id="06044-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06044-110">PARAMETERS</span></span>

### <span data-ttu-id="06044-111">-Address</span><span class="sxs-lookup"><span data-stu-id="06044-111">-Address</span></span>
<span data-ttu-id="06044-112">허브에 연결된 방화벽의 IP 주소</span><span class="sxs-lookup"><span data-stu-id="06044-112">The IP Addresses of the Firewall attached to a hub</span></span>

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

### <span data-ttu-id="06044-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06044-113">-DefaultProfile</span></span>
<span data-ttu-id="06044-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="06044-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06044-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06044-115">-Confirm</span></span>
<span data-ttu-id="06044-116">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="06044-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06044-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06044-117">-WhatIf</span></span>
<span data-ttu-id="06044-118">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="06044-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06044-119">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="06044-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06044-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06044-120">CommonParameters</span></span>
<span data-ttu-id="06044-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="06044-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06044-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="06044-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06044-123">입력</span><span class="sxs-lookup"><span data-stu-id="06044-123">INPUTS</span></span>

### <span data-ttu-id="06044-124">없음</span><span class="sxs-lookup"><span data-stu-id="06044-124">None</span></span>

## <span data-ttu-id="06044-125">출력</span><span class="sxs-lookup"><span data-stu-id="06044-125">OUTPUTS</span></span>

### <span data-ttu-id="06044-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="06044-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPublicIpAddress</span></span>

## <span data-ttu-id="06044-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="06044-127">NOTES</span></span>

## <span data-ttu-id="06044-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="06044-128">RELATED LINKS</span></span>
