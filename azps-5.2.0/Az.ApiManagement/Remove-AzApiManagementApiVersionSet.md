---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 58a082288a121e5e6b04353bad862edaea4c20fc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342957"
---
# <span data-ttu-id="b3361-101">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b3361-101">Remove-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="b3361-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3361-102">SYNOPSIS</span></span>
<span data-ttu-id="b3361-103">특정 API 버전 집합을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b3361-103">Removes a particular Api Version Set</span></span>

## <span data-ttu-id="b3361-104">구문</span><span class="sxs-lookup"><span data-stu-id="b3361-104">SYNTAX</span></span>

### <span data-ttu-id="b3361-105">ExpandedParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="b3361-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3361-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b3361-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3361-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b3361-107">ByResourceId</span></span>
```
Remove-AzApiManagementApiVersionSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3361-108">설명</span><span class="sxs-lookup"><span data-stu-id="b3361-108">DESCRIPTION</span></span>

<span data-ttu-id="b3361-109">**Remove-AzAzureRmApiManagementApiVersionSet** cmdlet은 기존 API 버전 집합을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b3361-109">The **Remove-AzAzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="b3361-110">예제</span><span class="sxs-lookup"><span data-stu-id="b3361-110">EXAMPLES</span></span>

### <span data-ttu-id="b3361-111">예제 1: API 버전 집합 제거</span><span class="sxs-lookup"><span data-stu-id="b3361-111">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="b3361-112">이 명령은 지정된 ApiVersionSetId를 사용하여 API 버전 집합을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b3361-112">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="b3361-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3361-113">PARAMETERS</span></span>

### <span data-ttu-id="b3361-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="b3361-114">-ApiVersionSetId</span></span>
<span data-ttu-id="b3361-115">API 버전 집합의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="b3361-115">Identifier of the API Version Set.</span></span>
<span data-ttu-id="b3361-116">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="b3361-116">This parameter is required.</span></span>

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

### <span data-ttu-id="b3361-117">-Context</span><span class="sxs-lookup"><span data-stu-id="b3361-117">-Context</span></span>
<span data-ttu-id="b3361-118">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="b3361-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b3361-119">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="b3361-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3361-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3361-120">-DefaultProfile</span></span>
<span data-ttu-id="b3361-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b3361-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3361-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3361-122">-InputObject</span></span>
<span data-ttu-id="b3361-123">PsApiManagementApiVersionSet의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="b3361-123">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="b3361-124">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="b3361-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3361-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3361-125">-PassThru</span></span>
<span data-ttu-id="b3361-126">지정된 경우 작업이 성공하는 경우 true를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="b3361-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="b3361-127">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="b3361-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="b3361-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3361-128">-ResourceId</span></span>
<span data-ttu-id="b3361-129">ApiVersionSet의 Arm ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="b3361-129">Arm ResourceId of ApiVersionSet.</span></span> <span data-ttu-id="b3361-130">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="b3361-130">This parameter is required.</span></span>

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

### <span data-ttu-id="b3361-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3361-131">-Confirm</span></span>
<span data-ttu-id="b3361-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b3361-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3361-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3361-133">-WhatIf</span></span>
<span data-ttu-id="b3361-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b3361-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3361-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b3361-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3361-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3361-136">CommonParameters</span></span>
<span data-ttu-id="b3361-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b3361-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3361-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b3361-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3361-139">입력</span><span class="sxs-lookup"><span data-stu-id="b3361-139">INPUTS</span></span>

### <span data-ttu-id="b3361-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b3361-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b3361-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b3361-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="b3361-142">System.String</span><span class="sxs-lookup"><span data-stu-id="b3361-142">System.String</span></span>

## <span data-ttu-id="b3361-143">출력</span><span class="sxs-lookup"><span data-stu-id="b3361-143">OUTPUTS</span></span>

### <span data-ttu-id="b3361-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b3361-144">System.Boolean</span></span>

## <span data-ttu-id="b3361-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b3361-145">NOTES</span></span>

## <span data-ttu-id="b3361-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b3361-146">RELATED LINKS</span></span>

[<span data-ttu-id="b3361-147">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b3361-147">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="b3361-148">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b3361-148">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="b3361-149">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b3361-149">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)