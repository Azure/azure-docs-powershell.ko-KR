---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
ms.openlocfilehash: 9b6eac7a0c0c994797de51c936840da515ef3f4c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382110"
---
# <span data-ttu-id="30a30-101">Remove-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="30a30-101">Remove-AzApiManagementGateway</span></span>

## <span data-ttu-id="30a30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30a30-102">SYNOPSIS</span></span>
<span data-ttu-id="30a30-103">게이트웨이에서 API를 디스어치합니다.</span><span class="sxs-lookup"><span data-stu-id="30a30-103">Detaches an API from a Gateway.</span></span>

## <span data-ttu-id="30a30-104">구문</span><span class="sxs-lookup"><span data-stu-id="30a30-104">SYNTAX</span></span>

### <span data-ttu-id="30a30-105">ContextParameterSetName(기본값)</span><span class="sxs-lookup"><span data-stu-id="30a30-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30a30-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="30a30-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30a30-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="30a30-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGateway -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30a30-108">설명</span><span class="sxs-lookup"><span data-stu-id="30a30-108">DESCRIPTION</span></span>
<span data-ttu-id="30a30-109">**Remove-AzApiManagementGateway** cmdlet은 게이트웨이에서 API를 분리합니다.</span><span class="sxs-lookup"><span data-stu-id="30a30-109">The **Remove-AzApiManagementGateway** cmdlet detaches an API from a Gateway.</span></span>

## <span data-ttu-id="30a30-110">예제</span><span class="sxs-lookup"><span data-stu-id="30a30-110">EXAMPLES</span></span>

### <span data-ttu-id="30a30-111">예제 1: 기존 게이트웨이 제거</span><span class="sxs-lookup"><span data-stu-id="30a30-111">Example 1: Remove an existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGateway -Context $apimContext -GatewayId "g0001" -Force
```

<span data-ttu-id="30a30-112">이 명령은 기존 게이트웨이를 제거하고 사용자에게 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="30a30-112">This command removes an existing gateway and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="30a30-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30a30-113">PARAMETERS</span></span>

### <span data-ttu-id="30a30-114">-Context</span><span class="sxs-lookup"><span data-stu-id="30a30-114">-Context</span></span>
<span data-ttu-id="30a30-115">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="30a30-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="30a30-116">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="30a30-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30a30-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30a30-117">-DefaultProfile</span></span>
<span data-ttu-id="30a30-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="30a30-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30a30-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="30a30-119">-GatewayId</span></span>
<span data-ttu-id="30a30-120">기존 게이트웨이의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="30a30-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="30a30-121">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="30a30-121">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30a30-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30a30-122">-InputObject</span></span>
<span data-ttu-id="30a30-123">PsApiManagementGateway의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="30a30-123">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="30a30-124">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="30a30-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30a30-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30a30-125">-PassThru</span></span>
<span data-ttu-id="30a30-126">지정된 경우 작업이 성공하는 경우 true를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="30a30-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="30a30-127">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="30a30-127">This parameter is optional.</span></span>
<span data-ttu-id="30a30-128">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="30a30-128">Default value is false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30a30-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="30a30-129">-ResourceId</span></span>
<span data-ttu-id="30a30-130">게이트웨이의 Arm ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="30a30-130">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="30a30-131">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="30a30-131">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30a30-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30a30-132">-Confirm</span></span>
<span data-ttu-id="30a30-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="30a30-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30a30-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30a30-134">-WhatIf</span></span>
<span data-ttu-id="30a30-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="30a30-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30a30-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="30a30-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30a30-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30a30-137">CommonParameters</span></span>
<span data-ttu-id="30a30-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="30a30-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30a30-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="30a30-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30a30-140">입력</span><span class="sxs-lookup"><span data-stu-id="30a30-140">INPUTS</span></span>

### <span data-ttu-id="30a30-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="30a30-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="30a30-142">System.String</span><span class="sxs-lookup"><span data-stu-id="30a30-142">System.String</span></span>

### <span data-ttu-id="30a30-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="30a30-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="30a30-144">출력</span><span class="sxs-lookup"><span data-stu-id="30a30-144">OUTPUTS</span></span>

### <span data-ttu-id="30a30-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="30a30-145">System.Boolean</span></span>

## <span data-ttu-id="30a30-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="30a30-146">NOTES</span></span>

## <span data-ttu-id="30a30-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="30a30-147">RELATED LINKS</span></span>
