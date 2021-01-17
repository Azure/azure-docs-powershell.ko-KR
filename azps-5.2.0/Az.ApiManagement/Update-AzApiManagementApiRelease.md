---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
ms.openlocfilehash: 99ec1234eea582fb91f2722032cb23c27e86b878
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347738"
---
# <span data-ttu-id="00454-101">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="00454-101">Update-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="00454-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00454-102">SYNOPSIS</span></span>
<span data-ttu-id="00454-103">특정 API 릴리스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="00454-103">Updates a particular Api Release.</span></span>

## <span data-ttu-id="00454-104">구문</span><span class="sxs-lookup"><span data-stu-id="00454-104">SYNTAX</span></span>

### <span data-ttu-id="00454-105">ExpandedParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="00454-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementApiRelease -Context <PsApiManagementContext> -ReleaseId <String> -ApiId <String>
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="00454-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="00454-106">ByInputObject</span></span>
```
Update-AzApiManagementApiRelease [-Note <String>] -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00454-107">설명</span><span class="sxs-lookup"><span data-stu-id="00454-107">DESCRIPTION</span></span>
<span data-ttu-id="00454-108">**Update-AzApiManagementApiRelease** cmdlet은 Azure API Management API 릴리스를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="00454-108">The **Update-AzApiManagementApiRelease** cmdlet modifies an Azure API Management API Release.</span></span>

## <span data-ttu-id="00454-109">예제</span><span class="sxs-lookup"><span data-stu-id="00454-109">EXAMPLES</span></span>

### <span data-ttu-id="00454-110">예제 1: API 개정에 대한 API 릴리스 업데이트</span><span class="sxs-lookup"><span data-stu-id="00454-110">Example 1: Updates an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId "echo-api" -ReleaseId "echo-api-release" -Note "Releasing version 2 of the echo-api to public"
```

<span data-ttu-id="00454-111">이 명령은 API의 API 릴리스를 새 참고 `echo-api-release` `echo-api` 사항으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="00454-111">This command updates the `echo-api-release` API Release of the Api `echo-api` with new note.</span></span>

## <span data-ttu-id="00454-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00454-112">PARAMETERS</span></span>

### <span data-ttu-id="00454-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="00454-113">-ApiId</span></span>
<span data-ttu-id="00454-114">기존 API의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="00454-114">Identifier of existing API.</span></span>
<span data-ttu-id="00454-115">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="00454-115">This parameter is required.</span></span>

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

### <span data-ttu-id="00454-116">-Context</span><span class="sxs-lookup"><span data-stu-id="00454-116">-Context</span></span>
<span data-ttu-id="00454-117">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="00454-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="00454-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="00454-118">This parameter is required.</span></span>

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

### <span data-ttu-id="00454-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00454-119">-DefaultProfile</span></span>
<span data-ttu-id="00454-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="00454-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00454-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00454-121">-InputObject</span></span>
<span data-ttu-id="00454-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease 형식의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="00454-122">Instance of type Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00454-123">-Note</span><span class="sxs-lookup"><span data-stu-id="00454-123">-Note</span></span>
<span data-ttu-id="00454-124">API 릴리스 정보.</span><span class="sxs-lookup"><span data-stu-id="00454-124">Api Release Notes.</span></span>
<span data-ttu-id="00454-125">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="00454-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="00454-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00454-126">-PassThru</span></span>
<span data-ttu-id="00454-127">지정된 경우 설정된 API 릴리스를 나타내는 Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease 형식의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="00454-127">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease type representing the set API Release.</span></span>

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

### <span data-ttu-id="00454-128">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="00454-128">-ReleaseId</span></span>
<span data-ttu-id="00454-129">Api Revision ReleaseId에 대한 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="00454-129">Identifier for the Api Revision ReleaseId.</span></span>
<span data-ttu-id="00454-130">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="00454-130">This parameter is required.</span></span>

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

### <span data-ttu-id="00454-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00454-131">-Confirm</span></span>
<span data-ttu-id="00454-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="00454-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00454-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00454-133">-WhatIf</span></span>
<span data-ttu-id="00454-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="00454-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00454-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="00454-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00454-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00454-136">CommonParameters</span></span>
<span data-ttu-id="00454-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="00454-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00454-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="00454-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00454-139">입력</span><span class="sxs-lookup"><span data-stu-id="00454-139">INPUTS</span></span>

### <span data-ttu-id="00454-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="00454-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="00454-141">System.String</span><span class="sxs-lookup"><span data-stu-id="00454-141">System.String</span></span>

### <span data-ttu-id="00454-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="00454-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="00454-143">출력</span><span class="sxs-lookup"><span data-stu-id="00454-143">OUTPUTS</span></span>

### <span data-ttu-id="00454-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="00454-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="00454-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="00454-145">NOTES</span></span>

## <span data-ttu-id="00454-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="00454-146">RELATED LINKS</span></span>

[<span data-ttu-id="00454-147">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="00454-147">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="00454-148">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="00454-148">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)
