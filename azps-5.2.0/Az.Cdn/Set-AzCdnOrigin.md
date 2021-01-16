---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 1c3b195f868db5d4e579aa833c4d9ce5a6203c56
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366122"
---
# <span data-ttu-id="f85c5-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="f85c5-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="f85c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f85c5-102">SYNOPSIS</span></span>
<span data-ttu-id="f85c5-103">CDN 원본 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f85c5-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="f85c5-104">구문</span><span class="sxs-lookup"><span data-stu-id="f85c5-104">SYNTAX</span></span>

### <span data-ttu-id="f85c5-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f85c5-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f85c5-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="f85c5-106">ByFieldsPrivateLinkParameterSet</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f85c5-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f85c5-107">ByObjectParameterSet</span></span>
```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f85c5-108">설명</span><span class="sxs-lookup"><span data-stu-id="f85c5-108">DESCRIPTION</span></span>
<span data-ttu-id="f85c5-109">**Set-AzCdnOrigin** cmdlet은 Azure CDN(Content Delivery Network) 원본 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f85c5-109">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="f85c5-110">예제</span><span class="sxs-lookup"><span data-stu-id="f85c5-110">EXAMPLES</span></span>

## <span data-ttu-id="f85c5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f85c5-111">PARAMETERS</span></span>

### <span data-ttu-id="f85c5-112">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="f85c5-112">-CdnOrigin</span></span>
<span data-ttu-id="f85c5-113">이 cmdlet이 업데이트하는 원본 서버를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f85c5-113">Specifies the origin server that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f85c5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f85c5-114">-DefaultProfile</span></span>
<span data-ttu-id="f85c5-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f85c5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f85c5-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="f85c5-116">-EndpointName</span></span>
<span data-ttu-id="f85c5-117">Azure CDN 엔드포인트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f85c5-117">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f85c5-118">-HostName</span><span class="sxs-lookup"><span data-stu-id="f85c5-118">-HostName</span></span>
<span data-ttu-id="f85c5-119">Azure CDN 원본 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f85c5-119">Azure CDN origin host name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f85c5-120">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="f85c5-120">-HttpPort</span></span>
<span data-ttu-id="f85c5-121">Azure CDN 원본 http 포트.</span><span class="sxs-lookup"><span data-stu-id="f85c5-121">Azure CDN origin http port.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f85c5-122">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="f85c5-122">-HttpsPort</span></span>
<span data-ttu-id="f85c5-123">Azure CDN 원본 https 포트.</span><span class="sxs-lookup"><span data-stu-id="f85c5-123">Azure CDN origin https port.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f85c5-124">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="f85c5-124">-OriginHostHeader</span></span>
<span data-ttu-id="f85c5-125">Azure CDN 원본 호스트 헤더입니다.</span><span class="sxs-lookup"><span data-stu-id="f85c5-125">Azure CDN origin host header.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f85c5-126">-OriginName</span><span class="sxs-lookup"><span data-stu-id="f85c5-126">-OriginName</span></span>
<span data-ttu-id="f85c5-127">Azure CDN 원본 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f85c5-127">Azure CDN origin name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f85c5-128">-Priority</span><span class="sxs-lookup"><span data-stu-id="f85c5-128">-Priority</span></span>
<span data-ttu-id="f85c5-129">Azure CDN 원본 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="f85c5-129">Azure CDN origin priority.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f85c5-130">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="f85c5-130">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="f85c5-131">개인 링크에 연결하기 위한 승인 요청에 포함될 사용자 지정 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="f85c5-131">A custom message to be included in the approval request to connect to the Private Link.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f85c5-132">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="f85c5-132">-PrivateLinkLocation</span></span>
<span data-ttu-id="f85c5-133">Azure CDN 원본 개인 링크 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="f85c5-133">Azure CDN origin private link location.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f85c5-134">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="f85c5-134">-PrivateLinkResourceId</span></span>
<span data-ttu-id="f85c5-135">Azure CDN 원본 개인 링크 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f85c5-135">Azure CDN origin private link resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f85c5-136">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="f85c5-136">-ProfileName</span></span>
<span data-ttu-id="f85c5-137">Azure CDN 프로필 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f85c5-137">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f85c5-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f85c5-138">-ResourceGroupName</span></span>
<span data-ttu-id="f85c5-139">Azure CDN 프로필의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="f85c5-139">The resource group of the Azure CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f85c5-140">-Weight</span><span class="sxs-lookup"><span data-stu-id="f85c5-140">-Weight</span></span>
<span data-ttu-id="f85c5-141">Azure CDN 원본 가중치입니다.</span><span class="sxs-lookup"><span data-stu-id="f85c5-141">Azure CDN origin weight.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f85c5-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f85c5-142">-Confirm</span></span>
<span data-ttu-id="f85c5-143">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f85c5-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f85c5-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f85c5-144">-WhatIf</span></span>
<span data-ttu-id="f85c5-145">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f85c5-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f85c5-146">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f85c5-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f85c5-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f85c5-147">CommonParameters</span></span>
<span data-ttu-id="f85c5-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f85c5-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f85c5-149">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f85c5-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f85c5-150">입력</span><span class="sxs-lookup"><span data-stu-id="f85c5-150">INPUTS</span></span>

### <span data-ttu-id="f85c5-151">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="f85c5-151">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="f85c5-152">출력</span><span class="sxs-lookup"><span data-stu-id="f85c5-152">OUTPUTS</span></span>

### <span data-ttu-id="f85c5-153">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="f85c5-153">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="f85c5-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f85c5-154">NOTES</span></span>

## <span data-ttu-id="f85c5-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f85c5-155">RELATED LINKS</span></span>

[<span data-ttu-id="f85c5-156">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="f85c5-156">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)


