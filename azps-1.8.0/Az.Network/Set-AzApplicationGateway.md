---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
ms.openlocfilehash: 34f3de9e2dafe3cfb9b15aad1dda7d75bab67c20
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700073"
---
# <span data-ttu-id="a5684-101">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a5684-101">Set-AzApplicationGateway</span></span>

## <span data-ttu-id="a5684-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5684-102">SYNOPSIS</span></span>
<span data-ttu-id="a5684-103">응용 프로그램 게이트웨이를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5684-103">Updates an application gateway.</span></span>

## <span data-ttu-id="a5684-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a5684-104">SYNTAX</span></span>

```
Set-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5684-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a5684-105">DESCRIPTION</span></span>
<span data-ttu-id="a5684-106">**AzApplicationGateway** Cmdlet은 Azure application gateway를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5684-106">The **Set-AzApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="a5684-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a5684-107">EXAMPLES</span></span>

### <span data-ttu-id="a5684-108">예제 1: 응용 프로그램 게이트웨이 업데이트</span><span class="sxs-lookup"><span data-stu-id="a5684-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$UpdatedAppGw = Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="a5684-109">이 명령은 $AppGw 변수의 설정을 사용 하 여 응용 프로그램 게이트웨이를 업데이트 하 고 업데이트 된 게이트웨이를 $UpdatedAppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5684-109">This command updates the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="a5684-110">변수</span><span class="sxs-lookup"><span data-stu-id="a5684-110">PARAMETERS</span></span>

### <span data-ttu-id="a5684-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a5684-111">-ApplicationGateway</span></span>
<span data-ttu-id="a5684-112">응용 프로그램 게이트웨이를 설정 해야 하는 상태를 나타내는 응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5684-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

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

### <span data-ttu-id="a5684-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5684-113">-AsJob</span></span>
<span data-ttu-id="a5684-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a5684-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a5684-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5684-115">-DefaultProfile</span></span>
<span data-ttu-id="a5684-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5684-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5684-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5684-117">CommonParameters</span></span>
<span data-ttu-id="a5684-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5684-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5684-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5684-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5684-120">입력</span><span class="sxs-lookup"><span data-stu-id="a5684-120">INPUTS</span></span>

### <span data-ttu-id="a5684-121">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a5684-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a5684-122">출력</span><span class="sxs-lookup"><span data-stu-id="a5684-122">OUTPUTS</span></span>

### <span data-ttu-id="a5684-123">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a5684-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a5684-124">상속자</span><span class="sxs-lookup"><span data-stu-id="a5684-124">NOTES</span></span>

## <span data-ttu-id="a5684-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5684-125">RELATED LINKS</span></span>

[<span data-ttu-id="a5684-126">시작-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a5684-126">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


