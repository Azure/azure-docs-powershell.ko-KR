---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D5E928C3-26B6-4B7C-8A9C-F1F602BABF75
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaybackendhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHealth.md
ms.openlocfilehash: b5910352c8abcfb880a1007a3f2246ff7c12d9f8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003616"
---
# <span data-ttu-id="1fae3-101">Get-AzApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="1fae3-101">Get-AzApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="1fae3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fae3-102">SYNOPSIS</span></span>
<span data-ttu-id="1fae3-103">애플리케이션 게이트웨이 백end 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="1fae3-103">Gets application gateway backend health.</span></span>

## <span data-ttu-id="1fae3-104">구문</span><span class="sxs-lookup"><span data-stu-id="1fae3-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHealth -Name <String> -ResourceGroupName <String> [-ExpandResource <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fae3-105">설명</span><span class="sxs-lookup"><span data-stu-id="1fae3-105">DESCRIPTION</span></span>
<span data-ttu-id="1fae3-106">Get-AzApplicationGatewayBackendHealth cmdlet은 애플리케이션 게이트웨이 백end 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="1fae3-106">The Get-AzApplicationGatewayBackendHealth cmdlet gets application gateway backend health.</span></span>

## <span data-ttu-id="1fae3-107">예제</span><span class="sxs-lookup"><span data-stu-id="1fae3-107">EXAMPLES</span></span>

### <span data-ttu-id="1fae3-108">예제 1: 확장된 리소스 없이 백end 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="1fae3-108">Example 1: Gets backend health without expanded resources.</span></span>
```
PS C:\>$BackendHealth = Get-AzApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="1fae3-109">이 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 ApplicationGateway01이라는 애플리케이션 게이트웨이의 백end $BackendHealth 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="1fae3-109">This command gets the backend health of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

### <span data-ttu-id="1fae3-110">예제 2: 확장된 리소스를 통해 백end 상태 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1fae3-110">Example 2: Gets backend health with expanded resources.</span></span>
```
PS C:\>$BackendHealth = Get-AzApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01 -ExpandResource "backendhealth/applicationgatewayresource"
```

<span data-ttu-id="1fae3-111">이 명령은 ResourceGroup01이라는 리소스 그룹에 속한 ApplicationGateway01이라는 애플리케이션 게이트웨이의 백end 상태(확장된 리소스)를 얻게 하여 해당 $BackendHealth 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="1fae3-111">This command gets the backend health (with expanded resources) of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

## <span data-ttu-id="1fae3-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1fae3-112">PARAMETERS</span></span>

### <span data-ttu-id="1fae3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1fae3-113">-AsJob</span></span>
<span data-ttu-id="1fae3-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1fae3-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fae3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fae3-115">-DefaultProfile</span></span>
<span data-ttu-id="1fae3-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1fae3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fae3-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="1fae3-117">-ExpandResource</span></span>
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

### <span data-ttu-id="1fae3-118">-Name</span><span class="sxs-lookup"><span data-stu-id="1fae3-118">-Name</span></span>
<span data-ttu-id="1fae3-119">이 cmdlet이 얻을 애플리케이션 게이트웨이의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1fae3-119">Specifies the name of the application gateway that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1fae3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fae3-120">-ResourceGroupName</span></span>
<span data-ttu-id="1fae3-121">애플리케이션 게이트웨이를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1fae3-121">Specifies the name of the resource group that contains the application gateway.</span></span>

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

### <span data-ttu-id="1fae3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fae3-122">CommonParameters</span></span>
<span data-ttu-id="1fae3-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1fae3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fae3-124">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1fae3-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fae3-125">입력</span><span class="sxs-lookup"><span data-stu-id="1fae3-125">INPUTS</span></span>

### <span data-ttu-id="1fae3-126">System.String</span><span class="sxs-lookup"><span data-stu-id="1fae3-126">System.String</span></span>

## <span data-ttu-id="1fae3-127">출력</span><span class="sxs-lookup"><span data-stu-id="1fae3-127">OUTPUTS</span></span>

### <span data-ttu-id="1fae3-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="1fae3-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="1fae3-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1fae3-129">NOTES</span></span>
<span data-ttu-id="1fae3-130">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="1fae3-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="1fae3-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1fae3-131">RELATED LINKS</span></span>

[<span data-ttu-id="1fae3-132">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1fae3-132">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

