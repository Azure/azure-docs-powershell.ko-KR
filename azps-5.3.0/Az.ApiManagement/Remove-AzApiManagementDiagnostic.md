---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
ms.openlocfilehash: 488f4082007c96a111483d7efac6a8b9a74dba8f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382131"
---
# <span data-ttu-id="3fd99-101">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="3fd99-101">Remove-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="3fd99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fd99-102">SYNOPSIS</span></span>
<span data-ttu-id="3fd99-103">전역 또는 API 수준 범위에서 진단 엔터티를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3fd99-103">Remove the Diagnostic entity from Global or API level scope.</span></span>

## <span data-ttu-id="3fd99-104">구문</span><span class="sxs-lookup"><span data-stu-id="3fd99-104">SYNTAX</span></span>

### <span data-ttu-id="3fd99-105">ByResourceIdParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="3fd99-105">ByResourceIdParameterSet (Default)</span></span>
```
Remove-AzApiManagementDiagnostic -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fd99-106">ExpandParameterSetName</span><span class="sxs-lookup"><span data-stu-id="3fd99-106">ExpandParameterSetName</span></span>
```
Remove-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-ApiId <String>] -DiagnosticId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fd99-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3fd99-107">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fd99-108">설명</span><span class="sxs-lookup"><span data-stu-id="3fd99-108">DESCRIPTION</span></span>
<span data-ttu-id="3fd99-109">**Remove-AzApiManagementDiagnostic** cmdlet은 전역 범위 또는 범위에서 지정된 진단 엔터티를 `DiagnosticId` `ApiId` 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3fd99-109">The cmdlet **Remove-AzApiManagementDiagnostic** removes the diagnostic entity specified by `DiagnosticId` from global scope or an `ApiId` scope</span></span>

## <span data-ttu-id="3fd99-110">예제</span><span class="sxs-lookup"><span data-stu-id="3fd99-110">EXAMPLES</span></span>

### <span data-ttu-id="3fd99-111">예제 1: 진단 엔터티 제거</span><span class="sxs-lookup"><span data-stu-id="3fd99-111">Example 1: Remove the Diagnostic entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementDiagnostic -Context $apimContext -DiagnosticId "applicationinsights"
```

<span data-ttu-id="3fd99-112">이 예제에서는 `applicationinsights` Api Management 서비스에서 진단을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3fd99-112">This example remove the diagnostic `applicationinsights` from the Api Management service.</span></span>

## <span data-ttu-id="3fd99-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3fd99-113">PARAMETERS</span></span>

### <span data-ttu-id="3fd99-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="3fd99-114">-ApiId</span></span>
<span data-ttu-id="3fd99-115">API의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="3fd99-115">Identifier of the API.</span></span>
<span data-ttu-id="3fd99-116">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="3fd99-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fd99-117">-Context</span><span class="sxs-lookup"><span data-stu-id="3fd99-117">-Context</span></span>
<span data-ttu-id="3fd99-118">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="3fd99-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3fd99-119">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="3fd99-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3fd99-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fd99-120">-DefaultProfile</span></span>
<span data-ttu-id="3fd99-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3fd99-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fd99-122">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="3fd99-122">-DiagnosticId</span></span>
<span data-ttu-id="3fd99-123">기존 제품의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="3fd99-123">Identifier of existing product.</span></span>
<span data-ttu-id="3fd99-124">지정된 경우 제품 범위 정책을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3fd99-124">If specified will return product-scope policy.</span></span>
<span data-ttu-id="3fd99-125">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="3fd99-125">This parameters is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fd99-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3fd99-126">-InputObject</span></span>
<span data-ttu-id="3fd99-127">PsApiManagementDiagnostic의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="3fd99-127">Instance of PsApiManagementDiagnostic.</span></span> <span data-ttu-id="3fd99-128">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="3fd99-128">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementDiagnostic
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3fd99-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3fd99-129">-PassThru</span></span>
<span data-ttu-id="3fd99-130">지정된 경우 작업이 성공하는 경우 true를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="3fd99-130">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="3fd99-131">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="3fd99-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="3fd99-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3fd99-132">-ResourceId</span></span>
<span data-ttu-id="3fd99-133">진단의 Arm ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="3fd99-133">Arm ResourceId of Diagnostic.</span></span> <span data-ttu-id="3fd99-134">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="3fd99-134">This parameter is required.</span></span>

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

### <span data-ttu-id="3fd99-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3fd99-135">-Confirm</span></span>
<span data-ttu-id="3fd99-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3fd99-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fd99-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fd99-137">-WhatIf</span></span>
<span data-ttu-id="3fd99-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3fd99-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fd99-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3fd99-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fd99-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fd99-140">CommonParameters</span></span>
<span data-ttu-id="3fd99-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3fd99-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fd99-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3fd99-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fd99-143">입력</span><span class="sxs-lookup"><span data-stu-id="3fd99-143">INPUTS</span></span>

### <span data-ttu-id="3fd99-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3fd99-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3fd99-145">System.String</span><span class="sxs-lookup"><span data-stu-id="3fd99-145">System.String</span></span>

### <span data-ttu-id="3fd99-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3fd99-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3fd99-147">출력</span><span class="sxs-lookup"><span data-stu-id="3fd99-147">OUTPUTS</span></span>

### <span data-ttu-id="3fd99-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3fd99-148">System.Boolean</span></span>

## <span data-ttu-id="3fd99-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3fd99-149">NOTES</span></span>

## <span data-ttu-id="3fd99-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3fd99-150">RELATED LINKS</span></span>

[<span data-ttu-id="3fd99-151">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="3fd99-151">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="3fd99-152">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="3fd99-152">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="3fd99-153">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="3fd99-153">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)