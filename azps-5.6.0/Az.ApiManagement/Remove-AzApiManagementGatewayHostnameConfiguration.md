---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: ad0c40e649384d4fb2bef9220f6ab8a994dea96c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012843"
---
# <span data-ttu-id="58bd9-101">Remove-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="58bd9-101">Remove-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="58bd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58bd9-102">SYNOPSIS</span></span>
<span data-ttu-id="58bd9-103">기존 게이트웨이에서 호스트 이름 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="58bd9-103">Removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="58bd9-104">구문</span><span class="sxs-lookup"><span data-stu-id="58bd9-104">SYNTAX</span></span>

### <span data-ttu-id="58bd9-105">ContextParameterSetName(기본값)</span><span class="sxs-lookup"><span data-stu-id="58bd9-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58bd9-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58bd9-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -InputObject <PsApiManagementGatewayHostnameConfiguration>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58bd9-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="58bd9-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58bd9-108">설명</span><span class="sxs-lookup"><span data-stu-id="58bd9-108">DESCRIPTION</span></span>
<span data-ttu-id="58bd9-109">**Remove-AzApiManagementGatewayHostnameConfiguration** cmdlet은 기존 게이트웨이에서 호스트 이름 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="58bd9-109">The **Remove-AzApiManagementGatewayHostnameConfiguration** cmdlet removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="58bd9-110">예제</span><span class="sxs-lookup"><span data-stu-id="58bd9-110">EXAMPLES</span></span>

### <span data-ttu-id="58bd9-111">예제 1: 기존 게이트웨이 호스트 이름 구성 제거</span><span class="sxs-lookup"><span data-stu-id="58bd9-111">Example 1: Remove an existing gateway hostname configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g0001" -GatewayHostnameConfigurationId "h0001" -Force
```

<span data-ttu-id="58bd9-112">이 명령은 기존 게이트웨이 호스트 이름 구성을 제거하고 사용자에게 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58bd9-112">This command removes an existing gateway hostname configuration and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="58bd9-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="58bd9-113">PARAMETERS</span></span>

### <span data-ttu-id="58bd9-114">-Context</span><span class="sxs-lookup"><span data-stu-id="58bd9-114">-Context</span></span>
<span data-ttu-id="58bd9-115">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="58bd9-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="58bd9-116">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="58bd9-116">This parameter is required.</span></span>

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

### <span data-ttu-id="58bd9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58bd9-117">-DefaultProfile</span></span>
<span data-ttu-id="58bd9-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="58bd9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58bd9-119">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="58bd9-119">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="58bd9-120">기존 게이트웨이 호스트 이름 구성의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="58bd9-120">Identifier of existing gateway hostname configuration.</span></span>
<span data-ttu-id="58bd9-121">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="58bd9-121">This parameter is required.</span></span>

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

### <span data-ttu-id="58bd9-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="58bd9-122">-GatewayId</span></span>
<span data-ttu-id="58bd9-123">기존 게이트웨이의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="58bd9-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="58bd9-124">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="58bd9-124">This parameter is required.</span></span>

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

### <span data-ttu-id="58bd9-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58bd9-125">-InputObject</span></span>
<span data-ttu-id="58bd9-126">PsApiManagementGatewayHostnameConfiguration의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="58bd9-126">Instance of PsApiManagementGatewayHostnameConfiguration.</span></span> <span data-ttu-id="58bd9-127">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="58bd9-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58bd9-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58bd9-128">-PassThru</span></span>
<span data-ttu-id="58bd9-129">지정한 경우 작업이 성공할 경우 true를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="58bd9-129">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="58bd9-130">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="58bd9-130">This parameter is optional.</span></span>
<span data-ttu-id="58bd9-131">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="58bd9-131">Default value is false.</span></span>

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

### <span data-ttu-id="58bd9-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58bd9-132">-ResourceId</span></span>
<span data-ttu-id="58bd9-133">GatewayHostnameConfiguration의 Arm ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="58bd9-133">Arm ResourceId of the GatewayHostnameConfiguration.</span></span> <span data-ttu-id="58bd9-134">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="58bd9-134">This parameter is required.</span></span>

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

### <span data-ttu-id="58bd9-135">-확인</span><span class="sxs-lookup"><span data-stu-id="58bd9-135">-Confirm</span></span>
<span data-ttu-id="58bd9-136">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="58bd9-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58bd9-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58bd9-137">-WhatIf</span></span>
<span data-ttu-id="58bd9-138">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="58bd9-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58bd9-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58bd9-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58bd9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58bd9-140">CommonParameters</span></span>
<span data-ttu-id="58bd9-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="58bd9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58bd9-142">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58bd9-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58bd9-143">입력</span><span class="sxs-lookup"><span data-stu-id="58bd9-143">INPUTS</span></span>

### <span data-ttu-id="58bd9-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="58bd9-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="58bd9-145">System.String</span><span class="sxs-lookup"><span data-stu-id="58bd9-145">System.String</span></span>

### <span data-ttu-id="58bd9-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="58bd9-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="58bd9-147">출력</span><span class="sxs-lookup"><span data-stu-id="58bd9-147">OUTPUTS</span></span>

### <span data-ttu-id="58bd9-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="58bd9-148">System.Boolean</span></span>

## <span data-ttu-id="58bd9-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="58bd9-149">NOTES</span></span>

## <span data-ttu-id="58bd9-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="58bd9-150">RELATED LINKS</span></span>
