---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
ms.openlocfilehash: 222a40c101d0491a6d9409a7404e6731d739a2ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189028"
---
# <span data-ttu-id="a8b2f-101">New-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="a8b2f-101">New-AzSignalR</span></span>

## <span data-ttu-id="a8b2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8b2f-102">SYNOPSIS</span></span>
<span data-ttu-id="a8b2f-103">SignalR 서비스를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="a8b2f-103">Create a SignalR service.</span></span>

## <span data-ttu-id="a8b2f-104">구문</span><span class="sxs-lookup"><span data-stu-id="a8b2f-104">SYNTAX</span></span>

```
New-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Location <String>] [-Sku <String>]
 [-UnitCount <Int32>] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-ServiceMode <String>] [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8b2f-105">설명</span><span class="sxs-lookup"><span data-stu-id="a8b2f-105">DESCRIPTION</span></span>
<span data-ttu-id="a8b2f-106">SignalR 서비스를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="a8b2f-106">Create a SignalR service.</span></span>
<span data-ttu-id="a8b2f-107">지정하지 않으면 매개 변수에 다음 값이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8b2f-107">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="a8b2f-108">`ResourceGroupName`: .로 설정된 기본 리소스 `Set-AzDefault -ResourceGroupName` 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="a8b2f-108">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="a8b2f-109">`Location`: 리소스 그룹의 위치</span><span class="sxs-lookup"><span data-stu-id="a8b2f-109">`Location`: the location of the resource group</span></span>
* <span data-ttu-id="a8b2f-110">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="a8b2f-110">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="a8b2f-111">예제</span><span class="sxs-lookup"><span data-stu-id="a8b2f-111">EXAMPLES</span></span>

### <span data-ttu-id="a8b2f-112">SignalR Service 만들기</span><span class="sxs-lookup"><span data-stu-id="a8b2f-112">Create a SignalR service</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr1 -Location eastus -Sku Standard_S1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="a8b2f-113">ServiceMode 및 AllowedOrigin 지정</span><span class="sxs-lookup"><span data-stu-id="a8b2f-113">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -Location eastus -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="a8b2f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8b2f-114">PARAMETERS</span></span>

### <span data-ttu-id="a8b2f-115">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="a8b2f-115">-AllowedOrigin</span></span>
<span data-ttu-id="a8b2f-116">SignalR 서비스에 허용되는 원본입니다.</span><span class="sxs-lookup"><span data-stu-id="a8b2f-116">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="a8b2f-117">모두 허용하려면 "\*"를 사용하여 목록에서 다른 모든 원본을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a8b2f-117">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="a8b2f-118">슬래시가 도메인의 일부로 또는 TLD 이후로 허용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a8b2f-118">Slashes are not allowed as part of domain or after TLD</span></span>

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

### <span data-ttu-id="a8b2f-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8b2f-119">-AsJob</span></span>
<span data-ttu-id="a8b2f-120">백그라운드 작업에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="a8b2f-120">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="a8b2f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8b2f-121">-DefaultProfile</span></span>
<span data-ttu-id="a8b2f-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a8b2f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8b2f-123">-Location</span><span class="sxs-lookup"><span data-stu-id="a8b2f-123">-Location</span></span>
<span data-ttu-id="a8b2f-124">SignalR 서비스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="a8b2f-124">The SignalR service location.</span></span> <span data-ttu-id="a8b2f-125">지정하지 않으면 리소스 그룹 위치가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8b2f-125">The resource group location will be used if not specified.</span></span>

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

### <span data-ttu-id="a8b2f-126">-Name</span><span class="sxs-lookup"><span data-stu-id="a8b2f-126">-Name</span></span>
<span data-ttu-id="a8b2f-127">SignalR 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8b2f-127">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8b2f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8b2f-128">-ResourceGroupName</span></span>
<span data-ttu-id="a8b2f-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8b2f-129">The resource group name.</span></span> <span data-ttu-id="a8b2f-130">지정하지 않으면 기본 기본 설정이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8b2f-130">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="a8b2f-131">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="a8b2f-131">-ServiceMode</span></span>
<span data-ttu-id="a8b2f-132">SignalR 서비스에 대한 서비스 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="a8b2f-132">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="a8b2f-133">-Sku</span><span class="sxs-lookup"><span data-stu-id="a8b2f-133">-Sku</span></span>
<span data-ttu-id="a8b2f-134">SignalR 서비스 SKU입니다.</span><span class="sxs-lookup"><span data-stu-id="a8b2f-134">The SignalR service SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Standard_S1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8b2f-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="a8b2f-135">-Tag</span></span>
<span data-ttu-id="a8b2f-136">SignalR 서비스에 대한 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="a8b2f-136">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="a8b2f-137">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="a8b2f-137">-UnitCount</span></span>
<span data-ttu-id="a8b2f-138">SignalR 서비스 단위 수(1~10).</span><span class="sxs-lookup"><span data-stu-id="a8b2f-138">The SignalR service unit count, from 1 to 10.</span></span> <span data-ttu-id="a8b2f-139">기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="a8b2f-139">Default to 1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8b2f-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8b2f-140">-Confirm</span></span>
<span data-ttu-id="a8b2f-141">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8b2f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8b2f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8b2f-142">-WhatIf</span></span>
<span data-ttu-id="a8b2f-143">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a8b2f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8b2f-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a8b2f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8b2f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8b2f-145">CommonParameters</span></span>
<span data-ttu-id="a8b2f-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a8b2f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8b2f-147">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a8b2f-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8b2f-148">입력</span><span class="sxs-lookup"><span data-stu-id="a8b2f-148">INPUTS</span></span>

### <span data-ttu-id="a8b2f-149">System.String</span><span class="sxs-lookup"><span data-stu-id="a8b2f-149">System.String</span></span>

## <span data-ttu-id="a8b2f-150">출력</span><span class="sxs-lookup"><span data-stu-id="a8b2f-150">OUTPUTS</span></span>

### <span data-ttu-id="a8b2f-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="a8b2f-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="a8b2f-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a8b2f-152">NOTES</span></span>

## <span data-ttu-id="a8b2f-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a8b2f-153">RELATED LINKS</span></span>
