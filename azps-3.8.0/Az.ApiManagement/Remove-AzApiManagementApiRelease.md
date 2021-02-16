---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
ms.openlocfilehash: 9673df14bdd0f5b7d0e946170a155231e8c4e751
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412659"
---
# <span data-ttu-id="b77cf-101">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b77cf-101">Remove-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="b77cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b77cf-102">SYNOPSIS</span></span>
<span data-ttu-id="b77cf-103">특정 API 릴리스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b77cf-103">Removes a particular API Release</span></span>

## <span data-ttu-id="b77cf-104">구문</span><span class="sxs-lookup"><span data-stu-id="b77cf-104">SYNTAX</span></span>

### <span data-ttu-id="b77cf-105">ByApiReleaseId(기본값)</span><span class="sxs-lookup"><span data-stu-id="b77cf-105">ByApiReleaseId (Default)</span></span>
```
Remove-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ReleaseId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b77cf-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b77cf-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiRelease -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b77cf-107">설명</span><span class="sxs-lookup"><span data-stu-id="b77cf-107">DESCRIPTION</span></span>

<span data-ttu-id="b77cf-108">**Remove-AzAzureRmApiManagementApiRelease** cmdlet은 기존 API 릴리스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b77cf-108">The **Remove-AzAzureRmApiManagementApiRelease** cmdlet removes an existing API Release.</span></span>

## <span data-ttu-id="b77cf-109">예제</span><span class="sxs-lookup"><span data-stu-id="b77cf-109">EXAMPLES</span></span>

### <span data-ttu-id="b77cf-110">예제 1: API 릴리스 제거</span><span class="sxs-lookup"><span data-stu-id="b77cf-110">Example 1: Remove an API Release</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiRelease -Context $apimContext -ApiId "echo-api" -ReleaseId "2"
```

<span data-ttu-id="b77cf-111">이 명령은 지정된 ApiId 및 ReleaseId를 사용하여 API 릴리스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b77cf-111">This command removes the API Release with the specified ApiId and ReleaseId.</span></span>

## <span data-ttu-id="b77cf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b77cf-112">PARAMETERS</span></span>

### <span data-ttu-id="b77cf-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="b77cf-113">-ApiId</span></span>
<span data-ttu-id="b77cf-114">API의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="b77cf-114">Identifier of the API.</span></span>
<span data-ttu-id="b77cf-115">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="b77cf-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b77cf-116">-Context</span><span class="sxs-lookup"><span data-stu-id="b77cf-116">-Context</span></span>
<span data-ttu-id="b77cf-117">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="b77cf-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b77cf-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="b77cf-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b77cf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b77cf-119">-DefaultProfile</span></span>
<span data-ttu-id="b77cf-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b77cf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b77cf-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b77cf-121">-InputObject</span></span>
<span data-ttu-id="b77cf-122">PsApiManagementApiRelease의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="b77cf-122">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="b77cf-123">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="b77cf-123">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b77cf-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b77cf-124">-PassThru</span></span>
<span data-ttu-id="b77cf-125">지정된 경우 작업이 성공하는 경우 true를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="b77cf-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="b77cf-126">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="b77cf-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="b77cf-127">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="b77cf-127">-ReleaseId</span></span>
<span data-ttu-id="b77cf-128">API 릴리스의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="b77cf-128">Identifier of the API Release.</span></span>
<span data-ttu-id="b77cf-129">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="b77cf-129">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b77cf-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b77cf-130">-Confirm</span></span>
<span data-ttu-id="b77cf-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b77cf-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b77cf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b77cf-132">-WhatIf</span></span>
<span data-ttu-id="b77cf-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b77cf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b77cf-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b77cf-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b77cf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b77cf-135">CommonParameters</span></span>
<span data-ttu-id="b77cf-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b77cf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b77cf-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b77cf-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b77cf-138">입력</span><span class="sxs-lookup"><span data-stu-id="b77cf-138">INPUTS</span></span>

### <span data-ttu-id="b77cf-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b77cf-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b77cf-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b77cf-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

### <span data-ttu-id="b77cf-141">System.String</span><span class="sxs-lookup"><span data-stu-id="b77cf-141">System.String</span></span>

## <span data-ttu-id="b77cf-142">출력</span><span class="sxs-lookup"><span data-stu-id="b77cf-142">OUTPUTS</span></span>

### <span data-ttu-id="b77cf-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b77cf-143">System.Boolean</span></span>

## <span data-ttu-id="b77cf-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b77cf-144">NOTES</span></span>

## <span data-ttu-id="b77cf-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b77cf-145">RELATED LINKS</span></span>

[<span data-ttu-id="b77cf-146">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b77cf-146">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="b77cf-147">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b77cf-147">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)

[<span data-ttu-id="b77cf-148">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b77cf-148">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)