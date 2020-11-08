---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
ms.openlocfilehash: a9ef1687333851e2ac67dfb3f0146509f3b77183
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216265"
---
# <span data-ttu-id="16964-101">New-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="16964-101">New-AzCdnOrigin</span></span>

## <span data-ttu-id="16964-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16964-102">SYNOPSIS</span></span>
<span data-ttu-id="16964-103">새 CDN 원본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="16964-103">Creates a new CDN origin</span></span>

## <span data-ttu-id="16964-104">구문과</span><span class="sxs-lookup"><span data-stu-id="16964-104">SYNTAX</span></span>

### <span data-ttu-id="16964-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="16964-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16964-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="16964-106">ByFieldsPrivateLinkParameterSet</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="16964-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="16964-107">ByObjectParameterSet</span></span>
```
New-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="16964-108">설명은</span><span class="sxs-lookup"><span data-stu-id="16964-108">DESCRIPTION</span></span>
<span data-ttu-id="16964-109">New-AzCdnOrigin에서는 지정 된 끝점 내에 새 CDN 원본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="16964-109">The New-AzCdnOrigin will create a new CDN origin within the specified endpoint.</span></span>

## <span data-ttu-id="16964-110">예제의</span><span class="sxs-lookup"><span data-stu-id="16964-110">EXAMPLES</span></span>

### <span data-ttu-id="16964-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="16964-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName -HostName $hostName
```

<span data-ttu-id="16964-112">이 cmdlet은 지정 된 끝점에 대 한 새 CDN 원본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="16964-112">This cmdlet will create a new CDN origin for the specified endpoint.</span></span> <span data-ttu-id="16964-113">제공 된 호스트 이름이 원점으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="16964-113">It will use the provided hostname as the origin.</span></span> 

## <span data-ttu-id="16964-114">변수</span><span class="sxs-lookup"><span data-stu-id="16964-114">PARAMETERS</span></span>

### <span data-ttu-id="16964-115">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="16964-115">-CdnOrigin</span></span>
<span data-ttu-id="16964-116">CDN 원본 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="16964-116">The CDN origin object.</span></span>

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

### <span data-ttu-id="16964-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16964-117">-DefaultProfile</span></span>
<span data-ttu-id="16964-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="16964-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16964-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="16964-119">-EndpointName</span></span>
<span data-ttu-id="16964-120">Azure CDN 끝점 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16964-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="16964-121">-HostName</span><span class="sxs-lookup"><span data-stu-id="16964-121">-HostName</span></span>
<span data-ttu-id="16964-122">Azure CDN 원본 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16964-122">Azure CDN origin host name.</span></span>

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

### <span data-ttu-id="16964-123">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="16964-123">-HttpPort</span></span>
<span data-ttu-id="16964-124">Azure CDN 원본 http 포트.</span><span class="sxs-lookup"><span data-stu-id="16964-124">Azure CDN origin http port.</span></span>

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

### <span data-ttu-id="16964-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="16964-125">-HttpsPort</span></span>
<span data-ttu-id="16964-126">Azure CDN 원본 https 포트.</span><span class="sxs-lookup"><span data-stu-id="16964-126">Azure CDN origin https port.</span></span>

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

### <span data-ttu-id="16964-127">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="16964-127">-OriginHostHeader</span></span>
<span data-ttu-id="16964-128">Azure CDN 원본 호스트 헤더.</span><span class="sxs-lookup"><span data-stu-id="16964-128">Azure CDN origin host header.</span></span>

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

### <span data-ttu-id="16964-129">-OriginName</span><span class="sxs-lookup"><span data-stu-id="16964-129">-OriginName</span></span>
<span data-ttu-id="16964-130">Azure CDN 원본 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16964-130">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="16964-131">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="16964-131">-Priority</span></span>
<span data-ttu-id="16964-132">Azure CDN 원본 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="16964-132">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="16964-133">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="16964-133">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="16964-134">개인 링크에 연결 하기 위해 승인 요청에 포함할 사용자 지정 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="16964-134">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="16964-135">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="16964-135">-PrivateLinkLocation</span></span>
<span data-ttu-id="16964-136">Azure CDN 원본 개인 링크 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="16964-136">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="16964-137">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="16964-137">-PrivateLinkResourceId</span></span>
<span data-ttu-id="16964-138">Azure CDN 원본 개인 링크 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="16964-138">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="16964-139">-/Profile</span><span class="sxs-lookup"><span data-stu-id="16964-139">-ProfileName</span></span>
<span data-ttu-id="16964-140">Azure CDN 프로필 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16964-140">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="16964-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16964-141">-ResourceGroupName</span></span>
<span data-ttu-id="16964-142">Azure CDN 프로필의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="16964-142">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="16964-143">-중량</span><span class="sxs-lookup"><span data-stu-id="16964-143">-Weight</span></span>
<span data-ttu-id="16964-144">Azure CDN 원본 가중치.</span><span class="sxs-lookup"><span data-stu-id="16964-144">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="16964-145">-확인</span><span class="sxs-lookup"><span data-stu-id="16964-145">-Confirm</span></span>
<span data-ttu-id="16964-146">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="16964-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16964-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16964-147">-WhatIf</span></span>
<span data-ttu-id="16964-148">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="16964-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16964-149">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16964-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16964-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16964-150">CommonParameters</span></span>
<span data-ttu-id="16964-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="16964-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16964-152">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="16964-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16964-153">입력</span><span class="sxs-lookup"><span data-stu-id="16964-153">INPUTS</span></span>

### <span data-ttu-id="16964-154">않아야</span><span class="sxs-lookup"><span data-stu-id="16964-154">None</span></span>

## <span data-ttu-id="16964-155">출력</span><span class="sxs-lookup"><span data-stu-id="16964-155">OUTPUTS</span></span>

### <span data-ttu-id="16964-156">Microsoft. Cdn. 원본 PSOrigin</span><span class="sxs-lookup"><span data-stu-id="16964-156">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="16964-157">상속자</span><span class="sxs-lookup"><span data-stu-id="16964-157">NOTES</span></span>

## <span data-ttu-id="16964-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16964-158">RELATED LINKS</span></span>
