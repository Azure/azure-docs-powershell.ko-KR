---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 68fa8e24d9cdc5e5dbf04ed132e1eac4909973d4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875369"
---
# <span data-ttu-id="8acbb-101">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8acbb-101">Remove-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="8acbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8acbb-102">SYNOPSIS</span></span>
<span data-ttu-id="8acbb-103">응용 프로그램 게이트웨이에서 IP 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8acbb-103">Removes an IP configuration from an application gateway.</span></span>

## <span data-ttu-id="8acbb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8acbb-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8acbb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8acbb-105">DESCRIPTION</span></span>
<span data-ttu-id="8acbb-106">**AzApplicationGatewayIPConfiguration** Cmdlet은 Azure 응용 프로그램 게이트웨이에서 IP 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8acbb-106">The **Remove-AzApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="8acbb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8acbb-107">EXAMPLES</span></span>

### <span data-ttu-id="8acbb-108">예제 1: Azure 응용 프로그램 게이트웨이에서 IP 구성 제거</span><span class="sxs-lookup"><span data-stu-id="8acbb-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="8acbb-109">첫 번째 명령은 응용 프로그램 게이트웨이를 가져와 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8acbb-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="8acbb-110">두 번째 명령은 $AppGw에 저장 된 응용 프로그램 게이트웨이에서 Subnet02 이라는 IP 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8acbb-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="8acbb-111">변수</span><span class="sxs-lookup"><span data-stu-id="8acbb-111">PARAMETERS</span></span>

### <span data-ttu-id="8acbb-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8acbb-112">-ApplicationGateway</span></span>
<span data-ttu-id="8acbb-113">IP 구성을 제거할 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8acbb-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8acbb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8acbb-114">-DefaultProfile</span></span>
<span data-ttu-id="8acbb-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8acbb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8acbb-116">-이름</span><span class="sxs-lookup"><span data-stu-id="8acbb-116">-Name</span></span>
<span data-ttu-id="8acbb-117">제거할 IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8acbb-117">Specifies the name of the IP configuration to remove.</span></span>

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

### <span data-ttu-id="8acbb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8acbb-118">CommonParameters</span></span>
<span data-ttu-id="8acbb-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8acbb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8acbb-120">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8acbb-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8acbb-121">입력</span><span class="sxs-lookup"><span data-stu-id="8acbb-121">INPUTS</span></span>

### <span data-ttu-id="8acbb-122">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8acbb-122">System.String</span></span>

## <span data-ttu-id="8acbb-123">출력</span><span class="sxs-lookup"><span data-stu-id="8acbb-123">OUTPUTS</span></span>

### <span data-ttu-id="8acbb-124">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8acbb-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8acbb-125">상속자</span><span class="sxs-lookup"><span data-stu-id="8acbb-125">NOTES</span></span>

## <span data-ttu-id="8acbb-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8acbb-126">RELATED LINKS</span></span>

[<span data-ttu-id="8acbb-127">추가-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8acbb-127">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="8acbb-128">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8acbb-128">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="8acbb-129">새로운 AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8acbb-129">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="8acbb-130">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8acbb-130">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


