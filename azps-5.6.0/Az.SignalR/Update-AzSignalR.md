---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/update-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
ms.openlocfilehash: d02db6e59c688a79b0088c3b3b42fde0cbc13bb8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955355"
---
# <span data-ttu-id="5ec6f-101">Update-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="5ec6f-101">Update-AzSignalR</span></span>

## <span data-ttu-id="5ec6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ec6f-102">SYNOPSIS</span></span>
<span data-ttu-id="5ec6f-103">SignalR 서비스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-103">Update a SignalR service.</span></span>

## <span data-ttu-id="5ec6f-104">구문</span><span class="sxs-lookup"><span data-stu-id="5ec6f-104">SYNTAX</span></span>

### <span data-ttu-id="5ec6f-105">ResourceGroupParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="5ec6f-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ec6f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ec6f-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalR -ResourceId <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ec6f-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ec6f-107">InputObjectParameterSet</span></span>
```
Update-AzSignalR -InputObject <PSSignalRResource> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5ec6f-108">설명</span><span class="sxs-lookup"><span data-stu-id="5ec6f-108">DESCRIPTION</span></span>
<span data-ttu-id="5ec6f-109">SignalR 서비스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-109">Update a SignalR service.</span></span>
<span data-ttu-id="5ec6f-110">지정하지 않은 경우 매개 변수에 다음 값이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-110">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="5ec6f-111">`ResourceGroupName`: 로 설정된 기본 리소스 `Set-AzDefault -ResourceGroupName` 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-111">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="5ec6f-112">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="5ec6f-112">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="5ec6f-113">예제</span><span class="sxs-lookup"><span data-stu-id="5ec6f-113">EXAMPLES</span></span>

### <span data-ttu-id="5ec6f-114">특정 SignalR 서비스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-114">Update a specific SignalR service.</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="5ec6f-115">ServiceMode 및 AllowedOrigin 지정</span><span class="sxs-lookup"><span data-stu-id="5ec6f-115">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="5ec6f-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5ec6f-116">PARAMETERS</span></span>

### <span data-ttu-id="5ec6f-117">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="5ec6f-117">-AllowedOrigin</span></span>
<span data-ttu-id="5ec6f-118">SignalR 서비스에 대해 허용되는 원본입니다.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-118">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="5ec6f-119">모두를 허용하려면 "\*"를 사용하여 목록에서 다른 모든 원본을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-119">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="5ec6f-120">슬래시가 도메인의 일부로 또는 TLD 이후로 허용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-120">Slashes are not allowed as part of domain or after TLD</span></span>

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

### <span data-ttu-id="5ec6f-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ec6f-121">-AsJob</span></span>
<span data-ttu-id="5ec6f-122">백그라운드 작업에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-122">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="5ec6f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ec6f-123">-DefaultProfile</span></span>
<span data-ttu-id="5ec6f-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ec6f-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ec6f-125">-InputObject</span></span>
<span data-ttu-id="5ec6f-126">SignalR 리소스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-126">The SignalR resource object.</span></span>

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

### <span data-ttu-id="5ec6f-127">-Name</span><span class="sxs-lookup"><span data-stu-id="5ec6f-127">-Name</span></span>
<span data-ttu-id="5ec6f-128">SignalR 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-128">The SignalR service name.</span></span>

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

### <span data-ttu-id="5ec6f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ec6f-129">-ResourceGroupName</span></span>
<span data-ttu-id="5ec6f-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-130">The resource group name.</span></span>
<span data-ttu-id="5ec6f-131">지정하지 않은 경우 기본 설정이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-131">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="5ec6f-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ec6f-132">-ResourceId</span></span>
<span data-ttu-id="5ec6f-133">SignalR 서비스 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-133">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="5ec6f-134">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="5ec6f-134">-ServiceMode</span></span>
<span data-ttu-id="5ec6f-135">SignalR 서비스에 대한 서비스 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-135">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="5ec6f-136">-Sku</span><span class="sxs-lookup"><span data-stu-id="5ec6f-136">-Sku</span></span>
<span data-ttu-id="5ec6f-137">SignalR 서비스 SKU.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-137">The SignalR service SKU.</span></span>
<span data-ttu-id="5ec6f-138">기본값은 "Standard_S1"입니다.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-138">Default to "Standard_S1".</span></span>

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

### <span data-ttu-id="5ec6f-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="5ec6f-139">-Tag</span></span>
<span data-ttu-id="5ec6f-140">SignalR 서비스에 대한 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-140">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="5ec6f-141">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="5ec6f-141">-UnitCount</span></span>
<span data-ttu-id="5ec6f-142">SignalR 서비스 단위 개수는 {1, 2, 5, 10, 20, 50, 100}의 값입니다.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-142">The SignalR service unit count, value only from {1, 2, 5, 10, 20, 50, 100}.</span></span>
<span data-ttu-id="5ec6f-143">기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-143">Default to 1.</span></span>

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

### <span data-ttu-id="5ec6f-144">-확인</span><span class="sxs-lookup"><span data-stu-id="5ec6f-144">-Confirm</span></span>
<span data-ttu-id="5ec6f-145">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ec6f-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ec6f-146">-WhatIf</span></span>
<span data-ttu-id="5ec6f-147">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ec6f-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ec6f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ec6f-149">CommonParameters</span></span>
<span data-ttu-id="5ec6f-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5ec6f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ec6f-151">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ec6f-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ec6f-152">입력</span><span class="sxs-lookup"><span data-stu-id="5ec6f-152">INPUTS</span></span>

### <span data-ttu-id="5ec6f-153">System.String</span><span class="sxs-lookup"><span data-stu-id="5ec6f-153">System.String</span></span>

### <span data-ttu-id="5ec6f-154">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="5ec6f-154">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="5ec6f-155">출력</span><span class="sxs-lookup"><span data-stu-id="5ec6f-155">OUTPUTS</span></span>

### <span data-ttu-id="5ec6f-156">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="5ec6f-156">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="5ec6f-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5ec6f-157">NOTES</span></span>

## <span data-ttu-id="5ec6f-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5ec6f-158">RELATED LINKS</span></span>
