---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D5E928C3-26B6-4B7C-8A9C-F1F602BABF75
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHealth.md
ms.openlocfilehash: d3f5114243828623ba6c55e9694cc4250ae12657
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527460"
---
# <span data-ttu-id="a5c57-101">Get-AzureRmApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="a5c57-101">Get-AzureRmApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="a5c57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5c57-102">SYNOPSIS</span></span>
<span data-ttu-id="a5c57-103">응용 프로그램 게이트웨이 백 엔드 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a5c57-103">Gets application gateway backend health.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5c57-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a5c57-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendHealth -Name <String> -ResourceGroupName <String>
 [-ExpandResource <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5c57-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a5c57-105">DESCRIPTION</span></span>
<span data-ttu-id="a5c57-106">Get-AzureRmApplicationGatewayBackendHealth cmdlet은 응용 프로그램 게이트웨이 백 엔드 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a5c57-106">The Get-AzureRmApplicationGatewayBackendHealth cmdlet gets application gateway backend health.</span></span>

## <span data-ttu-id="a5c57-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a5c57-107">EXAMPLES</span></span>

### <span data-ttu-id="a5c57-108">--------------------------예제 1: 확장 된 리소스가 없는 백 엔드 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a5c57-108">--------------------------  Example 1: Gets backend health without expanded resources.</span></span>  --------------------------
<span data-ttu-id="a5c57-109">@ {paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="a5c57-109">@{paragraph=PS C:\\\>}</span></span>



















```
PS C:\>$BackendHealth = Get-AzureRmApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="a5c57-110">이 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이의 백 엔드 상태를 가져오고이를 $BackendHealth 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c57-110">This command gets the backend health of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

### <span data-ttu-id="a5c57-111">--------------------------예제 1: 확장 리소스를 사용 하 여 백엔드 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a5c57-111">--------------------------  Example 1: Gets backend health with expanded resources.</span></span>  --------------------------
<span data-ttu-id="a5c57-112">@ {paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="a5c57-112">@{paragraph=PS C:\\\>}</span></span>



















```
PS C:\>$BackendHealth = Get-AzureRmApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01 -ExpandResource "backendhealth/applicationgatewayresource"
```

<span data-ttu-id="a5c57-113">이 명령은 ResourceGroup01 이라는 리소스 그룹에 속하고이를 $BackendHealth 변수에 저장 하는 응용 프로그램 게이트웨이의 확장 된 리소스를 사용 하 여 백 엔드 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a5c57-113">This command gets the backend health (with expanded resources) of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

## <span data-ttu-id="a5c57-114">변수</span><span class="sxs-lookup"><span data-stu-id="a5c57-114">PARAMETERS</span></span>

### <span data-ttu-id="a5c57-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="a5c57-115">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5c57-116">-이름</span><span class="sxs-lookup"><span data-stu-id="a5c57-116">-Name</span></span>
<span data-ttu-id="a5c57-117">이 cmdlet이 가져오는 응용 프로그램 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c57-117">Specifies the name of the application gateway that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5c57-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5c57-118">-ResourceGroupName</span></span>
<span data-ttu-id="a5c57-119">응용 프로그램 게이트웨이를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c57-119">Specifies the name of the resource group that contains the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5c57-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5c57-120">-DefaultProfile</span></span>
<span data-ttu-id="a5c57-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5c57-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5c57-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5c57-122">CommonParameters</span></span>
<span data-ttu-id="a5c57-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c57-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5c57-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5c57-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5c57-125">입력</span><span class="sxs-lookup"><span data-stu-id="a5c57-125">INPUTS</span></span>

### <span data-ttu-id="a5c57-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a5c57-126">System.String</span></span>

## <span data-ttu-id="a5c57-127">출력</span><span class="sxs-lookup"><span data-stu-id="a5c57-127">OUTPUTS</span></span>

### <span data-ttu-id="a5c57-128">PSApplicationGatewayBackendHealth에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a5c57-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="a5c57-129">상속자</span><span class="sxs-lookup"><span data-stu-id="a5c57-129">NOTES</span></span>
<span data-ttu-id="a5c57-130">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="a5c57-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="a5c57-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5c57-131">RELATED LINKS</span></span>

[<span data-ttu-id="a5c57-132">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a5c57-132">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

