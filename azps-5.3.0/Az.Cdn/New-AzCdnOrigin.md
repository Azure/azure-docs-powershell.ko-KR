---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
ms.openlocfilehash: a9ef1687333851e2ac67dfb3f0146509f3b77183
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493977"
---
# <span data-ttu-id="57fa1-101">New-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="57fa1-101">New-AzCdnOrigin</span></span>

## <span data-ttu-id="57fa1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57fa1-102">SYNOPSIS</span></span>
<span data-ttu-id="57fa1-103">새 CDN 원본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="57fa1-103">Creates a new CDN origin</span></span>

## <span data-ttu-id="57fa1-104">구문</span><span class="sxs-lookup"><span data-stu-id="57fa1-104">SYNTAX</span></span>

### <span data-ttu-id="57fa1-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="57fa1-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="57fa1-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="57fa1-106">ByFieldsPrivateLinkParameterSet</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="57fa1-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="57fa1-107">ByObjectParameterSet</span></span>
```
New-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57fa1-108">설명</span><span class="sxs-lookup"><span data-stu-id="57fa1-108">DESCRIPTION</span></span>
<span data-ttu-id="57fa1-109">이 New-AzCdnOrigin 지정된 엔드포인트 내에 새 CDN 원본을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="57fa1-109">The New-AzCdnOrigin will create a new CDN origin within the specified endpoint.</span></span>

## <span data-ttu-id="57fa1-110">예제</span><span class="sxs-lookup"><span data-stu-id="57fa1-110">EXAMPLES</span></span>

### <span data-ttu-id="57fa1-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="57fa1-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName -HostName $hostName
```

<span data-ttu-id="57fa1-112">이 cmdlet은 지정된 엔드포인트에 대한 새 CDN 원본을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="57fa1-112">This cmdlet will create a new CDN origin for the specified endpoint.</span></span> <span data-ttu-id="57fa1-113">제공된 호스트 이름을 원본으로 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="57fa1-113">It will use the provided hostname as the origin.</span></span> 

## <span data-ttu-id="57fa1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57fa1-114">PARAMETERS</span></span>

### <span data-ttu-id="57fa1-115">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="57fa1-115">-CdnOrigin</span></span>
<span data-ttu-id="57fa1-116">CDN 원본 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="57fa1-116">The CDN origin object.</span></span>

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

### <span data-ttu-id="57fa1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57fa1-117">-DefaultProfile</span></span>
<span data-ttu-id="57fa1-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="57fa1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57fa1-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="57fa1-119">-EndpointName</span></span>
<span data-ttu-id="57fa1-120">Azure CDN 엔드포인트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57fa1-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="57fa1-121">-HostName</span><span class="sxs-lookup"><span data-stu-id="57fa1-121">-HostName</span></span>
<span data-ttu-id="57fa1-122">Azure CDN 원본 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57fa1-122">Azure CDN origin host name.</span></span>

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

### <span data-ttu-id="57fa1-123">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="57fa1-123">-HttpPort</span></span>
<span data-ttu-id="57fa1-124">Azure CDN 원본 http 포트.</span><span class="sxs-lookup"><span data-stu-id="57fa1-124">Azure CDN origin http port.</span></span>

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

### <span data-ttu-id="57fa1-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="57fa1-125">-HttpsPort</span></span>
<span data-ttu-id="57fa1-126">Azure CDN 원본 https 포트.</span><span class="sxs-lookup"><span data-stu-id="57fa1-126">Azure CDN origin https port.</span></span>

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

### <span data-ttu-id="57fa1-127">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="57fa1-127">-OriginHostHeader</span></span>
<span data-ttu-id="57fa1-128">Azure CDN 원본 호스트 헤더입니다.</span><span class="sxs-lookup"><span data-stu-id="57fa1-128">Azure CDN origin host header.</span></span>

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

### <span data-ttu-id="57fa1-129">-OriginName</span><span class="sxs-lookup"><span data-stu-id="57fa1-129">-OriginName</span></span>
<span data-ttu-id="57fa1-130">Azure CDN 원본 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57fa1-130">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="57fa1-131">-Priority</span><span class="sxs-lookup"><span data-stu-id="57fa1-131">-Priority</span></span>
<span data-ttu-id="57fa1-132">Azure CDN 원본 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="57fa1-132">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="57fa1-133">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="57fa1-133">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="57fa1-134">개인 링크에 연결하기 위한 승인 요청에 포함될 사용자 지정 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="57fa1-134">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="57fa1-135">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="57fa1-135">-PrivateLinkLocation</span></span>
<span data-ttu-id="57fa1-136">Azure CDN 원본 개인 링크 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="57fa1-136">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="57fa1-137">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="57fa1-137">-PrivateLinkResourceId</span></span>
<span data-ttu-id="57fa1-138">Azure CDN 원본 개인 링크 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="57fa1-138">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="57fa1-139">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="57fa1-139">-ProfileName</span></span>
<span data-ttu-id="57fa1-140">Azure CDN 프로필 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="57fa1-140">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="57fa1-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57fa1-141">-ResourceGroupName</span></span>
<span data-ttu-id="57fa1-142">Azure CDN 프로필의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="57fa1-142">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="57fa1-143">-Weight</span><span class="sxs-lookup"><span data-stu-id="57fa1-143">-Weight</span></span>
<span data-ttu-id="57fa1-144">Azure CDN 원본 가중치입니다.</span><span class="sxs-lookup"><span data-stu-id="57fa1-144">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="57fa1-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57fa1-145">-Confirm</span></span>
<span data-ttu-id="57fa1-146">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="57fa1-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57fa1-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57fa1-147">-WhatIf</span></span>
<span data-ttu-id="57fa1-148">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="57fa1-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="57fa1-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="57fa1-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57fa1-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57fa1-150">CommonParameters</span></span>
<span data-ttu-id="57fa1-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="57fa1-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57fa1-152">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="57fa1-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57fa1-153">입력</span><span class="sxs-lookup"><span data-stu-id="57fa1-153">INPUTS</span></span>

### <span data-ttu-id="57fa1-154">없음</span><span class="sxs-lookup"><span data-stu-id="57fa1-154">None</span></span>

## <span data-ttu-id="57fa1-155">출력</span><span class="sxs-lookup"><span data-stu-id="57fa1-155">OUTPUTS</span></span>

### <span data-ttu-id="57fa1-156">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="57fa1-156">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="57fa1-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="57fa1-157">NOTES</span></span>

## <span data-ttu-id="57fa1-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57fa1-158">RELATED LINKS</span></span>
