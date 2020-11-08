---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
ms.openlocfilehash: 8eee112840fa7d7af81838927017b38988c9649b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213579"
---
# <span data-ttu-id="d932e-101">New-AzFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="d932e-101">New-AzFrontDoorBackendObject</span></span>

## <span data-ttu-id="d932e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d932e-102">SYNOPSIS</span></span>
<span data-ttu-id="d932e-103">PSBackend 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="d932e-103">Create a PSBackend object</span></span>

## <span data-ttu-id="d932e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d932e-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>] [-Priority <Int32>]
 [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>] [-PrivateLinkAlias <String>]
 [-PrivateLinkResourceId <String>] [-PrivateLinkLocation <String>] [-PrivateLinkApprovalMessage <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d932e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d932e-105">DESCRIPTION</span></span>
<span data-ttu-id="d932e-106">전방 문 생성을 위한 PSBackend 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="d932e-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="d932e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d932e-107">EXAMPLES</span></span>

### <span data-ttu-id="d932e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d932e-108">Example 1</span></span>
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

<span data-ttu-id="d932e-109">전방 문 생성을 위한 PSBackend 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="d932e-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="d932e-110">변수</span><span class="sxs-lookup"><span data-stu-id="d932e-110">PARAMETERS</span></span>

### <span data-ttu-id="d932e-111">-주소</span><span class="sxs-lookup"><span data-stu-id="d932e-111">-Address</span></span>
<span data-ttu-id="d932e-112">백 엔드의 위치 (IP 주소 또는 FQDN)</span><span class="sxs-lookup"><span data-stu-id="d932e-112">Location of the backend (IP address or FQDN)</span></span>

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

### <span data-ttu-id="d932e-113">-BackendHostHeader</span><span class="sxs-lookup"><span data-stu-id="d932e-113">-BackendHostHeader</span></span>
<span data-ttu-id="d932e-114">백 엔드로 전송 되는 호스트 헤더로 사용할 값입니다.</span><span class="sxs-lookup"><span data-stu-id="d932e-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="d932e-115">기본 값은 백 엔드 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="d932e-115">Default value is the backend address.</span></span>

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

### <span data-ttu-id="d932e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d932e-116">-DefaultProfile</span></span>
<span data-ttu-id="d932e-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d932e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d932e-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="d932e-118">-EnabledState</span></span>
<span data-ttu-id="d932e-119">이 백엔드 사용을 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d932e-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="d932e-120">기본값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d932e-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="d932e-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="d932e-121">-HttpPort</span></span>
<span data-ttu-id="d932e-122">HTTP TCP 포트 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="d932e-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="d932e-123">1에서 65535 사이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d932e-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="d932e-124">기본값은 80입니다.</span><span class="sxs-lookup"><span data-stu-id="d932e-124">Default value is 80.</span></span>

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

### <span data-ttu-id="d932e-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="d932e-125">-HttpsPort</span></span>
<span data-ttu-id="d932e-126">HTTPS TCP 포트 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="d932e-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="d932e-127">1에서 65535 사이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d932e-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="d932e-128">기본값은 443입니다.</span><span class="sxs-lookup"><span data-stu-id="d932e-128">Default value is 443</span></span>

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

### <span data-ttu-id="d932e-129">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="d932e-129">-Priority</span></span>
<span data-ttu-id="d932e-130">부하 분산에 사용 하는 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="d932e-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="d932e-131">1에서 5 사이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d932e-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="d932e-132">기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="d932e-132">Default value is 1</span></span>

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

### <span data-ttu-id="d932e-133">-PrivateLinkAlias</span><span class="sxs-lookup"><span data-stu-id="d932e-133">-PrivateLinkAlias</span></span>
<span data-ttu-id="d932e-134">개인 링크 리소스의 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="d932e-134">The Alias of the Private Link resource.</span></span> <span data-ttu-id="d932e-135">이 선택적 필드를 채우면이 백 엔드가 ' Private ' 상태임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d932e-135">Populating this optional field indicates that this backend is 'Private'</span></span>

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

### <span data-ttu-id="d932e-136">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="d932e-136">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="d932e-137">비공개 링크에 연결 하기 위해 승인 요청에 포함할 사용자 지정 메시지</span><span class="sxs-lookup"><span data-stu-id="d932e-137">A custom message to be included in the approval request to connect to the Private Link</span></span>

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

### <span data-ttu-id="d932e-138">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="d932e-138">-PrivateLinkLocation</span></span>
<span data-ttu-id="d932e-139">비공개 링크 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="d932e-139">The Location of Private Link resource.</span></span> <span data-ttu-id="d932e-140">PrivateLinkResourceId가 설정 된 경우 위치가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="d932e-140">Location is required when PrivateLinkResourceId is set</span></span>

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

### <span data-ttu-id="d932e-141">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="d932e-141">-PrivateLinkResourceId</span></span>
<span data-ttu-id="d932e-142">개인 링크의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d932e-142">The Resource ID of the Private Link.</span></span> <span data-ttu-id="d932e-143">이 선택적 필드를 채우면이 백 엔드가 ' Private ' 상태임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d932e-143">Populating this optional field indicates that this backend is 'Private'</span></span>

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

### <span data-ttu-id="d932e-144">-중량</span><span class="sxs-lookup"><span data-stu-id="d932e-144">-Weight</span></span>
<span data-ttu-id="d932e-145">부하 분산을 위해이 끝점의 가중치입니다.</span><span class="sxs-lookup"><span data-stu-id="d932e-145">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="d932e-146">1에서 1000 사이 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d932e-146">Must be between 1 and 1000.</span></span>
<span data-ttu-id="d932e-147">기본값은 50입니다.</span><span class="sxs-lookup"><span data-stu-id="d932e-147">Default value is 50</span></span>

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

### <span data-ttu-id="d932e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d932e-148">CommonParameters</span></span>
<span data-ttu-id="d932e-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d932e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d932e-150">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d932e-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d932e-151">입력</span><span class="sxs-lookup"><span data-stu-id="d932e-151">INPUTS</span></span>

### <span data-ttu-id="d932e-152">않아야</span><span class="sxs-lookup"><span data-stu-id="d932e-152">None</span></span>

## <span data-ttu-id="d932e-153">출력</span><span class="sxs-lookup"><span data-stu-id="d932e-153">OUTPUTS</span></span>

### <span data-ttu-id="d932e-154">FrontDoor. m a m/. a i m 백 엔드</span><span class="sxs-lookup"><span data-stu-id="d932e-154">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="d932e-155">상속자</span><span class="sxs-lookup"><span data-stu-id="d932e-155">NOTES</span></span>

## <span data-ttu-id="d932e-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d932e-156">RELATED LINKS</span></span>

[<span data-ttu-id="d932e-157">새로운 AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="d932e-157">New-AzFrontDoorBackendPoolObject</span></span>](./New-AzFrontDoorBackendPoolObject.md)
