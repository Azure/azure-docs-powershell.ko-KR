---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 1c3b195f868db5d4e579aa833c4d9ce5a6203c56
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217644"
---
# <span data-ttu-id="226b2-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="226b2-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="226b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="226b2-102">SYNOPSIS</span></span>
<span data-ttu-id="226b2-103">CDN 원본 서버를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="226b2-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="226b2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="226b2-104">SYNTAX</span></span>

### <span data-ttu-id="226b2-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="226b2-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="226b2-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="226b2-106">ByFieldsPrivateLinkParameterSet</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="226b2-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="226b2-107">ByObjectParameterSet</span></span>
```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="226b2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="226b2-108">DESCRIPTION</span></span>
<span data-ttu-id="226b2-109">**AzCdnOrigin** Cmdlet은 Azure CDN (콘텐츠 배달 네트워크) 원본 서버를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="226b2-109">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="226b2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="226b2-110">EXAMPLES</span></span>

## <span data-ttu-id="226b2-111">변수</span><span class="sxs-lookup"><span data-stu-id="226b2-111">PARAMETERS</span></span>

### <span data-ttu-id="226b2-112">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="226b2-112">-CdnOrigin</span></span>
<span data-ttu-id="226b2-113">이 cmdlet이 업데이트 하는 원본 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="226b2-113">Specifies the origin server that this cmdlet updates.</span></span>

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

### <span data-ttu-id="226b2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="226b2-114">-DefaultProfile</span></span>
<span data-ttu-id="226b2-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="226b2-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="226b2-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="226b2-116">-EndpointName</span></span>
<span data-ttu-id="226b2-117">Azure CDN 끝점 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="226b2-117">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="226b2-118">-HostName</span><span class="sxs-lookup"><span data-stu-id="226b2-118">-HostName</span></span>
<span data-ttu-id="226b2-119">Azure CDN 원본 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="226b2-119">Azure CDN origin host name.</span></span>

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

### <span data-ttu-id="226b2-120">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="226b2-120">-HttpPort</span></span>
<span data-ttu-id="226b2-121">Azure CDN 원본 http 포트.</span><span class="sxs-lookup"><span data-stu-id="226b2-121">Azure CDN origin http port.</span></span>

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

### <span data-ttu-id="226b2-122">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="226b2-122">-HttpsPort</span></span>
<span data-ttu-id="226b2-123">Azure CDN 원본 https 포트.</span><span class="sxs-lookup"><span data-stu-id="226b2-123">Azure CDN origin https port.</span></span>

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

### <span data-ttu-id="226b2-124">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="226b2-124">-OriginHostHeader</span></span>
<span data-ttu-id="226b2-125">Azure CDN 원본 호스트 헤더.</span><span class="sxs-lookup"><span data-stu-id="226b2-125">Azure CDN origin host header.</span></span>

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

### <span data-ttu-id="226b2-126">-OriginName</span><span class="sxs-lookup"><span data-stu-id="226b2-126">-OriginName</span></span>
<span data-ttu-id="226b2-127">Azure CDN 원본 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="226b2-127">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="226b2-128">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="226b2-128">-Priority</span></span>
<span data-ttu-id="226b2-129">Azure CDN 원본 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="226b2-129">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="226b2-130">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="226b2-130">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="226b2-131">개인 링크에 연결 하기 위해 승인 요청에 포함할 사용자 지정 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="226b2-131">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="226b2-132">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="226b2-132">-PrivateLinkLocation</span></span>
<span data-ttu-id="226b2-133">Azure CDN 원본 개인 링크 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="226b2-133">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="226b2-134">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="226b2-134">-PrivateLinkResourceId</span></span>
<span data-ttu-id="226b2-135">Azure CDN 원본 개인 링크 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="226b2-135">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="226b2-136">-/Profile</span><span class="sxs-lookup"><span data-stu-id="226b2-136">-ProfileName</span></span>
<span data-ttu-id="226b2-137">Azure CDN 프로필 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="226b2-137">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="226b2-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="226b2-138">-ResourceGroupName</span></span>
<span data-ttu-id="226b2-139">Azure CDN 프로필의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="226b2-139">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="226b2-140">-중량</span><span class="sxs-lookup"><span data-stu-id="226b2-140">-Weight</span></span>
<span data-ttu-id="226b2-141">Azure CDN 원본 가중치.</span><span class="sxs-lookup"><span data-stu-id="226b2-141">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="226b2-142">-확인</span><span class="sxs-lookup"><span data-stu-id="226b2-142">-Confirm</span></span>
<span data-ttu-id="226b2-143">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="226b2-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="226b2-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="226b2-144">-WhatIf</span></span>
<span data-ttu-id="226b2-145">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="226b2-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="226b2-146">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="226b2-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="226b2-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="226b2-147">CommonParameters</span></span>
<span data-ttu-id="226b2-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="226b2-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="226b2-149">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="226b2-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="226b2-150">입력</span><span class="sxs-lookup"><span data-stu-id="226b2-150">INPUTS</span></span>

### <span data-ttu-id="226b2-151">Microsoft. Cdn. 원본 PSOrigin</span><span class="sxs-lookup"><span data-stu-id="226b2-151">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="226b2-152">출력</span><span class="sxs-lookup"><span data-stu-id="226b2-152">OUTPUTS</span></span>

### <span data-ttu-id="226b2-153">Microsoft. Cdn. 원본 PSOrigin</span><span class="sxs-lookup"><span data-stu-id="226b2-153">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="226b2-154">상속자</span><span class="sxs-lookup"><span data-stu-id="226b2-154">NOTES</span></span>

## <span data-ttu-id="226b2-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="226b2-155">RELATED LINKS</span></span>

[<span data-ttu-id="226b2-156">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="226b2-156">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)


