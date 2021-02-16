---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprivatelinkipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
ms.openlocfilehash: 01da3615a43a5923d6017e759c1b04f039332c9f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202906"
---
# <span data-ttu-id="35efb-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="35efb-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="35efb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35efb-102">SYNOPSIS</span></span>
<span data-ttu-id="35efb-103">PrivateLink 구성과 연결될 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="35efb-103">Creates an Ip Configuration to be associated with PrivateLink Configuration</span></span>

## <span data-ttu-id="35efb-104">구문</span><span class="sxs-lookup"><span data-stu-id="35efb-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkIpConfiguration -Name <String> -Subnet <PSSubnet>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35efb-105">설명</span><span class="sxs-lookup"><span data-stu-id="35efb-105">DESCRIPTION</span></span>
<span data-ttu-id="35efb-106">**New-AzApplicationGatewayPrivateLinkIpConfiguration** cmdlet은 Azure 애플리케이션 게이트웨이에 대한 PrivateLink 구성과 연결될 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="35efb-106">The **New-AzApplicationGatewayPrivateLinkIpConfiguration** cmdlet creates an Ip Configuration to be associated with PrivateLink Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="35efb-107">예제</span><span class="sxs-lookup"><span data-stu-id="35efb-107">EXAMPLES</span></span>

### <span data-ttu-id="35efb-108">예제 1: PrivateLink IP 구성</span><span class="sxs-lookup"><span data-stu-id="35efb-108">Example 1: PrivateLink Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkIpConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
```

<span data-ttu-id="35efb-109">이 명령은 'ipConfig01'이라는 PrivateLink IP 구성을 만들어 해당 이름의 변수에 결과를 $PrivateLinkIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="35efb-109">This command creates an PrivateLink IP Configuration named 'ipConfig01' stores the result in the variable named $PrivateLinkIpConfiguration.</span></span> 

## <span data-ttu-id="35efb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35efb-110">PARAMETERS</span></span>

### <span data-ttu-id="35efb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35efb-111">-DefaultProfile</span></span>
<span data-ttu-id="35efb-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="35efb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35efb-113">-Name</span><span class="sxs-lookup"><span data-stu-id="35efb-113">-Name</span></span>
<span data-ttu-id="35efb-114">IpConfiguration의 이름</span><span class="sxs-lookup"><span data-stu-id="35efb-114">The name of the IpConfiguration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35efb-115">-Primary</span><span class="sxs-lookup"><span data-stu-id="35efb-115">-Primary</span></span>
<span data-ttu-id="35efb-116">IP 구성이 기본이 된다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="35efb-116">Indicate the ip configuration is primary.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35efb-117">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="35efb-117">-PrivateIpAddress</span></span>
<span data-ttu-id="35efb-118">고정 할당이 필요한 경우 ipConfiguration의 개인 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="35efb-118">The private ip address of the ipConfiguration if static allocation is desired.</span></span>

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

### <span data-ttu-id="35efb-119">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="35efb-119">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="35efb-120">IP 구성의 IP 버전</span><span class="sxs-lookup"><span data-stu-id="35efb-120">The ip version of the ip configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35efb-121">-Subnet</span><span class="sxs-lookup"><span data-stu-id="35efb-121">-Subnet</span></span>
<span data-ttu-id="35efb-122">서브넷</span><span class="sxs-lookup"><span data-stu-id="35efb-122">Subnet</span></span>

```yaml
Type: PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35efb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35efb-123">CommonParameters</span></span>
<span data-ttu-id="35efb-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="35efb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35efb-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="35efb-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35efb-126">입력</span><span class="sxs-lookup"><span data-stu-id="35efb-126">INPUTS</span></span>

### <span data-ttu-id="35efb-127">없음</span><span class="sxs-lookup"><span data-stu-id="35efb-127">None</span></span>

## <span data-ttu-id="35efb-128">출력</span><span class="sxs-lookup"><span data-stu-id="35efb-128">OUTPUTS</span></span>

### <span data-ttu-id="35efb-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="35efb-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="35efb-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="35efb-130">NOTES</span></span>

## <span data-ttu-id="35efb-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="35efb-131">RELATED LINKS</span></span>

[<span data-ttu-id="35efb-132">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="35efb-132">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)
