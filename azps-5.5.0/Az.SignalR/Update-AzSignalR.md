---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/update-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
ms.openlocfilehash: 632f271a085df8384a100392e8ed74ad7b5d0762
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189017"
---
# <span data-ttu-id="77723-101">Update-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="77723-101">Update-AzSignalR</span></span>

## <span data-ttu-id="77723-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77723-102">SYNOPSIS</span></span>
<span data-ttu-id="77723-103">SignalR 서비스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="77723-103">Update a SignalR service.</span></span>

## <span data-ttu-id="77723-104">구문</span><span class="sxs-lookup"><span data-stu-id="77723-104">SYNTAX</span></span>

### <span data-ttu-id="77723-105">ResourceGroupParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="77723-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="77723-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="77723-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalR -ResourceId <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="77723-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="77723-107">InputObjectParameterSet</span></span>
```
Update-AzSignalR -InputObject <PSSignalRResource> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="77723-108">설명</span><span class="sxs-lookup"><span data-stu-id="77723-108">DESCRIPTION</span></span>
<span data-ttu-id="77723-109">SignalR 서비스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="77723-109">Update a SignalR service.</span></span>
<span data-ttu-id="77723-110">지정하지 않으면 매개 변수에 다음 값이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="77723-110">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="77723-111">`ResourceGroupName`: .로 설정된 기본 리소스 `Set-AzDefault -ResourceGroupName` 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="77723-111">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="77723-112">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="77723-112">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="77723-113">예제</span><span class="sxs-lookup"><span data-stu-id="77723-113">EXAMPLES</span></span>

### <span data-ttu-id="77723-114">특정 SignalR 서비스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="77723-114">Update a specific SignalR service.</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="77723-115">ServiceMode 및 AllowedOrigin 지정</span><span class="sxs-lookup"><span data-stu-id="77723-115">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="77723-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77723-116">PARAMETERS</span></span>

### <span data-ttu-id="77723-117">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="77723-117">-AllowedOrigin</span></span>
<span data-ttu-id="77723-118">SignalR 서비스에 허용되는 원본입니다.</span><span class="sxs-lookup"><span data-stu-id="77723-118">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="77723-119">모두 허용하려면 "\*"를 사용하여 목록에서 다른 모든 원본을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="77723-119">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="77723-120">슬래시가 도메인의 일부로 또는 TLD 이후로 허용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="77723-120">Slashes are not allowed as part of domain or after TLD</span></span>

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

### <span data-ttu-id="77723-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77723-121">-AsJob</span></span>
<span data-ttu-id="77723-122">백그라운드 작업에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="77723-122">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="77723-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77723-123">-DefaultProfile</span></span>
<span data-ttu-id="77723-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="77723-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77723-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77723-125">-InputObject</span></span>
<span data-ttu-id="77723-126">SignalR 리소스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="77723-126">The SignalR resource object.</span></span>

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

### <span data-ttu-id="77723-127">-Name</span><span class="sxs-lookup"><span data-stu-id="77723-127">-Name</span></span>
<span data-ttu-id="77723-128">SignalR 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="77723-128">The SignalR service name.</span></span>

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

### <span data-ttu-id="77723-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77723-129">-ResourceGroupName</span></span>
<span data-ttu-id="77723-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="77723-130">The resource group name.</span></span>
<span data-ttu-id="77723-131">지정하지 않으면 기본 기본 설정이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="77723-131">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="77723-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77723-132">-ResourceId</span></span>
<span data-ttu-id="77723-133">SignalR Service 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="77723-133">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77723-134">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="77723-134">-ServiceMode</span></span>
<span data-ttu-id="77723-135">SignalR 서비스에 대한 서비스 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="77723-135">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="77723-136">-Sku</span><span class="sxs-lookup"><span data-stu-id="77723-136">-Sku</span></span>
<span data-ttu-id="77723-137">SignalR 서비스 SKU입니다.</span><span class="sxs-lookup"><span data-stu-id="77723-137">The SignalR service SKU.</span></span>
<span data-ttu-id="77723-138">기본값은 "Standard_S1"입니다.</span><span class="sxs-lookup"><span data-stu-id="77723-138">Default to "Standard_S1".</span></span>

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

### <span data-ttu-id="77723-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="77723-139">-Tag</span></span>
<span data-ttu-id="77723-140">SignalR 서비스에 대한 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="77723-140">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="77723-141">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="77723-141">-UnitCount</span></span>
<span data-ttu-id="77723-142">SignalR 서비스 단위 수, {1, 2, 5, 10, 20, 50, 100}의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="77723-142">The SignalR service unit count, value only from {1, 2, 5, 10, 20, 50, 100}.</span></span>
<span data-ttu-id="77723-143">기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="77723-143">Default to 1.</span></span>

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

### <span data-ttu-id="77723-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77723-144">-Confirm</span></span>
<span data-ttu-id="77723-145">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="77723-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77723-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77723-146">-WhatIf</span></span>
<span data-ttu-id="77723-147">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="77723-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77723-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="77723-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77723-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77723-149">CommonParameters</span></span>
<span data-ttu-id="77723-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="77723-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77723-151">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="77723-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77723-152">입력</span><span class="sxs-lookup"><span data-stu-id="77723-152">INPUTS</span></span>

### <span data-ttu-id="77723-153">System.String</span><span class="sxs-lookup"><span data-stu-id="77723-153">System.String</span></span>

### <span data-ttu-id="77723-154">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="77723-154">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="77723-155">출력</span><span class="sxs-lookup"><span data-stu-id="77723-155">OUTPUTS</span></span>

### <span data-ttu-id="77723-156">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="77723-156">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="77723-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="77723-157">NOTES</span></span>

## <span data-ttu-id="77723-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="77723-158">RELATED LINKS</span></span>
