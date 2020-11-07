---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
ms.openlocfilehash: 1141d671db13c3ea44a7ed7bd003574f3c13615c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697918"
---
# <span data-ttu-id="894b3-101">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="894b3-101">Update-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="894b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="894b3-102">SYNOPSIS</span></span>
<span data-ttu-id="894b3-103">특정 Api 릴리스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="894b3-103">Updates a particular Api Release.</span></span>

## <span data-ttu-id="894b3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="894b3-104">SYNTAX</span></span>

### <span data-ttu-id="894b3-105">ExpandedParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="894b3-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementApiRelease -Context <PsApiManagementContext> -ReleaseId <String> -ApiId <String>
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="894b3-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="894b3-106">ByInputObject</span></span>
```
Update-AzApiManagementApiRelease [-Note <String>] -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="894b3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="894b3-107">DESCRIPTION</span></span>
<span data-ttu-id="894b3-108">**업데이트 AzApiManagementApiRelease** Cmdlet은 Azure API Management api 릴리스를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="894b3-108">The **Update-AzApiManagementApiRelease** cmdlet modifies an Azure API Management API Release.</span></span>

## <span data-ttu-id="894b3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="894b3-109">EXAMPLES</span></span>

### <span data-ttu-id="894b3-110">예제 1: API 개정판에 대 한 API 릴리스 업데이트</span><span class="sxs-lookup"><span data-stu-id="894b3-110">Example 1: Updates an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId "echo-api" -ReleaseId "echo-api-release" -Note "Releasing version 2 of the echo-api to public"
```

<span data-ttu-id="894b3-111">이 명령은 `echo-api-release` api의 Api 릴리스를 `echo-api` 새 메모로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="894b3-111">This command updates the `echo-api-release` API Release of the Api `echo-api` with new note.</span></span>

## <span data-ttu-id="894b3-112">변수</span><span class="sxs-lookup"><span data-stu-id="894b3-112">PARAMETERS</span></span>

### <span data-ttu-id="894b3-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="894b3-113">-ApiId</span></span>
<span data-ttu-id="894b3-114">기존 API의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="894b3-114">Identifier of existing API.</span></span>
<span data-ttu-id="894b3-115">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="894b3-115">This parameter is required.</span></span>

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

### <span data-ttu-id="894b3-116">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="894b3-116">-Context</span></span>
<span data-ttu-id="894b3-117">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="894b3-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="894b3-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="894b3-118">This parameter is required.</span></span>

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

### <span data-ttu-id="894b3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="894b3-119">-DefaultProfile</span></span>
<span data-ttu-id="894b3-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="894b3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="894b3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="894b3-121">-InputObject</span></span>
<span data-ttu-id="894b3-122">ApiManagement. ServiceManagement의 인스턴스를 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="894b3-122">Instance of type Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease.</span></span>

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

### <span data-ttu-id="894b3-123">-메모</span><span class="sxs-lookup"><span data-stu-id="894b3-123">-Note</span></span>
<span data-ttu-id="894b3-124">Api 릴리스 정보</span><span class="sxs-lookup"><span data-stu-id="894b3-124">Api Release Notes.</span></span>
<span data-ttu-id="894b3-125">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="894b3-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="894b3-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="894b3-126">-PassThru</span></span>
<span data-ttu-id="894b3-127">지정 된 경우 set API Release를 나타내는 ApiManagement의 인스턴스를 ServiceManagement. PsApiManagementApiRelease 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="894b3-127">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease type representing the set API Release.</span></span>

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

### <span data-ttu-id="894b3-128">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="894b3-128">-ReleaseId</span></span>
<span data-ttu-id="894b3-129">Api 개정판 ReleaseId에 대 한 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="894b3-129">Identifier for the Api Revision ReleaseId.</span></span>
<span data-ttu-id="894b3-130">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="894b3-130">This parameter is required.</span></span>

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

### <span data-ttu-id="894b3-131">-확인</span><span class="sxs-lookup"><span data-stu-id="894b3-131">-Confirm</span></span>
<span data-ttu-id="894b3-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="894b3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="894b3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="894b3-133">-WhatIf</span></span>
<span data-ttu-id="894b3-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="894b3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="894b3-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="894b3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="894b3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="894b3-136">CommonParameters</span></span>
<span data-ttu-id="894b3-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="894b3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="894b3-138">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="894b3-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="894b3-139">입력</span><span class="sxs-lookup"><span data-stu-id="894b3-139">INPUTS</span></span>

### <span data-ttu-id="894b3-140">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="894b3-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="894b3-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="894b3-141">System.String</span></span>

### <span data-ttu-id="894b3-142">ApiManagement. ServiceManagement. \ PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="894b3-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="894b3-143">출력</span><span class="sxs-lookup"><span data-stu-id="894b3-143">OUTPUTS</span></span>

### <span data-ttu-id="894b3-144">ApiManagement. ServiceManagement. \ PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="894b3-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="894b3-145">상속자</span><span class="sxs-lookup"><span data-stu-id="894b3-145">NOTES</span></span>

## <span data-ttu-id="894b3-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="894b3-146">RELATED LINKS</span></span>

[<span data-ttu-id="894b3-147">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="894b3-147">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="894b3-148">새로운 AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="894b3-148">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)
