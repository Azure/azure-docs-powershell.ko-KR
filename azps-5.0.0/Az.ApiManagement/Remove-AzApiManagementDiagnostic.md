---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementDiagnostic.md
ms.openlocfilehash: 488f4082007c96a111483d7efac6a8b9a74dba8f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218156"
---
# <span data-ttu-id="711ec-101">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="711ec-101">Remove-AzApiManagementDiagnostic</span></span>

## <span data-ttu-id="711ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="711ec-102">SYNOPSIS</span></span>
<span data-ttu-id="711ec-103">전역 또는 API 수준 범위에서 진단 엔터티를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="711ec-103">Remove the Diagnostic entity from Global or API level scope.</span></span>

## <span data-ttu-id="711ec-104">구문과</span><span class="sxs-lookup"><span data-stu-id="711ec-104">SYNTAX</span></span>

### <span data-ttu-id="711ec-105">ByResourceIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="711ec-105">ByResourceIdParameterSet (Default)</span></span>
```
Remove-AzApiManagementDiagnostic -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="711ec-106">ExpandParameterSetName</span><span class="sxs-lookup"><span data-stu-id="711ec-106">ExpandParameterSetName</span></span>
```
Remove-AzApiManagementDiagnostic -Context <PsApiManagementContext> [-ApiId <String>] -DiagnosticId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="711ec-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="711ec-107">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementDiagnostic -InputObject <PsApiManagementDiagnostic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="711ec-108">설명은</span><span class="sxs-lookup"><span data-stu-id="711ec-108">DESCRIPTION</span></span>
<span data-ttu-id="711ec-109">Cmdlet **AzApiManagementDiagnostic** 는 `DiagnosticId` 전역 범위 또는 범위에서 지정 된 진단 엔터티를 제거 합니다. `ApiId`</span><span class="sxs-lookup"><span data-stu-id="711ec-109">The cmdlet **Remove-AzApiManagementDiagnostic** removes the diagnostic entity specified by `DiagnosticId` from global scope or an `ApiId` scope</span></span>

## <span data-ttu-id="711ec-110">예제의</span><span class="sxs-lookup"><span data-stu-id="711ec-110">EXAMPLES</span></span>

### <span data-ttu-id="711ec-111">예제 1: 진단 엔터티 제거</span><span class="sxs-lookup"><span data-stu-id="711ec-111">Example 1: Remove the Diagnostic entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementDiagnostic -Context $apimContext -DiagnosticId "applicationinsights"
```

<span data-ttu-id="711ec-112">이 예제에서는 `applicationinsights` Api Management 서비스에서 진단을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="711ec-112">This example remove the diagnostic `applicationinsights` from the Api Management service.</span></span>

## <span data-ttu-id="711ec-113">변수</span><span class="sxs-lookup"><span data-stu-id="711ec-113">PARAMETERS</span></span>

### <span data-ttu-id="711ec-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="711ec-114">-ApiId</span></span>
<span data-ttu-id="711ec-115">API의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="711ec-115">Identifier of the API.</span></span>
<span data-ttu-id="711ec-116">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="711ec-116">This parameter is required.</span></span>

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

### <span data-ttu-id="711ec-117">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="711ec-117">-Context</span></span>
<span data-ttu-id="711ec-118">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="711ec-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="711ec-119">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="711ec-119">This parameter is required.</span></span>

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

### <span data-ttu-id="711ec-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="711ec-120">-DefaultProfile</span></span>
<span data-ttu-id="711ec-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="711ec-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="711ec-122">-DiagnosticId</span><span class="sxs-lookup"><span data-stu-id="711ec-122">-DiagnosticId</span></span>
<span data-ttu-id="711ec-123">기존 제품의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="711ec-123">Identifier of existing product.</span></span>
<span data-ttu-id="711ec-124">지정 된 경우 제품 범위 정책이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="711ec-124">If specified will return product-scope policy.</span></span>
<span data-ttu-id="711ec-125">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="711ec-125">This parameters is optional.</span></span>

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

### <span data-ttu-id="711ec-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="711ec-126">-InputObject</span></span>
<span data-ttu-id="711ec-127">PsApiManagementDiagnostic의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="711ec-127">Instance of PsApiManagementDiagnostic.</span></span> <span data-ttu-id="711ec-128">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="711ec-128">This parameter is required.</span></span>

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

### <span data-ttu-id="711ec-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="711ec-129">-PassThru</span></span>
<span data-ttu-id="711ec-130">지정 된 경우 대/소문자 구분 작업이 성공한 경우 true를 씁니다.</span><span class="sxs-lookup"><span data-stu-id="711ec-130">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="711ec-131">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="711ec-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="711ec-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="711ec-132">-ResourceId</span></span>
<span data-ttu-id="711ec-133">진단의 팔 ResourceId 개수입니다.</span><span class="sxs-lookup"><span data-stu-id="711ec-133">Arm ResourceId of Diagnostic.</span></span> <span data-ttu-id="711ec-134">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="711ec-134">This parameter is required.</span></span>

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

### <span data-ttu-id="711ec-135">-확인</span><span class="sxs-lookup"><span data-stu-id="711ec-135">-Confirm</span></span>
<span data-ttu-id="711ec-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="711ec-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="711ec-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="711ec-137">-WhatIf</span></span>
<span data-ttu-id="711ec-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="711ec-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="711ec-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="711ec-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="711ec-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="711ec-140">CommonParameters</span></span>
<span data-ttu-id="711ec-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="711ec-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="711ec-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="711ec-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="711ec-143">입력</span><span class="sxs-lookup"><span data-stu-id="711ec-143">INPUTS</span></span>

### <span data-ttu-id="711ec-144">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="711ec-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="711ec-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="711ec-145">System.String</span></span>

### <span data-ttu-id="711ec-146">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="711ec-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="711ec-147">출력</span><span class="sxs-lookup"><span data-stu-id="711ec-147">OUTPUTS</span></span>

### <span data-ttu-id="711ec-148">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="711ec-148">System.Boolean</span></span>

## <span data-ttu-id="711ec-149">상속자</span><span class="sxs-lookup"><span data-stu-id="711ec-149">NOTES</span></span>

## <span data-ttu-id="711ec-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="711ec-150">RELATED LINKS</span></span>

[<span data-ttu-id="711ec-151">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="711ec-151">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="711ec-152">새로운 AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="711ec-152">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="711ec-153">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="711ec-153">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)