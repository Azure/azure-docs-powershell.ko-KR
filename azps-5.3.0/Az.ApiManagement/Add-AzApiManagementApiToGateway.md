---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementapitogateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
ms.openlocfilehash: 6bb40d46c80e609824b1c56d05091ade5716f7f8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494498"
---
# <span data-ttu-id="23d82-101">Add-AzApiManagementApiToGateway</span><span class="sxs-lookup"><span data-stu-id="23d82-101">Add-AzApiManagementApiToGateway</span></span>

## <span data-ttu-id="23d82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23d82-102">SYNOPSIS</span></span>
<span data-ttu-id="23d82-103">게이트웨이에 API를 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="23d82-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="23d82-104">구문</span><span class="sxs-lookup"><span data-stu-id="23d82-104">SYNTAX</span></span>

```
Add-AzApiManagementApiToGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-ProvisioningState <PsApiManagementGatewayApiProvisioningState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23d82-105">설명</span><span class="sxs-lookup"><span data-stu-id="23d82-105">DESCRIPTION</span></span>
<span data-ttu-id="23d82-106">**Add-AzApiManagementApiToGateway** cmdlet은 Azure API Management API를 게이트웨이에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="23d82-106">The **Add-AzApiManagementApiToGateway** cmdlet adds an Azure API Management API to a Gateway.</span></span>

## <span data-ttu-id="23d82-107">예제</span><span class="sxs-lookup"><span data-stu-id="23d82-107">EXAMPLES</span></span>

### <span data-ttu-id="23d82-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="23d82-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementApiToGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001"
```

<span data-ttu-id="23d82-109">이 명령은 지정된 게이트웨이에 지정된 API를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="23d82-109">This command adds the specified API to the specified Gateway.</span></span>

## <span data-ttu-id="23d82-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23d82-110">PARAMETERS</span></span>

### <span data-ttu-id="23d82-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="23d82-111">-ApiId</span></span>
<span data-ttu-id="23d82-112">기존 API의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="23d82-112">Identifier of existing API.</span></span>
<span data-ttu-id="23d82-113">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="23d82-113">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23d82-114">-Context</span><span class="sxs-lookup"><span data-stu-id="23d82-114">-Context</span></span>
<span data-ttu-id="23d82-115">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="23d82-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="23d82-116">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="23d82-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23d82-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23d82-117">-DefaultProfile</span></span>
<span data-ttu-id="23d82-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="23d82-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23d82-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="23d82-119">-GatewayId</span></span>
<span data-ttu-id="23d82-120">기존 게이트웨이의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="23d82-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="23d82-121">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="23d82-121">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23d82-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23d82-122">-PassThru</span></span>
<span data-ttu-id="23d82-123">지정된 경우 작업이 성공하는 경우 true를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="23d82-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="23d82-124">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="23d82-124">This parameter is optional.</span></span>
<span data-ttu-id="23d82-125">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="23d82-125">Default value is false.</span></span>

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

### <span data-ttu-id="23d82-126">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="23d82-126">-ProvisioningState</span></span>
<span data-ttu-id="23d82-127">프로비전 상태(생성)</span><span class="sxs-lookup"><span data-stu-id="23d82-127">Provisioning State (Created).</span></span>
<span data-ttu-id="23d82-128">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="23d82-128">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState]
Parameter Sets: (All)
Aliases:
Accepted values: Created

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23d82-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23d82-129">-Confirm</span></span>
<span data-ttu-id="23d82-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="23d82-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23d82-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23d82-131">-WhatIf</span></span>
<span data-ttu-id="23d82-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="23d82-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="23d82-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="23d82-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23d82-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23d82-134">CommonParameters</span></span>
<span data-ttu-id="23d82-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="23d82-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23d82-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="23d82-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23d82-137">입력</span><span class="sxs-lookup"><span data-stu-id="23d82-137">INPUTS</span></span>

### <span data-ttu-id="23d82-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="23d82-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="23d82-139">System.String</span><span class="sxs-lookup"><span data-stu-id="23d82-139">System.String</span></span>

### <span data-ttu-id="23d82-140">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="23d82-140">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="23d82-141">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="23d82-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="23d82-142">출력</span><span class="sxs-lookup"><span data-stu-id="23d82-142">OUTPUTS</span></span>

### <span data-ttu-id="23d82-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="23d82-143">System.Boolean</span></span>

## <span data-ttu-id="23d82-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="23d82-144">NOTES</span></span>

## <span data-ttu-id="23d82-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="23d82-145">RELATED LINKS</span></span>

[<span data-ttu-id="23d82-146">Remove-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="23d82-146">Remove-AzApiManagementApiFromGateway</span></span>](./Remove-AzApiManagementApiFromGateway.md)