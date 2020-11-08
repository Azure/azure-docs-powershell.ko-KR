---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 22E8CB18-8CDD-4992-AB81-E1BB400E6BC7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 294e931529b7de939a6a5c20181d48b18da1e892
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046277"
---
# <span data-ttu-id="52242-101">Get-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="52242-101">Get-AzureVNetGatewayDiagnostics</span></span>

## <span data-ttu-id="52242-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52242-102">SYNOPSIS</span></span>
<span data-ttu-id="52242-103">가상 네트워크 게이트웨이에 대 한 진단의 현재 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="52242-103">Gets the current state of diagnostics for a virtual network gateway.</span></span>

## <span data-ttu-id="52242-104">구문과</span><span class="sxs-lookup"><span data-stu-id="52242-104">SYNTAX</span></span>

```
Get-AzureVNetGatewayDiagnostics -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="52242-105">설명은</span><span class="sxs-lookup"><span data-stu-id="52242-105">DESCRIPTION</span></span>
<span data-ttu-id="52242-106">**Get-Azurevnet2| 진단** cmdlet은 가상 네트워크 게이트웨이에 대 한 진단의 현재 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="52242-106">The **Get-AzureVNetGatewayDiagnostics** cmdlet gets the current state of diagnostics for a virtual network gateway.</span></span>
<span data-ttu-id="52242-107">Blob (binary large object)가 **시작-AzureVNetGatewayDiagnostics 진단** 유틸리티에서 이전 진단 세션을 저장 한 경우이 cmdlet은 해당 cmdlet이 진단 세션을 저장 한 BLOB의 URL도 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="52242-107">If a binary large object (blob) exists where the **Start-AzureVNetGatewayDiagnostics** saved a previous diagnostics session, this cmdlet also returns the URL of the blob where that cmdlet saved that diagnostics session.</span></span>

## <span data-ttu-id="52242-108">예제의</span><span class="sxs-lookup"><span data-stu-id="52242-108">EXAMPLES</span></span>

## <span data-ttu-id="52242-109">변수</span><span class="sxs-lookup"><span data-stu-id="52242-109">PARAMETERS</span></span>

### <span data-ttu-id="52242-110">-프로필</span><span class="sxs-lookup"><span data-stu-id="52242-110">-Profile</span></span>
<span data-ttu-id="52242-111">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="52242-111">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="52242-112">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="52242-112">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="52242-113">-VNetName</span><span class="sxs-lookup"><span data-stu-id="52242-113">-VNetName</span></span>
<span data-ttu-id="52242-114">이 cmdlet이 진단 프로그램을 제공 하는 가상 네트워크 게이트웨이를 포함 하는 가상 네트워크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="52242-114">Specifies the virtual network that contains a virtual network gateway for which this cmdlet gets diagnostics.</span></span>

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

### <span data-ttu-id="52242-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52242-115">CommonParameters</span></span>
<span data-ttu-id="52242-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="52242-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52242-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52242-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52242-118">입력</span><span class="sxs-lookup"><span data-stu-id="52242-118">INPUTS</span></span>

## <span data-ttu-id="52242-119">출력</span><span class="sxs-lookup"><span data-stu-id="52242-119">OUTPUTS</span></span>

## <span data-ttu-id="52242-120">상속자</span><span class="sxs-lookup"><span data-stu-id="52242-120">NOTES</span></span>

## <span data-ttu-id="52242-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="52242-121">RELATED LINKS</span></span>

[<span data-ttu-id="52242-122">Start-Azurevnet2| 진단</span><span class="sxs-lookup"><span data-stu-id="52242-122">Start-AzureVNetGatewayDiagnostics</span></span>](./Start-AzureVNetGatewayDiagnostics.md)

[<span data-ttu-id="52242-123">중지-Azurevnet2| 진단</span><span class="sxs-lookup"><span data-stu-id="52242-123">Stop-AzureVNetGatewayDiagnostics</span></span>](./Stop-AzureVNetGatewayDiagnostics.md)


