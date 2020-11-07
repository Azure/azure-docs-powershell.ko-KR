---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorBackendObject.md
ms.openlocfilehash: 429db1fae2987531911bd4dfbd4c41daf66a5440
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702933"
---
# <span data-ttu-id="88e10-101">New-AzureRmFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="88e10-101">New-AzureRmFrontDoorBackendObject</span></span>

## <span data-ttu-id="88e10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88e10-102">SYNOPSIS</span></span>
<span data-ttu-id="88e10-103">PSBackend 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="88e10-103">Create a PSBackend object</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88e10-104">구문과</span><span class="sxs-lookup"><span data-stu-id="88e10-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-Priority <Int32>] [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88e10-105">설명은</span><span class="sxs-lookup"><span data-stu-id="88e10-105">DESCRIPTION</span></span>
<span data-ttu-id="88e10-106">전방 문 생성을 위한 PSBackend 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="88e10-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="88e10-107">예제의</span><span class="sxs-lookup"><span data-stu-id="88e10-107">EXAMPLES</span></span>

### <span data-ttu-id="88e10-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="88e10-108">Example 1</span></span>
```powershell
PS C:\>New-AzureRmFrontDoorBackendObject -Address "contoso1.azurewebsites.net"


Address           : contoso1.azurewebsites.net
HttpPort          : 80
HttpsPort         : 443
Priority          : 1
Weight            : 50
BackendHostHeader :
EnabledState      : Enabled
```

<span data-ttu-id="88e10-109">전방 문 생성을 위한 PSBackend 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="88e10-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="88e10-110">변수</span><span class="sxs-lookup"><span data-stu-id="88e10-110">PARAMETERS</span></span>

### <span data-ttu-id="88e10-111">-주소</span><span class="sxs-lookup"><span data-stu-id="88e10-111">-Address</span></span>
<span data-ttu-id="88e10-112">백 엔드의 위치 (IP 주소 또는 FQDN)</span><span class="sxs-lookup"><span data-stu-id="88e10-112">Location of the backend (IP address or FQDN)</span></span>

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

### <span data-ttu-id="88e10-113">-BackendHostHeader</span><span class="sxs-lookup"><span data-stu-id="88e10-113">-BackendHostHeader</span></span>
<span data-ttu-id="88e10-114">백 엔드로 전송 되는 호스트 헤더로 사용할 값입니다.</span><span class="sxs-lookup"><span data-stu-id="88e10-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="88e10-115">기본 값은 백 엔드 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="88e10-115">Default value is the backend address.</span></span>

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

### <span data-ttu-id="88e10-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88e10-116">-DefaultProfile</span></span>
<span data-ttu-id="88e10-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="88e10-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88e10-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="88e10-118">-EnabledState</span></span>
<span data-ttu-id="88e10-119">이 백엔드 사용을 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88e10-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="88e10-120">기본값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="88e10-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="88e10-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="88e10-121">-HttpPort</span></span>
<span data-ttu-id="88e10-122">HTTP TCP 포트 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="88e10-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="88e10-123">1에서 65535 사이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="88e10-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="88e10-124">기본값은 80입니다.</span><span class="sxs-lookup"><span data-stu-id="88e10-124">Default value is 80.</span></span>

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

### <span data-ttu-id="88e10-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="88e10-125">-HttpsPort</span></span>
<span data-ttu-id="88e10-126">HTTPS TCP 포트 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="88e10-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="88e10-127">1에서 65535 사이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="88e10-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="88e10-128">기본값은 443입니다.</span><span class="sxs-lookup"><span data-stu-id="88e10-128">Default value is 443</span></span>

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

### <span data-ttu-id="88e10-129">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="88e10-129">-Priority</span></span>
<span data-ttu-id="88e10-130">부하 분산에 사용 하는 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="88e10-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="88e10-131">1에서 5 사이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="88e10-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="88e10-132">기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="88e10-132">Default value is 1</span></span>

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

### <span data-ttu-id="88e10-133">-중량</span><span class="sxs-lookup"><span data-stu-id="88e10-133">-Weight</span></span>
<span data-ttu-id="88e10-134">부하 분산을 위해이 끝점의 가중치입니다.</span><span class="sxs-lookup"><span data-stu-id="88e10-134">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="88e10-135">1에서 1000 사이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="88e10-135">Must be between 1 and 1000.</span></span>
<span data-ttu-id="88e10-136">기본값은 50입니다.</span><span class="sxs-lookup"><span data-stu-id="88e10-136">Default value is 50</span></span>

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

### <span data-ttu-id="88e10-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88e10-137">CommonParameters</span></span>
<span data-ttu-id="88e10-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="88e10-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88e10-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88e10-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88e10-140">입력</span><span class="sxs-lookup"><span data-stu-id="88e10-140">INPUTS</span></span>

### <span data-ttu-id="88e10-141">않아야</span><span class="sxs-lookup"><span data-stu-id="88e10-141">None</span></span>

## <span data-ttu-id="88e10-142">출력</span><span class="sxs-lookup"><span data-stu-id="88e10-142">OUTPUTS</span></span>

### <span data-ttu-id="88e10-143">FrontDoor. m a m/. a i m 백 엔드</span><span class="sxs-lookup"><span data-stu-id="88e10-143">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="88e10-144">상속자</span><span class="sxs-lookup"><span data-stu-id="88e10-144">NOTES</span></span>

## <span data-ttu-id="88e10-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88e10-145">RELATED LINKS</span></span>

[<span data-ttu-id="88e10-146">새로운 AzureRmFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="88e10-146">New-AzureRmFrontDoorBackendPoolObject</span></span>](./New-AzureRmFrontDoorBackendPoolObject.md)
