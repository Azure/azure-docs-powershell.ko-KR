---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprivatelinkipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
ms.openlocfilehash: 01da3615a43a5923d6017e759c1b04f039332c9f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214873"
---
# <span data-ttu-id="293ea-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="293ea-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="293ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="293ea-102">SYNOPSIS</span></span>
<span data-ttu-id="293ea-103">PrivateLink 구성에 연결할 Ip 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="293ea-103">Creates an Ip Configuration to be associated with PrivateLink Configuration</span></span>

## <span data-ttu-id="293ea-104">구문과</span><span class="sxs-lookup"><span data-stu-id="293ea-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkIpConfiguration -Name <String> -Subnet <PSSubnet>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="293ea-105">설명은</span><span class="sxs-lookup"><span data-stu-id="293ea-105">DESCRIPTION</span></span>
<span data-ttu-id="293ea-106">**AzApplicationGatewayPrivateLinkIpConfiguration** Cmdlet은 Azure application gateway에 대 한 PrivateLink 구성에 연결할 Ip 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="293ea-106">The **New-AzApplicationGatewayPrivateLinkIpConfiguration** cmdlet creates an Ip Configuration to be associated with PrivateLink Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="293ea-107">예제의</span><span class="sxs-lookup"><span data-stu-id="293ea-107">EXAMPLES</span></span>

### <span data-ttu-id="293ea-108">예제 1: PrivateLink Ip 구성</span><span class="sxs-lookup"><span data-stu-id="293ea-108">Example 1: PrivateLink Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkIpConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
```

<span data-ttu-id="293ea-109">이 명령은 이름이 ' ipConfig01 ' 인 PrivateLink IP 구성을 만들어 $PrivateLinkIpConfiguration 이라는 변수에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="293ea-109">This command creates an PrivateLink IP Configuration named 'ipConfig01' stores the result in the variable named $PrivateLinkIpConfiguration.</span></span> 

## <span data-ttu-id="293ea-110">변수</span><span class="sxs-lookup"><span data-stu-id="293ea-110">PARAMETERS</span></span>

### <span data-ttu-id="293ea-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="293ea-111">-DefaultProfile</span></span>
<span data-ttu-id="293ea-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="293ea-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="293ea-113">-이름</span><span class="sxs-lookup"><span data-stu-id="293ea-113">-Name</span></span>
<span data-ttu-id="293ea-114">IpConfiguration의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="293ea-114">The name of the IpConfiguration</span></span>

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

### <span data-ttu-id="293ea-115">-기본</span><span class="sxs-lookup"><span data-stu-id="293ea-115">-Primary</span></span>
<span data-ttu-id="293ea-116">기본 ip 구성을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="293ea-116">Indicate the ip configuration is primary.</span></span>

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

### <span data-ttu-id="293ea-117">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="293ea-117">-PrivateIpAddress</span></span>
<span data-ttu-id="293ea-118">정적 할당이 필요한 경우 ipConfiguration의 개인 ip 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="293ea-118">The private ip address of the ipConfiguration if static allocation is desired.</span></span>

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

### <span data-ttu-id="293ea-119">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="293ea-119">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="293ea-120">Ip 구성의 ip 버전</span><span class="sxs-lookup"><span data-stu-id="293ea-120">The ip version of the ip configuration</span></span>

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

### <span data-ttu-id="293ea-121">-서브넷</span><span class="sxs-lookup"><span data-stu-id="293ea-121">-Subnet</span></span>
<span data-ttu-id="293ea-122">서브넷</span><span class="sxs-lookup"><span data-stu-id="293ea-122">Subnet</span></span>

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

### <span data-ttu-id="293ea-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="293ea-123">CommonParameters</span></span>
<span data-ttu-id="293ea-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="293ea-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="293ea-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="293ea-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="293ea-126">입력</span><span class="sxs-lookup"><span data-stu-id="293ea-126">INPUTS</span></span>

### <span data-ttu-id="293ea-127">않아야</span><span class="sxs-lookup"><span data-stu-id="293ea-127">None</span></span>

## <span data-ttu-id="293ea-128">출력</span><span class="sxs-lookup"><span data-stu-id="293ea-128">OUTPUTS</span></span>

### <span data-ttu-id="293ea-129">PSApplicationGatewayPrivateLinkIpConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="293ea-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="293ea-130">상속자</span><span class="sxs-lookup"><span data-stu-id="293ea-130">NOTES</span></span>

## <span data-ttu-id="293ea-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="293ea-131">RELATED LINKS</span></span>

[<span data-ttu-id="293ea-132">새로운 AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="293ea-132">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)
