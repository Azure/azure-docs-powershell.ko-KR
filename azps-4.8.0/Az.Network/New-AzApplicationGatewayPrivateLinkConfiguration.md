---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: df616c0b8e6d2fdb7de3567c921714251093fd60
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214874"
---
# <span data-ttu-id="d6366-101">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6366-101">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="d6366-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6366-102">SYNOPSIS</span></span>
<span data-ttu-id="d6366-103">응용 프로그램 게이트웨이에 대 한 개인 링크 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d6366-103">Creates a private link configuration for an application gateway</span></span>

## <span data-ttu-id="d6366-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d6366-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkConfiguration -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6366-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d6366-105">DESCRIPTION</span></span>
<span data-ttu-id="d6366-106">**AzApplicationGatewayPrivateLinkConfiguration** Cmdlet은 Azure application gateway에 대 한 PrivateLink 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d6366-106">The **New-AzApplicationGatewayPrivateLinkConfiguration** cmdlet creates an PrivateLink Configuration for an Azure application gateway.</span></span>
<span data-ttu-id="d6366-107">비공개 링크 기능을 사용 하려면 개인 링크 구성을 프런트 엔드 ip 구성에 연결 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6366-107">The private link configuration must be associated to a frontend ip configuration to enable the private link functionality.</span></span>
<span data-ttu-id="d6366-108">하나의 개인 링크 구성은 응용 프로그램 게이트웨이에서 하나의 프런트 엔드 ip 구성에만 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d6366-108">One private link configuration can atmost be associated to only one frontend ip configuration on application gateway.</span></span>

## <span data-ttu-id="d6366-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d6366-109">EXAMPLES</span></span>

### <span data-ttu-id="d6366-110">예제 1: 단일 Ip 구성을 사용 하 여 개인 링크 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="d6366-110">Example 1: Create an Private Link Configuration with single Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1
```

<span data-ttu-id="d6366-111">이 명령은 ' privateLinkConfig01 ' 이라는 PrivateLink 구성을 만들고 그 결과를 $PrivateLinkConfiguration 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6366-111">This command creates an PrivateLink configuration named 'privateLinkConfig01' and stores the result in the variable named $PrivateLinkConfiguration.</span></span>

### <span data-ttu-id="d6366-112">예제 2: 여러 Ip 구성을 사용 하 여 개인 링크 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="d6366-112">Example 2: Create an Private Link Configuration with multiple Ip Configurations</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1, $privateLinkIpConfiguration2
```

<span data-ttu-id="d6366-113">이 명령은 두 개의 ipConfigurations 있는 ' privateLinkConfig01 ' PrivateLink 구성을 만들고 그 결과를 $PrivateLinkConfiguration 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6366-113">This command creates an PrivateLink configuration named 'privateLinkConfig01' with two ipConfigurations and stores the result in the variable named $PrivateLinkConfiguration.</span></span> 

## <span data-ttu-id="d6366-114">변수</span><span class="sxs-lookup"><span data-stu-id="d6366-114">PARAMETERS</span></span>

### <span data-ttu-id="d6366-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6366-115">-DefaultProfile</span></span>
<span data-ttu-id="d6366-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d6366-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6366-117">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6366-117">-IpConfiguration</span></span>
<span data-ttu-id="d6366-118">IpConfiguration 목록</span><span class="sxs-lookup"><span data-stu-id="d6366-118">The list of ipConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6366-119">-이름</span><span class="sxs-lookup"><span data-stu-id="d6366-119">-Name</span></span>
<span data-ttu-id="d6366-120">PrivateLink 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d6366-120">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="d6366-121">-확인</span><span class="sxs-lookup"><span data-stu-id="d6366-121">-Confirm</span></span>
<span data-ttu-id="d6366-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6366-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6366-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6366-123">-WhatIf</span></span>
<span data-ttu-id="d6366-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d6366-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6366-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d6366-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6366-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6366-126">CommonParameters</span></span>
<span data-ttu-id="d6366-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6366-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6366-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d6366-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6366-129">입력</span><span class="sxs-lookup"><span data-stu-id="d6366-129">INPUTS</span></span>

### <span data-ttu-id="d6366-130">PSApplicationGatewayPrivateLinkIpConfiguration [] (으)로</span><span class="sxs-lookup"><span data-stu-id="d6366-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="d6366-131">출력</span><span class="sxs-lookup"><span data-stu-id="d6366-131">OUTPUTS</span></span>

### <span data-ttu-id="d6366-132">PSApplicationGatewayPrivateLinkConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="d6366-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="d6366-133">상속자</span><span class="sxs-lookup"><span data-stu-id="d6366-133">NOTES</span></span>

## <span data-ttu-id="d6366-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d6366-134">RELATED LINKS</span></span>

[<span data-ttu-id="d6366-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6366-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="d6366-136">추가-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6366-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="d6366-137">제거-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6366-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="d6366-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d6366-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)
