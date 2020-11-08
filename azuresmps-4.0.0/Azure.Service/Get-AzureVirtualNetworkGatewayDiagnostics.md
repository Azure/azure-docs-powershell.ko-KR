---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: F6A89D39-18AD-4087-823C-63FA0A3690E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 36c51d0ceae42aab50e2df9e0532c98dd6800747
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046520"
---
# <span data-ttu-id="85535-101">Get-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="85535-101">Get-AzureVirtualNetworkGatewayDiagnostics</span></span>

## <span data-ttu-id="85535-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85535-102">SYNOPSIS</span></span>
<span data-ttu-id="85535-103">Azure 가상 네트워크 게이트웨이 진단 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="85535-103">Gets the results of Azure virtual network gateway diagnostics.</span></span>

## <span data-ttu-id="85535-104">구문과</span><span class="sxs-lookup"><span data-stu-id="85535-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGatewayDiagnostics -GatewayId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="85535-105">설명은</span><span class="sxs-lookup"><span data-stu-id="85535-105">DESCRIPTION</span></span>
<span data-ttu-id="85535-106">**AzureVirtualNetworkGatewayDiagnostics** Cmdlet은 Azure 가상 네트워크 게이트웨이 진단 결과를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="85535-106">The **Get-AzureVirtualNetworkGatewayDiagnostics** cmdlet gets the results of Azure virtual network gateway diagnostics.</span></span>

## <span data-ttu-id="85535-107">예제의</span><span class="sxs-lookup"><span data-stu-id="85535-107">EXAMPLES</span></span>

## <span data-ttu-id="85535-108">변수</span><span class="sxs-lookup"><span data-stu-id="85535-108">PARAMETERS</span></span>

### <span data-ttu-id="85535-109">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="85535-109">-GatewayId</span></span>
<span data-ttu-id="85535-110">게이트웨이의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="85535-110">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="85535-111">-프로필</span><span class="sxs-lookup"><span data-stu-id="85535-111">-Profile</span></span>
<span data-ttu-id="85535-112">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="85535-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="85535-113">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="85535-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85535-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85535-114">CommonParameters</span></span>
<span data-ttu-id="85535-115">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="85535-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85535-116">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85535-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85535-117">입력</span><span class="sxs-lookup"><span data-stu-id="85535-117">INPUTS</span></span>

## <span data-ttu-id="85535-118">출력</span><span class="sxs-lookup"><span data-stu-id="85535-118">OUTPUTS</span></span>

## <span data-ttu-id="85535-119">상속자</span><span class="sxs-lookup"><span data-stu-id="85535-119">NOTES</span></span>

## <span data-ttu-id="85535-120">관련 링크</span><span class="sxs-lookup"><span data-stu-id="85535-120">RELATED LINKS</span></span>

[<span data-ttu-id="85535-121">시작-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="85535-121">Start-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Start-AzureVirtualNetworkGatewayDiagnostics.md)

[<span data-ttu-id="85535-122">중지-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="85535-122">Stop-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Stop-AzureVirtualNetworkGatewayDiagnostics.md)


