---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D5E928C3-26B6-4B7C-8A9C-F1F602BABF75
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHealth.md
ms.openlocfilehash: eb4415f4c61fd97543bd0e50de6a0a3737f435f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700664"
---
# <span data-ttu-id="483cf-101">Get-AzApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="483cf-101">Get-AzApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="483cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="483cf-102">SYNOPSIS</span></span>
<span data-ttu-id="483cf-103">응용 프로그램 게이트웨이 백 엔드 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="483cf-103">Gets application gateway backend health.</span></span>

## <span data-ttu-id="483cf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="483cf-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHealth -Name <String> -ResourceGroupName <String> [-ExpandResource <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="483cf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="483cf-105">DESCRIPTION</span></span>
<span data-ttu-id="483cf-106">Get-AzApplicationGatewayBackendHealth cmdlet은 응용 프로그램 게이트웨이 백 엔드 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="483cf-106">The Get-AzApplicationGatewayBackendHealth cmdlet gets application gateway backend health.</span></span>

## <span data-ttu-id="483cf-107">예제의</span><span class="sxs-lookup"><span data-stu-id="483cf-107">EXAMPLES</span></span>

### <span data-ttu-id="483cf-108">예제 1: 확장 된 리소스가 없는 백 엔드 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="483cf-108">Example 1: Gets backend health without expanded resources.</span></span>
```
PS C:\>$BackendHealth = Get-AzApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="483cf-109">이 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이의 백 엔드 상태를 가져오고이를 $BackendHealth 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="483cf-109">This command gets the backend health of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

### <span data-ttu-id="483cf-110">예제 2: 확장 리소스를 사용 하 여 백엔드 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="483cf-110">Example 2: Gets backend health with expanded resources.</span></span>
```
PS C:\>$BackendHealth = Get-AzApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01 -ExpandResource "backendhealth/applicationgatewayresource"
```

<span data-ttu-id="483cf-111">이 명령은 ResourceGroup01 이라는 리소스 그룹에 속하고이를 $BackendHealth 변수에 저장 하는 응용 프로그램 게이트웨이의 확장 된 리소스를 사용 하 여 백 엔드 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="483cf-111">This command gets the backend health (with expanded resources) of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

## <span data-ttu-id="483cf-112">변수</span><span class="sxs-lookup"><span data-stu-id="483cf-112">PARAMETERS</span></span>

### <span data-ttu-id="483cf-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="483cf-113">-AsJob</span></span>
<span data-ttu-id="483cf-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="483cf-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="483cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="483cf-115">-DefaultProfile</span></span>
<span data-ttu-id="483cf-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="483cf-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="483cf-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="483cf-117">-ExpandResource</span></span>
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

### <span data-ttu-id="483cf-118">-이름</span><span class="sxs-lookup"><span data-stu-id="483cf-118">-Name</span></span>
<span data-ttu-id="483cf-119">이 cmdlet이 가져오는 응용 프로그램 게이트웨이의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="483cf-119">Specifies the name of the application gateway that this cmdlet gets.</span></span>

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

### <span data-ttu-id="483cf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="483cf-120">-ResourceGroupName</span></span>
<span data-ttu-id="483cf-121">응용 프로그램 게이트웨이를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="483cf-121">Specifies the name of the resource group that contains the application gateway.</span></span>

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

### <span data-ttu-id="483cf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="483cf-122">CommonParameters</span></span>
<span data-ttu-id="483cf-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="483cf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="483cf-124">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="483cf-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="483cf-125">입력</span><span class="sxs-lookup"><span data-stu-id="483cf-125">INPUTS</span></span>

### <span data-ttu-id="483cf-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="483cf-126">System.String</span></span>

## <span data-ttu-id="483cf-127">출력</span><span class="sxs-lookup"><span data-stu-id="483cf-127">OUTPUTS</span></span>

### <span data-ttu-id="483cf-128">PSApplicationGatewayBackendHealth에 대 한.</span><span class="sxs-lookup"><span data-stu-id="483cf-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="483cf-129">상속자</span><span class="sxs-lookup"><span data-stu-id="483cf-129">NOTES</span></span>
<span data-ttu-id="483cf-130">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹</span><span class="sxs-lookup"><span data-stu-id="483cf-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="483cf-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="483cf-131">RELATED LINKS</span></span>

[<span data-ttu-id="483cf-132">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="483cf-132">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

