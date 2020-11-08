---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: DA5689DF-AA4A-4161-89B0-8055BF384274
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7b71367ac18a753fad5425d0073b55cacb413e4b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045772"
---
# <span data-ttu-id="d3ce0-101">Start-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="d3ce0-101">Start-AzureVirtualNetworkGatewayDiagnostics</span></span>

## <span data-ttu-id="d3ce0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3ce0-102">SYNOPSIS</span></span>
<span data-ttu-id="d3ce0-103">가상 네트워크 게이트웨이에 대 한 진단을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ce0-103">Starts diagnostics for a virtual network gateway.</span></span>

## <span data-ttu-id="d3ce0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d3ce0-104">SYNTAX</span></span>

```
Start-AzureVirtualNetworkGatewayDiagnostics -GatewayId <String> [-CaptureDurationInSeconds <Int32>]
 [-ContainerName <String>] [-StorageContext <AzureStorageContext>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d3ce0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d3ce0-105">DESCRIPTION</span></span>
<span data-ttu-id="d3ce0-106">**AzureVirtualNetworkGatewayDiagnostics** cmdlet은 가상 네트워크 게이트웨이에 대 한 새 게이트웨이 진단 세션을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ce0-106">The **Start-AzureVirtualNetworkGatewayDiagnostics** cmdlet starts a new gateway diagnostics session for a virtual network gateway.</span></span>
<span data-ttu-id="d3ce0-107">게이트웨이 진단 세션은 한 번에 하나만 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d3ce0-107">Only one gateway diagnostics session can run at a time.</span></span>
<span data-ttu-id="d3ce0-108">게이트웨이 진단 세션이 실행 되는 동안이 cmdlet을 실행 하면이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ce0-108">If you run this cmdlet while a gateway diagnostics session is running, this cmdlet returns an error.</span></span>

## <span data-ttu-id="d3ce0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d3ce0-109">EXAMPLES</span></span>

## <span data-ttu-id="d3ce0-110">변수</span><span class="sxs-lookup"><span data-stu-id="d3ce0-110">PARAMETERS</span></span>

### <span data-ttu-id="d3ce0-111">-CaptureDurationInSeconds</span><span class="sxs-lookup"><span data-stu-id="d3ce0-111">-CaptureDurationInSeconds</span></span>
<span data-ttu-id="d3ce0-112">캡처 지속 시간 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ce0-112">Specifies the capture duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3ce0-113">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="d3ce0-113">-ContainerName</span></span>
<span data-ttu-id="d3ce0-114">Azure 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ce0-114">Specifies the name of an Azure container.</span></span>
<span data-ttu-id="d3ce0-115">이 cmdlet은이 매개 변수에서 지정 하는 컨테이너에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ce0-115">This cmdlet stores results in the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3ce0-116">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="d3ce0-116">-GatewayId</span></span>
<span data-ttu-id="d3ce0-117">게이트웨이의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ce0-117">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="d3ce0-118">-프로필</span><span class="sxs-lookup"><span data-stu-id="d3ce0-118">-Profile</span></span>
<span data-ttu-id="d3ce0-119">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ce0-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d3ce0-120">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="d3ce0-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d3ce0-121">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="d3ce0-121">-StorageContext</span></span>
<span data-ttu-id="d3ce0-122">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ce0-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d3ce0-123">이 cmdlet은이 매개 변수에서 지정 하는 저장소 컨텍스트를 사용 하 여 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ce0-123">This cmdlet stores results by using the storage context that this parameter specifies.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3ce0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3ce0-124">CommonParameters</span></span>
<span data-ttu-id="d3ce0-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3ce0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3ce0-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3ce0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3ce0-127">입력</span><span class="sxs-lookup"><span data-stu-id="d3ce0-127">INPUTS</span></span>

## <span data-ttu-id="d3ce0-128">출력</span><span class="sxs-lookup"><span data-stu-id="d3ce0-128">OUTPUTS</span></span>

## <span data-ttu-id="d3ce0-129">상속자</span><span class="sxs-lookup"><span data-stu-id="d3ce0-129">NOTES</span></span>

## <span data-ttu-id="d3ce0-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d3ce0-130">RELATED LINKS</span></span>

[<span data-ttu-id="d3ce0-131">Get-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="d3ce0-131">Get-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Get-AzureVirtualNetworkGatewayDiagnostics.md)

[<span data-ttu-id="d3ce0-132">중지-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="d3ce0-132">Stop-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Stop-AzureVirtualNetworkGatewayDiagnostics.md)


