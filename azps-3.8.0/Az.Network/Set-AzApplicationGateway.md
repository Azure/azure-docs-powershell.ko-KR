---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
ms.openlocfilehash: e4f0e4e40def984916012cf32bf8c5e1df5eea76
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043927"
---
# <span data-ttu-id="8e12b-101">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e12b-101">Set-AzApplicationGateway</span></span>

## <span data-ttu-id="8e12b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e12b-102">SYNOPSIS</span></span>
<span data-ttu-id="8e12b-103">응용 프로그램 게이트웨이를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e12b-103">Updates an application gateway.</span></span>

## <span data-ttu-id="8e12b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8e12b-104">SYNTAX</span></span>

```
Set-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e12b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8e12b-105">DESCRIPTION</span></span>
<span data-ttu-id="8e12b-106">**AzApplicationGateway** Cmdlet은 Azure application gateway를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e12b-106">The **Set-AzApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="8e12b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8e12b-107">EXAMPLES</span></span>

### <span data-ttu-id="8e12b-108">예제 1: 응용 프로그램 게이트웨이 업데이트</span><span class="sxs-lookup"><span data-stu-id="8e12b-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$UpdatedAppGw = Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="8e12b-109">이 명령은 $AppGw 변수의 설정을 사용 하 여 응용 프로그램 게이트웨이를 업데이트 하 고 업데이트 된 게이트웨이를 $UpdatedAppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e12b-109">This command updates the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="8e12b-110">변수</span><span class="sxs-lookup"><span data-stu-id="8e12b-110">PARAMETERS</span></span>

### <span data-ttu-id="8e12b-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e12b-111">-ApplicationGateway</span></span>
<span data-ttu-id="8e12b-112">응용 프로그램 게이트웨이를 설정 해야 하는 상태를 나타내는 응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e12b-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

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

### <span data-ttu-id="8e12b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e12b-113">-AsJob</span></span>
<span data-ttu-id="8e12b-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="8e12b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e12b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e12b-115">-DefaultProfile</span></span>
<span data-ttu-id="8e12b-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8e12b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e12b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e12b-117">CommonParameters</span></span>
<span data-ttu-id="8e12b-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e12b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e12b-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e12b-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e12b-120">입력</span><span class="sxs-lookup"><span data-stu-id="8e12b-120">INPUTS</span></span>

### <span data-ttu-id="8e12b-121">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e12b-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8e12b-122">출력</span><span class="sxs-lookup"><span data-stu-id="8e12b-122">OUTPUTS</span></span>

### <span data-ttu-id="8e12b-123">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e12b-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8e12b-124">상속자</span><span class="sxs-lookup"><span data-stu-id="8e12b-124">NOTES</span></span>

## <span data-ttu-id="8e12b-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e12b-125">RELATED LINKS</span></span>

[<span data-ttu-id="8e12b-126">시작-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e12b-126">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


