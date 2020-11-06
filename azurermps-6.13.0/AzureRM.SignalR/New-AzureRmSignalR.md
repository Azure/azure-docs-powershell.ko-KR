---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/new-azurermsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/New-AzureRmSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/New-AzureRmSignalR.md
ms.openlocfilehash: d5b7e5480ea3078dadf5280b4f683280dcd00ea4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530882"
---
# <span data-ttu-id="879a1-101">New-AzureRmSignalR</span><span class="sxs-lookup"><span data-stu-id="879a1-101">New-AzureRmSignalR</span></span>

## <span data-ttu-id="879a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="879a1-102">SYNOPSIS</span></span>
<span data-ttu-id="879a1-103">SignalR 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="879a1-103">Create a SignalR service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="879a1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="879a1-104">SYNTAX</span></span>

```
New-AzureRmSignalR [-ResourceGroupName <String>] [-Name] <String> [-Location <String>] [-Sku <String>]
 [-UnitCount <Int32>] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="879a1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="879a1-105">DESCRIPTION</span></span>
<span data-ttu-id="879a1-106">SignalR 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="879a1-106">Create a SignalR service.</span></span>
<span data-ttu-id="879a1-107">지정 하지 않은 경우 다음 값이 매개 변수에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="879a1-107">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="879a1-108">`ResourceGroupName`:으로 설정 된 기본 리소스 그룹 `Set-AzureRmDefault -ResourceGroupName` 입니다.</span><span class="sxs-lookup"><span data-stu-id="879a1-108">`ResourceGroupName`: the default resource group set by `Set-AzureRmDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="879a1-109">`Location`: 리소스 그룹의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="879a1-109">`Location`: the location of the resource group</span></span>
* <span data-ttu-id="879a1-110">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="879a1-110">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="879a1-111">예제의</span><span class="sxs-lookup"><span data-stu-id="879a1-111">EXAMPLES</span></span>

### <span data-ttu-id="879a1-112">SignalR를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="879a1-112">Create a SignalR serivce</span></span>
```powershell
PS C:\> New-AzureRmSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr1 -Location eastus -Sku Standard_S1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0-preview
```

## <span data-ttu-id="879a1-113">변수</span><span class="sxs-lookup"><span data-stu-id="879a1-113">PARAMETERS</span></span>

### <span data-ttu-id="879a1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="879a1-114">-AsJob</span></span>
<span data-ttu-id="879a1-115">백그라운드 작업에서 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="879a1-115">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="879a1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="879a1-116">-DefaultProfile</span></span>
<span data-ttu-id="879a1-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="879a1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="879a1-118">-위치</span><span class="sxs-lookup"><span data-stu-id="879a1-118">-Location</span></span>
<span data-ttu-id="879a1-119">SignalR 서비스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="879a1-119">The SignalR service location.</span></span> <span data-ttu-id="879a1-120">리소스 그룹 위치가 지정 되지 않은 경우 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="879a1-120">The resource group location will be used if not specified.</span></span>

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

### <span data-ttu-id="879a1-121">-이름</span><span class="sxs-lookup"><span data-stu-id="879a1-121">-Name</span></span>
<span data-ttu-id="879a1-122">SignalR 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="879a1-122">The SignalR service name.</span></span>

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

### <span data-ttu-id="879a1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="879a1-123">-ResourceGroupName</span></span>
<span data-ttu-id="879a1-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="879a1-124">The resource group name.</span></span> <span data-ttu-id="879a1-125">지정 되지 않은 경우 기본 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="879a1-125">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="879a1-126">-Sku</span><span class="sxs-lookup"><span data-stu-id="879a1-126">-Sku</span></span>
<span data-ttu-id="879a1-127">SignalR 서비스 SKU.</span><span class="sxs-lookup"><span data-stu-id="879a1-127">The SignalR service SKU.</span></span>

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

### <span data-ttu-id="879a1-128">태그</span><span class="sxs-lookup"><span data-stu-id="879a1-128">-Tag</span></span>
<span data-ttu-id="879a1-129">SignalR 서비스에 대 한 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="879a1-129">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="879a1-130">-단위 개수</span><span class="sxs-lookup"><span data-stu-id="879a1-130">-UnitCount</span></span>
<span data-ttu-id="879a1-131">SignalR 서비스 단위 수 (1 ~ 10)입니다.</span><span class="sxs-lookup"><span data-stu-id="879a1-131">The SignalR service unit count, from 1 to 10.</span></span> <span data-ttu-id="879a1-132">기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="879a1-132">Default to 1.</span></span>

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

### <span data-ttu-id="879a1-133">-확인</span><span class="sxs-lookup"><span data-stu-id="879a1-133">-Confirm</span></span>
<span data-ttu-id="879a1-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="879a1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="879a1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="879a1-135">-WhatIf</span></span>
<span data-ttu-id="879a1-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="879a1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="879a1-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="879a1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="879a1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="879a1-138">CommonParameters</span></span>
<span data-ttu-id="879a1-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="879a1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="879a1-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="879a1-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="879a1-141">입력</span><span class="sxs-lookup"><span data-stu-id="879a1-141">INPUTS</span></span>

### <span data-ttu-id="879a1-142">않아야</span><span class="sxs-lookup"><span data-stu-id="879a1-142">None</span></span>

## <span data-ttu-id="879a1-143">출력</span><span class="sxs-lookup"><span data-stu-id="879a1-143">OUTPUTS</span></span>

### <span data-ttu-id="879a1-144">SignalR. PSSignalRResource/.</span><span class="sxs-lookup"><span data-stu-id="879a1-144">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="879a1-145">상속자</span><span class="sxs-lookup"><span data-stu-id="879a1-145">NOTES</span></span>

## <span data-ttu-id="879a1-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="879a1-146">RELATED LINKS</span></span>
