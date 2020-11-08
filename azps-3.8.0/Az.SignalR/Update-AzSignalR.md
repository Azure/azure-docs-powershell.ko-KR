---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/update-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
ms.openlocfilehash: 52e422f6c86f17c6620c58c1034b45250d4edf08
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034744"
---
# <span data-ttu-id="6f81c-101">Update-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="6f81c-101">Update-AzSignalR</span></span>

## <span data-ttu-id="6f81c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f81c-102">SYNOPSIS</span></span>
<span data-ttu-id="6f81c-103">SignalR 서비스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f81c-103">Update a SignalR service.</span></span>

## <span data-ttu-id="6f81c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6f81c-104">SYNTAX</span></span>

### <span data-ttu-id="6f81c-105">ResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="6f81c-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f81c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f81c-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalR -ResourceId <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f81c-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f81c-107">InputObjectParameterSet</span></span>
```
Update-AzSignalR -InputObject <PSSignalRResource> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6f81c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6f81c-108">DESCRIPTION</span></span>
<span data-ttu-id="6f81c-109">SignalR 서비스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f81c-109">Update a SignalR service.</span></span>
<span data-ttu-id="6f81c-110">지정 하지 않은 경우 다음 값이 매개 변수에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f81c-110">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="6f81c-111">`ResourceGroupName`:으로 설정 된 기본 리소스 그룹 `Set-AzDefault -ResourceGroupName` 입니다.</span><span class="sxs-lookup"><span data-stu-id="6f81c-111">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="6f81c-112">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="6f81c-112">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="6f81c-113">예제의</span><span class="sxs-lookup"><span data-stu-id="6f81c-113">EXAMPLES</span></span>

### <span data-ttu-id="6f81c-114">특정 SignalR 서비스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f81c-114">Update a specific SignalR service.</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="6f81c-115">ServiceMode 및 AllowedOrigin 지정</span><span class="sxs-lookup"><span data-stu-id="6f81c-115">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="6f81c-116">변수</span><span class="sxs-lookup"><span data-stu-id="6f81c-116">PARAMETERS</span></span>

### <span data-ttu-id="6f81c-117">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="6f81c-117">-AllowedOrigin</span></span>
<span data-ttu-id="6f81c-118">SignalR 서비스에 대해 허용 된 원본입니다.</span><span class="sxs-lookup"><span data-stu-id="6f81c-118">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="6f81c-119">모두 허용 하려면 "\*"를 사용 하 여 목록에서 다른 모든 원본을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f81c-119">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="6f81c-120">슬래시는 도메인의 일부로 또는 TLD 이후 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6f81c-120">Slashes are not allowed as part of domain or after TLD</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f81c-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f81c-121">-AsJob</span></span>
<span data-ttu-id="6f81c-122">백그라운드 작업에서 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f81c-122">Run the cmdlet in background job.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f81c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f81c-123">-DefaultProfile</span></span>
<span data-ttu-id="6f81c-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6f81c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f81c-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f81c-125">-InputObject</span></span>
<span data-ttu-id="6f81c-126">SignalR resource 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6f81c-126">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f81c-127">-이름</span><span class="sxs-lookup"><span data-stu-id="6f81c-127">-Name</span></span>
<span data-ttu-id="6f81c-128">SignalR 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f81c-128">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f81c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f81c-129">-ResourceGroupName</span></span>
<span data-ttu-id="6f81c-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f81c-130">The resource group name.</span></span>
<span data-ttu-id="6f81c-131">지정 되지 않은 경우 기본 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6f81c-131">The default one will be used if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f81c-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f81c-132">-ResourceId</span></span>
<span data-ttu-id="6f81c-133">SignalR 서비스 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6f81c-133">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f81c-134">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="6f81c-134">-ServiceMode</span></span>
<span data-ttu-id="6f81c-135">SignalR 서비스에 대 한 서비스 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="6f81c-135">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="6f81c-136">-Sku</span><span class="sxs-lookup"><span data-stu-id="6f81c-136">-Sku</span></span>
<span data-ttu-id="6f81c-137">SignalR 서비스 SKU.</span><span class="sxs-lookup"><span data-stu-id="6f81c-137">The SignalR service SKU.</span></span>
<span data-ttu-id="6f81c-138">"Standard_S1"를 기본값으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f81c-138">Default to "Standard_S1".</span></span>

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

### <span data-ttu-id="6f81c-139">태그</span><span class="sxs-lookup"><span data-stu-id="6f81c-139">-Tag</span></span>
<span data-ttu-id="6f81c-140">SignalR 서비스에 대 한 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="6f81c-140">The tags for the SignalR service.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f81c-141">-단위 개수</span><span class="sxs-lookup"><span data-stu-id="6f81c-141">-UnitCount</span></span>
<span data-ttu-id="6f81c-142">SignalR 서비스 단위 개수, {1, 2, 5, 10, 20, 50, 100}의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="6f81c-142">The SignalR service unit count, value only from {1, 2, 5, 10, 20, 50, 100}.</span></span>
<span data-ttu-id="6f81c-143">기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="6f81c-143">Default to 1.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f81c-144">-확인</span><span class="sxs-lookup"><span data-stu-id="6f81c-144">-Confirm</span></span>
<span data-ttu-id="6f81c-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f81c-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f81c-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f81c-146">-WhatIf</span></span>
<span data-ttu-id="6f81c-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6f81c-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f81c-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6f81c-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f81c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f81c-149">CommonParameters</span></span>
<span data-ttu-id="6f81c-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6f81c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f81c-151">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6f81c-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f81c-152">입력</span><span class="sxs-lookup"><span data-stu-id="6f81c-152">INPUTS</span></span>

### <span data-ttu-id="6f81c-153">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6f81c-153">System.String</span></span>

### <span data-ttu-id="6f81c-154">SignalR. PSSignalRResource/.</span><span class="sxs-lookup"><span data-stu-id="6f81c-154">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="6f81c-155">출력</span><span class="sxs-lookup"><span data-stu-id="6f81c-155">OUTPUTS</span></span>

### <span data-ttu-id="6f81c-156">SignalR. PSSignalRResource/.</span><span class="sxs-lookup"><span data-stu-id="6f81c-156">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="6f81c-157">상속자</span><span class="sxs-lookup"><span data-stu-id="6f81c-157">NOTES</span></span>

## <span data-ttu-id="6f81c-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f81c-158">RELATED LINKS</span></span>
