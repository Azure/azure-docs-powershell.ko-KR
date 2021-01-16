---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/Update-AzApiManagementGateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
ms.openlocfilehash: d053bc60390c43c3409bb7adfad5a3ff3720f5b7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381550"
---
# <span data-ttu-id="04920-101">Update-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="04920-101">Update-AzApiManagementGateway</span></span>

## <span data-ttu-id="04920-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04920-102">SYNOPSIS</span></span>
<span data-ttu-id="04920-103">API 관리 게이트웨이를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="04920-103">Configures an API management Gateway.</span></span>

## <span data-ttu-id="04920-104">구문</span><span class="sxs-lookup"><span data-stu-id="04920-104">SYNTAX</span></span>

### <span data-ttu-id="04920-105">ExpandedParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="04920-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04920-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="04920-106">ByInputObject</span></span>
```
Update-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04920-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="04920-107">ByResourceId</span></span>
```
Update-AzApiManagementGateway -ResourceId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04920-108">설명</span><span class="sxs-lookup"><span data-stu-id="04920-108">DESCRIPTION</span></span>
<span data-ttu-id="04920-109">**Update-AzApiManagementGateway** cmdlet은 API Management Gateway를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="04920-109">The **Update-AzApiManagementGateway** cmdlet configures an API management Gateway.</span></span>

## <span data-ttu-id="04920-110">예제</span><span class="sxs-lookup"><span data-stu-id="04920-110">EXAMPLES</span></span>

### <span data-ttu-id="04920-111">예제 1: 관리 그룹 구성</span><span class="sxs-lookup"><span data-stu-id="04920-111">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementGateway -Context $apimContext -GatewayId "0001" -Description "Updated Gateway"
```

<span data-ttu-id="04920-112">이 명령은 게이트웨이를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="04920-112">This command configures a gateway.</span></span>

## <span data-ttu-id="04920-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04920-113">PARAMETERS</span></span>

### <span data-ttu-id="04920-114">-Context</span><span class="sxs-lookup"><span data-stu-id="04920-114">-Context</span></span>
<span data-ttu-id="04920-115">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="04920-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="04920-116">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="04920-116">This parameter is required.</span></span>

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

### <span data-ttu-id="04920-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04920-117">-DefaultProfile</span></span>
<span data-ttu-id="04920-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="04920-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04920-119">-Description</span><span class="sxs-lookup"><span data-stu-id="04920-119">-Description</span></span>
<span data-ttu-id="04920-120">게이트웨이 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="04920-120">Gateway description.</span></span>
<span data-ttu-id="04920-121">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="04920-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="04920-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="04920-122">-GatewayId</span></span>
<span data-ttu-id="04920-123">기존 게이트웨이의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="04920-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="04920-124">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="04920-124">This parameter is required.</span></span>

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

### <span data-ttu-id="04920-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04920-125">-InputObject</span></span>
<span data-ttu-id="04920-126">PsApiManagementGateway의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="04920-126">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="04920-127">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="04920-127">This parameter is required.</span></span>

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

### <span data-ttu-id="04920-128">-LocationData</span><span class="sxs-lookup"><span data-stu-id="04920-128">-LocationData</span></span>
<span data-ttu-id="04920-129">게이트웨이 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="04920-129">Gateway location.</span></span>
<span data-ttu-id="04920-130">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="04920-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="04920-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04920-131">-PassThru</span></span>
<span data-ttu-id="04920-132">지정된 경우 수정된 게이트웨이를 나타내는 Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway 형식의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="04920-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway type representing the modified gateway.</span></span>

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

### <span data-ttu-id="04920-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04920-133">-ResourceId</span></span>
<span data-ttu-id="04920-134">게이트웨이의 Arm ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="04920-134">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="04920-135">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="04920-135">This parameter is required.</span></span>

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

### <span data-ttu-id="04920-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04920-136">-Confirm</span></span>
<span data-ttu-id="04920-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="04920-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04920-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04920-138">-WhatIf</span></span>
<span data-ttu-id="04920-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="04920-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04920-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04920-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04920-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04920-141">CommonParameters</span></span>
<span data-ttu-id="04920-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="04920-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04920-143">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="04920-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04920-144">입력</span><span class="sxs-lookup"><span data-stu-id="04920-144">INPUTS</span></span>

### <span data-ttu-id="04920-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="04920-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="04920-146">System.String</span><span class="sxs-lookup"><span data-stu-id="04920-146">System.String</span></span>

### <span data-ttu-id="04920-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="04920-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

### <span data-ttu-id="04920-148">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="04920-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="04920-149">출력</span><span class="sxs-lookup"><span data-stu-id="04920-149">OUTPUTS</span></span>

### <span data-ttu-id="04920-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="04920-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="04920-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="04920-151">NOTES</span></span>

## <span data-ttu-id="04920-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="04920-152">RELATED LINKS</span></span>
