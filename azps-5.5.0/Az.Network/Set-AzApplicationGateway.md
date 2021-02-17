---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
ms.openlocfilehash: 38a9d9d36d4abdf85149fe9d7da5387468985daf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184228"
---
# <span data-ttu-id="8d72f-101">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8d72f-101">Set-AzApplicationGateway</span></span>

## <span data-ttu-id="8d72f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d72f-102">SYNOPSIS</span></span>
<span data-ttu-id="8d72f-103">애플리케이션 게이트웨이를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8d72f-103">Updates an application gateway.</span></span>

## <span data-ttu-id="8d72f-104">구문</span><span class="sxs-lookup"><span data-stu-id="8d72f-104">SYNTAX</span></span>

```
Set-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d72f-105">설명</span><span class="sxs-lookup"><span data-stu-id="8d72f-105">DESCRIPTION</span></span>
<span data-ttu-id="8d72f-106">**Set-AzApplicationGateway** cmdlet은 Azure 애플리케이션 게이트웨이를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8d72f-106">The **Set-AzApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="8d72f-107">예제</span><span class="sxs-lookup"><span data-stu-id="8d72f-107">EXAMPLES</span></span>

### <span data-ttu-id="8d72f-108">예제 1: 애플리케이션 게이트웨이 업데이트</span><span class="sxs-lookup"><span data-stu-id="8d72f-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name Test -ResourceGroupName Appgwtest
PS C:\>$AppGw.Tag = @{"key"="value"}
PS C:\>$UpdatedAppGw = Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="8d72f-109">이러한 명령은 $AppGw 변수의 설정으로 애플리케이션 게이트웨이를 업데이트하고 업데이트된 게이트웨이를 $UpdatedAppGw 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="8d72f-109">These commands update the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="8d72f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d72f-110">PARAMETERS</span></span>

### <span data-ttu-id="8d72f-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8d72f-111">-ApplicationGateway</span></span>
<span data-ttu-id="8d72f-112">애플리케이션 게이트웨이를 설정해야 하는 상태를 나타내는 애플리케이션 게이트웨이 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8d72f-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d72f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d72f-113">-AsJob</span></span>
<span data-ttu-id="8d72f-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="8d72f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8d72f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d72f-115">-DefaultProfile</span></span>
<span data-ttu-id="8d72f-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8d72f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d72f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d72f-117">CommonParameters</span></span>
<span data-ttu-id="8d72f-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8d72f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d72f-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8d72f-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d72f-120">입력</span><span class="sxs-lookup"><span data-stu-id="8d72f-120">INPUTS</span></span>

### <span data-ttu-id="8d72f-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8d72f-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8d72f-122">출력</span><span class="sxs-lookup"><span data-stu-id="8d72f-122">OUTPUTS</span></span>

### <span data-ttu-id="8d72f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8d72f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8d72f-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8d72f-124">NOTES</span></span>

## <span data-ttu-id="8d72f-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8d72f-125">RELATED LINKS</span></span>

[<span data-ttu-id="8d72f-126">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8d72f-126">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


