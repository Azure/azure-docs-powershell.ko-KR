---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/Update-AzApiManagementGateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
ms.openlocfilehash: 62131f634d049afe137b635d6a970d37e2173b8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001931"
---
# <span data-ttu-id="31bc9-101">Update-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="31bc9-101">Update-AzApiManagementGateway</span></span>

## <span data-ttu-id="31bc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31bc9-102">SYNOPSIS</span></span>
<span data-ttu-id="31bc9-103">API 관리 게이트웨이를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="31bc9-103">Configures an API management Gateway.</span></span>

## <span data-ttu-id="31bc9-104">구문</span><span class="sxs-lookup"><span data-stu-id="31bc9-104">SYNTAX</span></span>

### <span data-ttu-id="31bc9-105">ExpandedParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="31bc9-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31bc9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="31bc9-106">ByInputObject</span></span>
```
Update-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31bc9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="31bc9-107">ByResourceId</span></span>
```
Update-AzApiManagementGateway -ResourceId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31bc9-108">설명</span><span class="sxs-lookup"><span data-stu-id="31bc9-108">DESCRIPTION</span></span>
<span data-ttu-id="31bc9-109">**Update-AzApiManagementGateway** cmdlet은 API 관리 게이트웨이를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="31bc9-109">The **Update-AzApiManagementGateway** cmdlet configures an API management Gateway.</span></span>

## <span data-ttu-id="31bc9-110">예제</span><span class="sxs-lookup"><span data-stu-id="31bc9-110">EXAMPLES</span></span>

### <span data-ttu-id="31bc9-111">예제 1: 관리 그룹 구성</span><span class="sxs-lookup"><span data-stu-id="31bc9-111">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementGateway -Context $apimContext -GatewayId "0001" -Description "Updated Gateway"
```

<span data-ttu-id="31bc9-112">이 명령은 게이트웨이를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="31bc9-112">This command configures a gateway.</span></span>

## <span data-ttu-id="31bc9-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="31bc9-113">PARAMETERS</span></span>

### <span data-ttu-id="31bc9-114">-Context</span><span class="sxs-lookup"><span data-stu-id="31bc9-114">-Context</span></span>
<span data-ttu-id="31bc9-115">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="31bc9-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="31bc9-116">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="31bc9-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31bc9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31bc9-117">-DefaultProfile</span></span>
<span data-ttu-id="31bc9-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="31bc9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31bc9-119">-Description</span><span class="sxs-lookup"><span data-stu-id="31bc9-119">-Description</span></span>
<span data-ttu-id="31bc9-120">게이트웨이 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="31bc9-120">Gateway description.</span></span>
<span data-ttu-id="31bc9-121">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="31bc9-121">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31bc9-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="31bc9-122">-GatewayId</span></span>
<span data-ttu-id="31bc9-123">기존 게이트웨이의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="31bc9-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="31bc9-124">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="31bc9-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31bc9-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31bc9-125">-InputObject</span></span>
<span data-ttu-id="31bc9-126">PsApiManagementGateway의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="31bc9-126">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="31bc9-127">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="31bc9-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31bc9-128">-LocationData</span><span class="sxs-lookup"><span data-stu-id="31bc9-128">-LocationData</span></span>
<span data-ttu-id="31bc9-129">게이트웨이 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="31bc9-129">Gateway location.</span></span>
<span data-ttu-id="31bc9-130">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="31bc9-130">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31bc9-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31bc9-131">-PassThru</span></span>
<span data-ttu-id="31bc9-132">지정된 경우 Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway 형식의 인스턴스가 수정된 게이트웨이를 나타내는 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="31bc9-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway type representing the modified gateway.</span></span>

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

### <span data-ttu-id="31bc9-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31bc9-133">-ResourceId</span></span>
<span data-ttu-id="31bc9-134">게이트웨이의 Arm ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="31bc9-134">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="31bc9-135">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="31bc9-135">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31bc9-136">-확인</span><span class="sxs-lookup"><span data-stu-id="31bc9-136">-Confirm</span></span>
<span data-ttu-id="31bc9-137">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="31bc9-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31bc9-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31bc9-138">-WhatIf</span></span>
<span data-ttu-id="31bc9-139">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="31bc9-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31bc9-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31bc9-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31bc9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31bc9-141">CommonParameters</span></span>
<span data-ttu-id="31bc9-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="31bc9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31bc9-143">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="31bc9-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31bc9-144">입력</span><span class="sxs-lookup"><span data-stu-id="31bc9-144">INPUTS</span></span>

### <span data-ttu-id="31bc9-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="31bc9-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="31bc9-146">System.String</span><span class="sxs-lookup"><span data-stu-id="31bc9-146">System.String</span></span>

### <span data-ttu-id="31bc9-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="31bc9-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

### <span data-ttu-id="31bc9-148">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="31bc9-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="31bc9-149">출력</span><span class="sxs-lookup"><span data-stu-id="31bc9-149">OUTPUTS</span></span>

### <span data-ttu-id="31bc9-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="31bc9-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="31bc9-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="31bc9-151">NOTES</span></span>

## <span data-ttu-id="31bc9-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31bc9-152">RELATED LINKS</span></span>
