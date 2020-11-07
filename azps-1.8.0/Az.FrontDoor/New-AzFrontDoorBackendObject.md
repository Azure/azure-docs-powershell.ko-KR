---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
ms.openlocfilehash: 5cf730c5ba450978730617b7ddb270c0fdec2bf9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868406"
---
# <span data-ttu-id="dbd7d-101">New-AzFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="dbd7d-101">New-AzFrontDoorBackendObject</span></span>

## <span data-ttu-id="dbd7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbd7d-102">SYNOPSIS</span></span>
<span data-ttu-id="dbd7d-103">PSBackend 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="dbd7d-103">Create a PSBackend object</span></span>

## <span data-ttu-id="dbd7d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dbd7d-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>] [-Priority <Int32>]
 [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbd7d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dbd7d-105">DESCRIPTION</span></span>
<span data-ttu-id="dbd7d-106">전방 문 생성을 위한 PSBackend 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="dbd7d-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="dbd7d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dbd7d-107">EXAMPLES</span></span>

### <span data-ttu-id="dbd7d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="dbd7d-108">Example 1</span></span>
```powershell
PS C:\>New-AzFrontDoorBackendObject -Address "contoso1.azurewebsites.net"


Address           : contoso1.azurewebsites.net
HttpPort          : 80
HttpsPort         : 443
Priority          : 1
Weight            : 50
BackendHostHeader :
EnabledState      : Enabled
```

<span data-ttu-id="dbd7d-109">전방 문 생성을 위한 PSBackend 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="dbd7d-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="dbd7d-110">변수</span><span class="sxs-lookup"><span data-stu-id="dbd7d-110">PARAMETERS</span></span>

### <span data-ttu-id="dbd7d-111">-주소</span><span class="sxs-lookup"><span data-stu-id="dbd7d-111">-Address</span></span>
<span data-ttu-id="dbd7d-112">백 엔드의 위치 (IP 주소 또는 FQDN)</span><span class="sxs-lookup"><span data-stu-id="dbd7d-112">Location of the backend (IP address or FQDN)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbd7d-113">-BackendHostHeader</span><span class="sxs-lookup"><span data-stu-id="dbd7d-113">-BackendHostHeader</span></span>
<span data-ttu-id="dbd7d-114">백 엔드로 전송 되는 호스트 헤더로 사용할 값입니다.</span><span class="sxs-lookup"><span data-stu-id="dbd7d-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="dbd7d-115">기본 값은 백 엔드 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="dbd7d-115">Default value is the backend address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbd7d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbd7d-116">-DefaultProfile</span></span>
<span data-ttu-id="dbd7d-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dbd7d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbd7d-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="dbd7d-118">-EnabledState</span></span>
<span data-ttu-id="dbd7d-119">이 백엔드 사용을 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbd7d-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="dbd7d-120">기본값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbd7d-120">Default value is Enabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbd7d-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="dbd7d-121">-HttpPort</span></span>
<span data-ttu-id="dbd7d-122">HTTP TCP 포트 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="dbd7d-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="dbd7d-123">1에서 65535 사이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbd7d-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="dbd7d-124">기본값은 80입니다.</span><span class="sxs-lookup"><span data-stu-id="dbd7d-124">Default value is 80.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbd7d-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="dbd7d-125">-HttpsPort</span></span>
<span data-ttu-id="dbd7d-126">HTTPS TCP 포트 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="dbd7d-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="dbd7d-127">1에서 65535 사이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbd7d-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="dbd7d-128">기본값은 443입니다.</span><span class="sxs-lookup"><span data-stu-id="dbd7d-128">Default value is 443</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbd7d-129">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="dbd7d-129">-Priority</span></span>
<span data-ttu-id="dbd7d-130">부하 분산에 사용 하는 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="dbd7d-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="dbd7d-131">1에서 5 사이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbd7d-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="dbd7d-132">기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="dbd7d-132">Default value is 1</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbd7d-133">-중량</span><span class="sxs-lookup"><span data-stu-id="dbd7d-133">-Weight</span></span>
<span data-ttu-id="dbd7d-134">부하 분산을 위해이 끝점의 가중치입니다.</span><span class="sxs-lookup"><span data-stu-id="dbd7d-134">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="dbd7d-135">1에서 1000 사이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbd7d-135">Must be between 1 and 1000.</span></span>
<span data-ttu-id="dbd7d-136">기본값은 50입니다.</span><span class="sxs-lookup"><span data-stu-id="dbd7d-136">Default value is 50</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbd7d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbd7d-137">CommonParameters</span></span>
<span data-ttu-id="dbd7d-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbd7d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbd7d-139">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dbd7d-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbd7d-140">입력</span><span class="sxs-lookup"><span data-stu-id="dbd7d-140">INPUTS</span></span>

### <span data-ttu-id="dbd7d-141">않아야</span><span class="sxs-lookup"><span data-stu-id="dbd7d-141">None</span></span>

## <span data-ttu-id="dbd7d-142">출력</span><span class="sxs-lookup"><span data-stu-id="dbd7d-142">OUTPUTS</span></span>

### <span data-ttu-id="dbd7d-143">FrontDoor. m a m/. a i m 백 엔드</span><span class="sxs-lookup"><span data-stu-id="dbd7d-143">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="dbd7d-144">상속자</span><span class="sxs-lookup"><span data-stu-id="dbd7d-144">NOTES</span></span>

## <span data-ttu-id="dbd7d-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dbd7d-145">RELATED LINKS</span></span>

[<span data-ttu-id="dbd7d-146">새로운 AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="dbd7d-146">New-AzFrontDoorBackendPoolObject</span></span>](./New-AzFrontDoorBackendPoolObject.md)
