---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
ms.openlocfilehash: 222a40c101d0491a6d9409a7404e6731d739a2ba
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034750"
---
# <span data-ttu-id="9990a-101">New-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="9990a-101">New-AzSignalR</span></span>

## <span data-ttu-id="9990a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9990a-102">SYNOPSIS</span></span>
<span data-ttu-id="9990a-103">SignalR 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9990a-103">Create a SignalR service.</span></span>

## <span data-ttu-id="9990a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9990a-104">SYNTAX</span></span>

```
New-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Location <String>] [-Sku <String>]
 [-UnitCount <Int32>] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-ServiceMode <String>] [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9990a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9990a-105">DESCRIPTION</span></span>
<span data-ttu-id="9990a-106">SignalR 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9990a-106">Create a SignalR service.</span></span>
<span data-ttu-id="9990a-107">지정 하지 않은 경우 다음 값이 매개 변수에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9990a-107">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="9990a-108">`ResourceGroupName`:으로 설정 된 기본 리소스 그룹 `Set-AzDefault -ResourceGroupName` 입니다.</span><span class="sxs-lookup"><span data-stu-id="9990a-108">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="9990a-109">`Location`: 리소스 그룹의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="9990a-109">`Location`: the location of the resource group</span></span>
* <span data-ttu-id="9990a-110">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="9990a-110">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="9990a-111">예제의</span><span class="sxs-lookup"><span data-stu-id="9990a-111">EXAMPLES</span></span>

### <span data-ttu-id="9990a-112">SignalR 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="9990a-112">Create a SignalR service</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr1 -Location eastus -Sku Standard_S1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="9990a-113">ServiceMode 및 AllowedOrigin 지정</span><span class="sxs-lookup"><span data-stu-id="9990a-113">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -Location eastus -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="9990a-114">변수</span><span class="sxs-lookup"><span data-stu-id="9990a-114">PARAMETERS</span></span>

### <span data-ttu-id="9990a-115">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="9990a-115">-AllowedOrigin</span></span>
<span data-ttu-id="9990a-116">SignalR 서비스에 대해 허용 된 원본입니다.</span><span class="sxs-lookup"><span data-stu-id="9990a-116">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="9990a-117">모두 허용 하려면 "\*"를 사용 하 여 목록에서 다른 모든 원본을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9990a-117">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="9990a-118">슬래시는 도메인의 일부로 또는 TLD 이후 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9990a-118">Slashes are not allowed as part of domain or after TLD</span></span>

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

### <span data-ttu-id="9990a-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9990a-119">-AsJob</span></span>
<span data-ttu-id="9990a-120">백그라운드 작업에서 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9990a-120">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="9990a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9990a-121">-DefaultProfile</span></span>
<span data-ttu-id="9990a-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9990a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9990a-123">-위치</span><span class="sxs-lookup"><span data-stu-id="9990a-123">-Location</span></span>
<span data-ttu-id="9990a-124">SignalR 서비스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="9990a-124">The SignalR service location.</span></span> <span data-ttu-id="9990a-125">리소스 그룹 위치가 지정 되지 않은 경우 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9990a-125">The resource group location will be used if not specified.</span></span>

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

### <span data-ttu-id="9990a-126">-이름</span><span class="sxs-lookup"><span data-stu-id="9990a-126">-Name</span></span>
<span data-ttu-id="9990a-127">SignalR 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9990a-127">The SignalR service name.</span></span>

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

### <span data-ttu-id="9990a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9990a-128">-ResourceGroupName</span></span>
<span data-ttu-id="9990a-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9990a-129">The resource group name.</span></span> <span data-ttu-id="9990a-130">지정 되지 않은 경우 기본 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9990a-130">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="9990a-131">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="9990a-131">-ServiceMode</span></span>
<span data-ttu-id="9990a-132">SignalR 서비스에 대 한 서비스 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="9990a-132">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="9990a-133">-Sku</span><span class="sxs-lookup"><span data-stu-id="9990a-133">-Sku</span></span>
<span data-ttu-id="9990a-134">SignalR 서비스 SKU.</span><span class="sxs-lookup"><span data-stu-id="9990a-134">The SignalR service SKU.</span></span>

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

### <span data-ttu-id="9990a-135">태그</span><span class="sxs-lookup"><span data-stu-id="9990a-135">-Tag</span></span>
<span data-ttu-id="9990a-136">SignalR 서비스에 대 한 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="9990a-136">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="9990a-137">-단위 개수</span><span class="sxs-lookup"><span data-stu-id="9990a-137">-UnitCount</span></span>
<span data-ttu-id="9990a-138">SignalR 서비스 단위 수 (1 ~ 10)입니다.</span><span class="sxs-lookup"><span data-stu-id="9990a-138">The SignalR service unit count, from 1 to 10.</span></span> <span data-ttu-id="9990a-139">기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="9990a-139">Default to 1.</span></span>

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

### <span data-ttu-id="9990a-140">-확인</span><span class="sxs-lookup"><span data-stu-id="9990a-140">-Confirm</span></span>
<span data-ttu-id="9990a-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9990a-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9990a-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9990a-142">-WhatIf</span></span>
<span data-ttu-id="9990a-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9990a-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9990a-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9990a-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9990a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9990a-145">CommonParameters</span></span>
<span data-ttu-id="9990a-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9990a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9990a-147">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9990a-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9990a-148">입력</span><span class="sxs-lookup"><span data-stu-id="9990a-148">INPUTS</span></span>

### <span data-ttu-id="9990a-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9990a-149">System.String</span></span>

## <span data-ttu-id="9990a-150">출력</span><span class="sxs-lookup"><span data-stu-id="9990a-150">OUTPUTS</span></span>

### <span data-ttu-id="9990a-151">SignalR. PSSignalRResource/.</span><span class="sxs-lookup"><span data-stu-id="9990a-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="9990a-152">상속자</span><span class="sxs-lookup"><span data-stu-id="9990a-152">NOTES</span></span>

## <span data-ttu-id="9990a-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9990a-153">RELATED LINKS</span></span>
