---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9FCECA04-9855-461C-9470-85312993C4B1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5bb7bb3e708720b481edc4489d858c70736eac95
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046026"
---
# <span data-ttu-id="c61ac-101">Start-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="c61ac-101">Start-AzureVNetGatewayDiagnostics</span></span>

## <span data-ttu-id="c61ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c61ac-102">SYNOPSIS</span></span>
<span data-ttu-id="c61ac-103">VPN 게이트웨이에 대 한 게이트웨이 진단을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c61ac-103">Starts gateway diagnostics for a VPN gateway.</span></span>

## <span data-ttu-id="c61ac-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c61ac-104">SYNTAX</span></span>

```
Start-AzureVNetGatewayDiagnostics -VNetName <String> -CaptureDurationInSeconds <Int32>
 [-ContainerName <String>] -StorageContext <AzureStorageContext> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="c61ac-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c61ac-105">DESCRIPTION</span></span>
<span data-ttu-id="c61ac-106">**시작-Azurevnet2| 진단** cmdlet은 가상 개인 네트워크 (VPN) 게이트웨이에 대 한 새 게이트웨이 진단 세션을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c61ac-106">The **Start-AzureVNetGatewayDiagnostics** cmdlet starts a new gateway diagnostics session for a virtual private network (VPN) gateway.</span></span>
<span data-ttu-id="c61ac-107">게이트웨이 진단 세션은 한 번에 하나만 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c61ac-107">Only one gateway diagnostics session can run at a time.</span></span>
<span data-ttu-id="c61ac-108">게이트웨이 진단 세션이 실행 되는 동안이 cmdlet을 실행 하면이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c61ac-108">If you run this cmdlet while a gateway diagnostics session is running, this cmdlet returns an error.</span></span>

## <span data-ttu-id="c61ac-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c61ac-109">EXAMPLES</span></span>

## <span data-ttu-id="c61ac-110">변수</span><span class="sxs-lookup"><span data-stu-id="c61ac-110">PARAMETERS</span></span>

### <span data-ttu-id="c61ac-111">-CaptureDurationInSeconds</span><span class="sxs-lookup"><span data-stu-id="c61ac-111">-CaptureDurationInSeconds</span></span>
<span data-ttu-id="c61ac-112">캡처 지속 시간 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c61ac-112">Specifies the capture duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c61ac-113">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="c61ac-113">-ContainerName</span></span>
<span data-ttu-id="c61ac-114">Azure 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c61ac-114">Specifies the name of an Azure container.</span></span>
<span data-ttu-id="c61ac-115">이 cmdlet은이 매개 변수에서 지정 하는 컨테이너에 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c61ac-115">This cmdlet stores results in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="c61ac-116">-프로필</span><span class="sxs-lookup"><span data-stu-id="c61ac-116">-Profile</span></span>
<span data-ttu-id="c61ac-117">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c61ac-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="c61ac-118">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="c61ac-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c61ac-119">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="c61ac-119">-StorageContext</span></span>
<span data-ttu-id="c61ac-120">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c61ac-120">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c61ac-121">이 cmdlet은이 매개 변수에서 지정 하는 저장소 컨텍스트를 사용 하 여 결과를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c61ac-121">This cmdlet stores results by using the storage context that this parameter specifies.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c61ac-122">-VNetName</span><span class="sxs-lookup"><span data-stu-id="c61ac-122">-VNetName</span></span>
<span data-ttu-id="c61ac-123">이 cmdlet이 진단 유틸리티를 실행 하는 가상 네트워크 게이트웨이를 포함 하는 가상 네트워크를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c61ac-123">Specifies the virtual network that contains a virtual network gateway for which this cmdlet runs diagnostics.</span></span>

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

### <span data-ttu-id="c61ac-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c61ac-124">CommonParameters</span></span>
<span data-ttu-id="c61ac-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c61ac-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c61ac-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c61ac-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c61ac-127">입력</span><span class="sxs-lookup"><span data-stu-id="c61ac-127">INPUTS</span></span>

## <span data-ttu-id="c61ac-128">출력</span><span class="sxs-lookup"><span data-stu-id="c61ac-128">OUTPUTS</span></span>

## <span data-ttu-id="c61ac-129">상속자</span><span class="sxs-lookup"><span data-stu-id="c61ac-129">NOTES</span></span>

## <span data-ttu-id="c61ac-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c61ac-130">RELATED LINKS</span></span>

[<span data-ttu-id="c61ac-131">Get-Azurevnet게이트웨이 진단</span><span class="sxs-lookup"><span data-stu-id="c61ac-131">Get-AzureVNetGatewayDiagnostics</span></span>](./Get-AzureVNetGatewayDiagnostics.md)

[<span data-ttu-id="c61ac-132">중지-Azurevnet2| 진단</span><span class="sxs-lookup"><span data-stu-id="c61ac-132">Stop-AzureVNetGatewayDiagnostics</span></span>](./Stop-AzureVNetGatewayDiagnostics.md)


