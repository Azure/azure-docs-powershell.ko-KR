---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
ms.openlocfilehash: 8eee112840fa7d7af81838927017b38988c9649b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493015"
---
# <span data-ttu-id="7a527-101">New-AzFrontDoorBackendObject</span><span class="sxs-lookup"><span data-stu-id="7a527-101">New-AzFrontDoorBackendObject</span></span>

## <span data-ttu-id="7a527-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a527-102">SYNOPSIS</span></span>
<span data-ttu-id="7a527-103">PSBackend 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="7a527-103">Create a PSBackend object</span></span>

## <span data-ttu-id="7a527-104">구문</span><span class="sxs-lookup"><span data-stu-id="7a527-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>] [-Priority <Int32>]
 [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>] [-PrivateLinkAlias <String>]
 [-PrivateLinkResourceId <String>] [-PrivateLinkLocation <String>] [-PrivateLinkApprovalMessage <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a527-105">설명</span><span class="sxs-lookup"><span data-stu-id="7a527-105">DESCRIPTION</span></span>
<span data-ttu-id="7a527-106">Front Door 만들기를 위한 PSBackend 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="7a527-106">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="7a527-107">예제</span><span class="sxs-lookup"><span data-stu-id="7a527-107">EXAMPLES</span></span>

### <span data-ttu-id="7a527-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7a527-108">Example 1</span></span>
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

<span data-ttu-id="7a527-109">Front Door 만들기를 위한 PSBackend 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="7a527-109">Create a PSBackend object for Front Door creation</span></span>

## <span data-ttu-id="7a527-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a527-110">PARAMETERS</span></span>

### <span data-ttu-id="7a527-111">-Address</span><span class="sxs-lookup"><span data-stu-id="7a527-111">-Address</span></span>
<span data-ttu-id="7a527-112">백end의 위치(IP 주소 또는 FQDN)</span><span class="sxs-lookup"><span data-stu-id="7a527-112">Location of the backend (IP address or FQDN)</span></span>

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

### <span data-ttu-id="7a527-113">-BackendHostHeader</span><span class="sxs-lookup"><span data-stu-id="7a527-113">-BackendHostHeader</span></span>
<span data-ttu-id="7a527-114">백end로 전송된 호스트 헤더로 사용할 값입니다.</span><span class="sxs-lookup"><span data-stu-id="7a527-114">The value to use as the host header sent to the backend.</span></span> <span data-ttu-id="7a527-115">기본값은 백end 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="7a527-115">Default value is the backend address.</span></span>

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

### <span data-ttu-id="7a527-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a527-116">-DefaultProfile</span></span>
<span data-ttu-id="7a527-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7a527-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a527-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="7a527-118">-EnabledState</span></span>
<span data-ttu-id="7a527-119">이 백end의 사용을 사용하도록 설정할지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="7a527-119">Whether to enable use of this backend.</span></span> <span data-ttu-id="7a527-120">기본값이 사용하도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a527-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="7a527-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="7a527-121">-HttpPort</span></span>
<span data-ttu-id="7a527-122">HTTP TCP 포트 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="7a527-122">The HTTP TCP port number.</span></span>
<span data-ttu-id="7a527-123">1에서 65535 사이로 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a527-123">Must be between 1 and 65535.</span></span>
<span data-ttu-id="7a527-124">기본값은 80입니다.</span><span class="sxs-lookup"><span data-stu-id="7a527-124">Default value is 80.</span></span>

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

### <span data-ttu-id="7a527-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="7a527-125">-HttpsPort</span></span>
<span data-ttu-id="7a527-126">HTTPS TCP 포트 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="7a527-126">The HTTPS TCP port number.</span></span>
<span data-ttu-id="7a527-127">1에서 65535 사이로 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a527-127">Must be between 1 and 65535.</span></span>
<span data-ttu-id="7a527-128">기본값은 443입니다.</span><span class="sxs-lookup"><span data-stu-id="7a527-128">Default value is 443</span></span>

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

### <span data-ttu-id="7a527-129">-Priority</span><span class="sxs-lookup"><span data-stu-id="7a527-129">-Priority</span></span>
<span data-ttu-id="7a527-130">부하 분산에 사용할 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="7a527-130">Priority to use for load balancing.</span></span>
<span data-ttu-id="7a527-131">1에서 5 사이로 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a527-131">Must be between 1 and 5.</span></span>
<span data-ttu-id="7a527-132">기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="7a527-132">Default value is 1</span></span>

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

### <span data-ttu-id="7a527-133">-PrivateLinkAlias</span><span class="sxs-lookup"><span data-stu-id="7a527-133">-PrivateLinkAlias</span></span>
<span data-ttu-id="7a527-134">개인 링크 리소스의 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="7a527-134">The Alias of the Private Link resource.</span></span> <span data-ttu-id="7a527-135">이 선택적 필드를 채우면 이 백안이 '비공개'입니다.</span><span class="sxs-lookup"><span data-stu-id="7a527-135">Populating this optional field indicates that this backend is 'Private'</span></span>

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

### <span data-ttu-id="7a527-136">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="7a527-136">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="7a527-137">개인 링크에 연결하기 위한 승인 요청에 포함될 사용자 지정 메시지</span><span class="sxs-lookup"><span data-stu-id="7a527-137">A custom message to be included in the approval request to connect to the Private Link</span></span>

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

### <span data-ttu-id="7a527-138">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="7a527-138">-PrivateLinkLocation</span></span>
<span data-ttu-id="7a527-139">개인 링크 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="7a527-139">The Location of Private Link resource.</span></span> <span data-ttu-id="7a527-140">PrivateLinkResourceId가 설정된 경우 위치가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="7a527-140">Location is required when PrivateLinkResourceId is set</span></span>

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

### <span data-ttu-id="7a527-141">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="7a527-141">-PrivateLinkResourceId</span></span>
<span data-ttu-id="7a527-142">개인 링크의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7a527-142">The Resource ID of the Private Link.</span></span> <span data-ttu-id="7a527-143">이 선택적 필드를 채우면 이 백안이 '비공개'입니다.</span><span class="sxs-lookup"><span data-stu-id="7a527-143">Populating this optional field indicates that this backend is 'Private'</span></span>

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

### <span data-ttu-id="7a527-144">-Weight</span><span class="sxs-lookup"><span data-stu-id="7a527-144">-Weight</span></span>
<span data-ttu-id="7a527-145">부하 분산을 위해 이 엔드포인트의 가중치입니다.</span><span class="sxs-lookup"><span data-stu-id="7a527-145">Weight of this endpoint for load balancing purposes.</span></span>
<span data-ttu-id="7a527-146">1에서 1000 사이로 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a527-146">Must be between 1 and 1000.</span></span>
<span data-ttu-id="7a527-147">기본값은 50입니다.</span><span class="sxs-lookup"><span data-stu-id="7a527-147">Default value is 50</span></span>

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

### <span data-ttu-id="7a527-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a527-148">CommonParameters</span></span>
<span data-ttu-id="7a527-149">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7a527-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a527-150">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7a527-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a527-151">입력</span><span class="sxs-lookup"><span data-stu-id="7a527-151">INPUTS</span></span>

### <span data-ttu-id="7a527-152">없음</span><span class="sxs-lookup"><span data-stu-id="7a527-152">None</span></span>

## <span data-ttu-id="7a527-153">출력</span><span class="sxs-lookup"><span data-stu-id="7a527-153">OUTPUTS</span></span>

### <span data-ttu-id="7a527-154">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span><span class="sxs-lookup"><span data-stu-id="7a527-154">Microsoft.Azure.Commands.FrontDoor.Models.PSBackend</span></span>

## <span data-ttu-id="7a527-155">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7a527-155">NOTES</span></span>

## <span data-ttu-id="7a527-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7a527-156">RELATED LINKS</span></span>

[<span data-ttu-id="7a527-157">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="7a527-157">New-AzFrontDoorBackendPoolObject</span></span>](./New-AzFrontDoorBackendPoolObject.md)
