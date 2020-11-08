---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9E7A170D-512A-4117-85C3-3AA4D6341C6B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 97fe847fd183caa7de281b358da579e8df4d5831
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045740"
---
# <span data-ttu-id="3ff7f-101">Stop-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="3ff7f-101">Stop-AzureVirtualNetworkGatewayDiagnostics</span></span>

## <span data-ttu-id="3ff7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ff7f-102">SYNOPSIS</span></span>
<span data-ttu-id="3ff7f-103">실행 중인 가상 네트워크 게이트웨이 진단 세션을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ff7f-103">Stops a running virtual network gateway diagnostics session.</span></span>

## <span data-ttu-id="3ff7f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3ff7f-104">SYNTAX</span></span>

```
Stop-AzureVirtualNetworkGatewayDiagnostics -GatewayId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3ff7f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3ff7f-105">DESCRIPTION</span></span>
<span data-ttu-id="3ff7f-106">**AzureVirtualNetworkGatewayDiagnostics** cmdlet은 실행 중인 가상 네트워크 게이트웨이 진단 세션을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ff7f-106">The **Stop-AzureVirtualNetworkGatewayDiagnostics** cmdlet stops a running virtual network gateway diagnostics session.</span></span>
<span data-ttu-id="3ff7f-107">이 명령은 Start-AzureVirtualNetworkGatewayDiagnostics cmdlet에서 지정 하는 저장소 계정에 진단 세션의 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ff7f-107">This command saves the results of the diagnostics session to the storage account that the Start-AzureVirtualNetworkGatewayDiagnostics cmdlet specifies.</span></span>

## <span data-ttu-id="3ff7f-108">예제의</span><span class="sxs-lookup"><span data-stu-id="3ff7f-108">EXAMPLES</span></span>

## <span data-ttu-id="3ff7f-109">변수</span><span class="sxs-lookup"><span data-stu-id="3ff7f-109">PARAMETERS</span></span>

### <span data-ttu-id="3ff7f-110">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="3ff7f-110">-GatewayId</span></span>
<span data-ttu-id="3ff7f-111">게이트웨이의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ff7f-111">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="3ff7f-112">-프로필</span><span class="sxs-lookup"><span data-stu-id="3ff7f-112">-Profile</span></span>
<span data-ttu-id="3ff7f-113">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ff7f-113">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="3ff7f-114">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="3ff7f-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3ff7f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ff7f-115">CommonParameters</span></span>
<span data-ttu-id="3ff7f-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ff7f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ff7f-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ff7f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ff7f-118">입력</span><span class="sxs-lookup"><span data-stu-id="3ff7f-118">INPUTS</span></span>

## <span data-ttu-id="3ff7f-119">출력</span><span class="sxs-lookup"><span data-stu-id="3ff7f-119">OUTPUTS</span></span>

## <span data-ttu-id="3ff7f-120">상속자</span><span class="sxs-lookup"><span data-stu-id="3ff7f-120">NOTES</span></span>

## <span data-ttu-id="3ff7f-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3ff7f-121">RELATED LINKS</span></span>

[<span data-ttu-id="3ff7f-122">Get-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="3ff7f-122">Get-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Get-AzureVirtualNetworkGatewayDiagnostics.md)

[<span data-ttu-id="3ff7f-123">시작-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="3ff7f-123">Start-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Start-AzureVirtualNetworkGatewayDiagnostics.md)


